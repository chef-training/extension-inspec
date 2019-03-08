require 'erb'
require 'inspec'
require 'json'

task :default => "snippets:resources:status"

namespace :snippets do

  def inspec_version
    "InSpec #{Inspec::VERSION}"
  end

  def inspec_resources
    Inspec::Resource.registry.keys
  end

  def extension_package_file
    "package.json"
  end

  def extension_package_desc
    JSON.parse(File.read(extension_package_file))
  end

  def update_resource_definitions(resources)
    updated_extension_package_desc = extension_package_desc
    base_language_snippets = [ { language: 'inspec', path: './snippets/_language-inspec.json' } ]
    updated_extension_package_desc['contributes']['snippets'] = base_language_snippets + resources.map {|name| { language: 'inspec', path: snippet_path_from_resource_name(name) } }
    File.write(extension_package_file, JSON.pretty_generate(updated_extension_package_desc, { indent: '    ' }))
  end

  def existing_resources_definitions
    extension_package_desc['contributes']['snippets'].reject { |definition| File.basename(definition['path']).start_with?('_') }
  end

  def existing_resources_registered
    existing_resources_definitions.map { |definition| File.basename(definition['path'],template_ext) }
  end

  def snippets_path
    "snippets"
  end

  def template_ext
    '.json'
  end

  # Ignore any snippets that start with an underscore      
  def existing_resource_snippets_paths
    Dir["#{snippets_path}/*#{template_ext}"].reject { |path| File.basename(path).start_with?('_') }
  end

  def existing_resource_snippets
    existing_resource_snippets_paths.map { |path| File.basename(path,template_ext) }
  end

  def snippet_template
    ERB.new File.read("snippet-template#{template_ext}")
  end

  def snippet_path_from_resource_name(name)
    "./#{snippets_path}/#{name}#{template_ext}"
  end

  namespace :resources do
    desc 'Display the resources as they are found across the various locations'
    task :status do

      puts ""
      puts "  Checking for resources in InSpec runtime (#{inspec_version}), extension manifest (#{extension_package_file}), and snippet definitions (./#{snippets_path})"

      puts "  . found #{inspec_resources.count.to_s.rjust(4)} resources defined in #{inspec_version}"
      puts "  . found #{existing_resources_definitions.count.to_s.rjust(4)} resources defined in the extension manifest (#{extension_package_file})"
      puts "  . found #{existing_resource_snippets.count.to_s.rjust(4)} resources defined in snippet definitions in (./#{snippets_path})"
      
      puts ""

      unregistered_resources = inspec_resources - existing_resources_registered
      
      puts "  . found #{unregistered_resources.count.to_s.rjust(4)} unregistered resources"
      unless unregistered_resources.empty?
        puts "\t#{unregistered_resources.join(', ')}\n" 
        puts "\n  ! FIX by running $ rake snippets:resources:register\n\n"
      end

      resources_to_deregister = existing_resources_registered - inspec_resources
      
      puts "  . found #{resources_to_deregister.count.to_s.rjust(4)} resources that need to be de-registered"
      unless resources_to_deregister.empty?
        puts "\t#{resources_to_deregister.join(', ')}\n"
        puts "\n  ! FIX by running $ rake snippets:resources:purge:registry\n\n"
      end
      
      missing_snippet_resources = inspec_resources - existing_resource_snippets
      
      puts "  . found #{missing_snippet_resources.count.to_s.rjust(4)} resource snippets missing"
      unless missing_snippet_resources.empty?
        puts "\t#{missing_snippet_resources.join(', ')}\n"
        puts "\n  ! FIX by running $ rake snippets:resources:create\n\n"
      end
      
      resources_to_remove_snippet = existing_resource_snippets - inspec_resources
      
      puts "  . found #{resources_to_remove_snippet.count.to_s.rjust(4)} resource snippets to remove"
      unless resources_to_remove_snippet.empty?
        puts "\t#{resources_to_remove_snippet.join(', ')}\n"
        puts "\n  ! FIX by running $ rake rake snippets:resources:purge:snippets\n\n"
      end

      puts ""
    end

    desc 'Purges missing resources, creates snippets, registers them, and then commits them all'
    task :update => [:purge, :create, :register, :commit] do
      puts "  * UPDATE of resources is complete"
    end

    desc 'purge from the extension registry and the resource snippets file'
    task :purge => [ 'purge:registry', 'purge:snippets' ]

    desc 'purge from the extension registry all snippets missing from InSpec'
    task 'purge:registry' => [:status] do
      resources_to_deregister = existing_resources_registered - inspec_resources

      if resources_to_deregister.empty?
        puts "  . no resource registrations to purge"
      else
        puts "  ! purge #{resources_to_deregister.count.to_s.rjust(4)} snippet registrations"
        puts "\t#{resources_to_deregister.join(',')}"
        update_resource_definitions(existing_resources_registered - resources_to_deregister)
      end
    end

    desc 'purge from the snippet files missing from InSpec'
    task 'purge:snippets' => [:status] do
      resources_to_remove_snippet = existing_resource_snippets - inspec_resources

      if resources_to_remove_snippet.empty?
        puts "  . no resource snippets to purge"
      else
        puts "  ! purge #{resources_to_remove_snippet.count.to_s.rjust(4)} snippets"
        puts "\t#{resources_to_remove_snippet.join(',')}"

        resources_to_remove_snippet.each do |resource|
          `git rm #{snippet_path_from_resource_name(resource)}`
        end
      end
    end

    desc 'Create missing resource snippets'
    task :create => [:status] do
      puts "  CREATE missing resources snippets"

      missing_resources = inspec_resources - existing_resource_snippets

      missing_resources.each do |resource|
        new_snippet_path = "snippets/#{resource}#{template_ext}"
        puts "    + creating snippet #{resource} at #{new_snippet_path}"

        # Assigning this to an instance variable for use the template
        @resource = resource
        File.write(new_snippet_path,snippet_template.result(binding))
      end
    end

    desc 'Register missing resource snippets'
    task :register => [:status] do
      puts "  REGISTER missing resources snippets"

      resources_to_register = existing_resource_snippets - existing_resources_registered

      if resources_to_register.empty?
        puts "    . no resources need to be registered"
      else
        puts "    + #{resources_to_register.count.to_s.rjust(4)} snippet registrations"
        puts "\t#{resources_to_register.join(',')}"
        update_resource_definitions(existing_resource_snippets)
      end
    end

    desc "Commits snippet files that are currently staged"
    task :commit => [:status] do
      puts "  COMMIT new snippets"
      
      puts "  + generating snippets commit manifest"
      commit_subject = ""
      commit_body = ""
      
      staged_snippets = `git --no-pager diff --cached --name-status snippets`
      added_snippets = staged_snippets.lines.find_all { |line| line.start_with?('A') }
      
      unless added_snippets.empty?
        added_subject = "adds #{added_snippets.count} snippet#{added_snippets.count == 1 ? '' : 's'}"
        added_body = added_snippets.map { |file| " * adds the #{File.basename(file.split(' ').last,template_ext)} resource" }.join("\n")
      end

      removed_snippets = staged_snippets.lines.find_all { |line| line.start_with?('D') }

      unless removed_snippets.empty?
        removed_subject = "removes #{removed_snippets.count} snippet#{removed_snippets.count == 1 ? '' : 's'}"
        removed_body = removed_snippets.map { |file| " * removes the #{File.basename(file.split(' ').last,template_ext)} resource" }.join("\n")
      end

      [ added_subject, removed_subject ]

      commit_subject += added_subject if added_subject
      commit_body += added_body if added_body
      commit_subject += " and " if !commit_subject.empty? && removed_subject
      commit_subject += removed_subject if removed_subject
      commit_body += "\n" if !commit_body.empty? && removed_body
      commit_body += removed_body if removed_body

      commit_subject.capitalize!
      
      if commit_subject
        puts "git commit -m \"#{commit_subject}\n#{commit_body}\""
      end
    end
   end

  def extension_version
    extension_package_desc["version"]
  end
end

namespace :changelog do
  task :calc do
    puts "  . building CHANGELOG since version #{extension_version}"
    results = `git --no-pager log --format="%s (%an)"`
    new_changes, old_changes = results.split("\n#{extension_version}",2)
    
    new_changes.lines.each do |commit|
      puts "* #{commit}"
    end
  end
end
