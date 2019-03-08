# [InSpec](http://inspec.io) Extension for Visual Studio Code

This extension for Visual Studio Code provides grammar and code snippets for InSpec when using [Visual Studio Code](http://code.visualstudio.com).

![InSpec Extention Demo](/images/vscode-inspec-demo.gif)

## Features

#### Syntax/keyword highlighting:

* InSpec - control blocks
* InSpec - describe blocks
* InSpec - resource

## Installation
 * You will need to install Visual Studio Code `1.5` or higher.
 * From the command palette `Ctrl-Shift-P` (Windows, Linux) or `Cmd-Shift-P` (OSX) select `Install Extension`, choose `Inspec` and reload Visual Studio Code.
 * Once the Extention is installed to enable it, choose the `InSpec` language from the bottom right corner (the default is `Plain Text`)
 It should then look like this

   ![InSpec Extention Enabled](/images/vscode-inspec.jpg)

 *  .... or use the keyboard shortcut `(Ctrl-K) M & type Inspec` if you happen to be scared of mice :)

## Usage
InSpec in it's simplest form is _describe_ block in which you describe a _resource's_ expected configuration. e.g.

```ruby
describe file('/etc/myapp.conf') do
  it { should exist }
  its('mode') { should cmp '0644' }
end
```

**TIP:** Try typing the resource you want to use i.e. `file` and let the snippet create the describe block for you

![InSpec describe demo](/images/vscode-inspec-demo.gif)

## What is InSpec?
InSpec is an open-source testing framework for infrastructure with a human- and machine-readable language for specifying compliance, security and policy requirements.

### Where can I find more?
The [inspec.io](http://inspec.io) website is full of documentation and links to download the code
There is also an _interactive demo_ in which will allow you try it out with a web browser.


## InSpec Snippet Support matrix
[//]: # ( Use a :x: if we don't have support)
[//]: # ( Use a :white_check_mark: if we do have support provide link to source code)

| *InSpec Resource* | *Extension Snippet* |
|-------------------|---------------------|
|[apache_conf](http://inspec.io//docs/reference/resources/apache_conf)| :white_check_mark: [apache_conf.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/apache_conf.json)|
|[apt](http://inspec.io//docs/reference/resources/apt)| :white_check_mark: [apt.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/apt.json)|
|[audit_policy](http://inspec.io//docs/reference/resources/audit_policy)| :white_check_mark: [auditd_conf.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/auditd_conf.json)|
|[auditd_conf](http://inspec.io//docs/reference/resources/auditd_conf)| :white_check_mark: [auditd_rules.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/auditd_rules.json)|
|[auditd_rules](http://inspec.io//docs/reference/resources/auditd_rules)| :white_check_mark: [audit_policy.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/audit_policy.json)|
|[bash](http://inspec.io//docs/reference/resources/bash)| :white_check_mark: [bash.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/bash.json)|
|[bond](http://inspec.io//docs/reference/resources/bond)| :white_check_mark: [bond.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/bond.json)|
|[bridge](http://inspec.io//docs/reference/resources/bridge)| :white_check_mark: [bridge.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/bridge.json)|
|[bsd_service](http://inspec.io//docs/reference/resources/bsd_service)| :white_check_mark: [bsd_service.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/bsd_service.json)|
|[command](http://inspec.io//docs/reference/resources/command)| :white_check_mark: [command.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/command.json)|
|[csv](http://inspec.io//docs/reference/resources/csv)| :white_check_mark: [csv.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/csv.json)|
|[directory](http://inspec.io//docs/reference/resources/directory)| :white_check_mark: [directory.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/directory.json)|
|[etc_group](http://inspec.io//docs/reference/resources/etc_group)| :white_check_mark: [etc_group.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/etc_group.json)|
|[etc_passwd](http://inspec.io//docs/reference/resources/etc_passwd)| :white_check_mark: [etc_passwd.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/etc_passwd.json)|
|[etc_shadow](http://inspec.io//docs/reference/resources/etc_shadow)| :white_check_mark: [etc_shadow.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/etc_shadow.json)|
|[file](http://inspec.io//docs/reference/resources/file)| :white_check_mark: [file.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/file.json)|
|[gem](http://inspec.io//docs/reference/resources/gem)| :white_check_mark: [gem.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/gem.json)|
|[group](http://inspec.io//docs/reference/resources/group)| :white_check_mark: [group.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/group.json)|
|[grub_conf](http://inspec.io//docs/reference/resources/grub_conf)| :white_check_mark: [grub_conf.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/grub_conf.json)|
|[host](http://inspec.io//docs/reference/resources/host)| :white_check_mark: [host.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/host.json)|
|[iis_site](http://inspec.io//docs/reference/resources/iis_site)| :white_check_mark: [iis_site.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/iis_site.json)|
|[inetd_conf](http://inspec.io//docs/reference/resources/inetd_conf)| :white_check_mark: [inetd_conf.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/inetd_conf.json)|
|[ini](http://inspec.io//docs/reference/resources/ini)| :white_check_mark: [ini.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/ini.json)|
|[interface](http://inspec.io//docs/reference/resources/interface)| :white_check_mark: [interface.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/interface.json)|
|[iptables](http://inspec.io//docs/reference/resources/iptables)| :white_check_mark: [iptables.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/iptables.json)|
|[json](http://inspec.io//docs/reference/resources/json)| :white_check_mark: [json.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/json.json)|
|[kernel_module](http://inspec.io//docs/reference/resources/kernel_module)| :white_check_mark: [kernel_module.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/kernel_module.json)|
|[kernel_parameter](http://inspec.io//docs/reference/resources/kernel_parameter)| :white_check_mark: [language.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/language.json)|
|[launchd_service](http://inspec.io//docs/reference/resources/launchd_service)| :white_check_mark: [launchd_service.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/launchd_service.json)|
|[limits_conf](http://inspec.io//docs/reference/resources/limits_conf)| :white_check_mark: [limits_conf.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/limits_conf.json)|
|[login_def](http://inspec.io//docs/reference/resources/login_def)| :white_check_mark: [login_defs.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/login_defs.json)|
|[mount](http://inspec.io//docs/reference/resources/mount)| :white_check_mark: [mount.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/mount.json)|
|[mysql_conf](http://inspec.io//docs/reference/resources/mysql_conf)| :white_check_mark: [mysql_conf.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/mysql_conf.json)|
|[mysql_session](http://inspec.io//docs/reference/resources/mysql_session)| :white_check_mark: [mysql_session.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/mysql_session.json)|
|[npm](http://inspec.io//docs/reference/resources/npm)| :white_check_mark: [npm.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/npm.json)|
|[ntp_conf](http://inspec.io//docs/reference/resources/ntp_conf)| :white_check_mark: [ntp_conf.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/ntp_conf.json)|
|[oneget](http://inspec.io//docs/reference/resources/oneget)| :white_check_mark: [oneget.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/oneget.json)|
|[os](http://inspec.io//docs/reference/resources/os)| :white_check_mark: [os.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/os.json)|
|[os_env](http://inspec.io//docs/reference/resources/os_env)| :white_check_mark: [os_env.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/os_env.json)|
|[package](http://inspec.io//docs/reference/resources/package)| :white_check_mark: [package.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/package.json)|
|[parse_config](http://inspec.io//docs/reference/resources/parse_config)| :white_check_mark: [parse_config.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/parse_config.json)|
|[parse_config_file](http://inspec.io//docs/reference/resources/parse_config_file)| :white_check_mark: [parse_config_file.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/parse_config_file.json)|
|[pip](http://inspec.io//docs/reference/resources/pip)| :white_check_mark: [pip.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/pip.json)|
|[port](http://inspec.io//docs/reference/resources/port)| :white_check_mark: [port.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/port.json)|
|[postgres_conf](http://inspec.io//docs/reference/resources/postgres_conf)| :white_check_mark: [postgres_conf.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/postgres_conf.json)|
|[postgres_session](http://inspec.io//docs/reference/resources/postgres_session)| :white_check_mark: [postgres_session.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/postgres_session.json)|
|[powershell](http://inspec.io//docs/reference/resources/powershell)| :white_check_mark: [powershell.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/powershell.json)|
|[process](http://inspec.io//docs/reference/resources/process)| :white_check_mark: [processes.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/processes.json)|
|[registry_key](http://inspec.io//docs/reference/resources/registry_key)| :white_check_mark: [registry_key.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/registry_key.json)|
|[runit_service](http://inspec.io//docs/reference/resources/runit_service)| :white_check_mark: [runit_service.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/runit_service.json)|
|[security_policy](http://inspec.io//docs/reference/resources/security_policy)| :white_check_mark: [security_policy.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/security_policy.json)|
|[service](http://inspec.io//docs/reference/resources/service)| :white_check_mark: [service.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/service.json)|
|[ssh_config](http://inspec.io//docs/reference/resources/ssh_config)| :white_check_mark: [sshd_config.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/sshd_config.json)|
|[sshd_config](http://inspec.io//docs/reference/resources/sshd_config)| :white_check_mark: [ssh_config.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/ssh_config.json)|
|[ssl](http://inspec.io//docs/reference/resources/ssl)| :white_check_mark: [ssl.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/ssl.json)|
|[sys_info](http://inspec.io//docs/reference/resources/sys_info)| :white_check_mark: [systemd_service.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/systemd_service.json)|
|[systemd_service](http://inspec.io//docs/reference/resources/systemd_service)| :white_check_mark: [sysv_service.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/sysv_service.json)|
|[sysv_service](http://inspec.io//docs/reference/resources/sysv_service)| :white_check_mark: [sys_info.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/sys_info.json)|
|[upstart_service](http://inspec.io//docs/reference/resources/upstart_service)| :white_check_mark: [upstart_service.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/upstart_service.json)|
|[user](http://inspec.io//docs/reference/resources/user)| :white_check_mark: [user.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/user.json)|
|[users](http://inspec.io//docs/reference/resources/users)| :white_check_mark: [users.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/users.json)|
|[vbscript](http://inspec.io//docs/reference/resources/vbscript)| :white_check_mark: [vbscript.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/vbscript.json)|
|[windows_feature](http://inspec.io//docs/reference/resources/windows_feature)| :white_check_mark: [windows_feature.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/windows_feature.json)|
|[windows_task](http://inspec.io//docs/reference/resources/windows_task)| :white_check_mark: [windows_task.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/windows_task.json)|
|[wmi](http://inspec.io//docs/reference/resources/wmi)| :white_check_mark: [wmi.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/wmi.json)|
|[xinetd_conf](http://inspec.io//docs/reference/resources/xinetd_conf)| :white_check_mark: [xinetd_conf.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/xinetd_conf.json)|
|[yaml](http://inspec.io//docs/reference/resources/yaml)| :white_check_mark: [yaml.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/yaml.json)|
|[yum](http://inspec.io//docs/reference/resources/yum)| :white_check_mark: [yum.json](https://github.com/chef-training/extension-inspec/tree/master/snippets/yum.json)|

## Publishing

This describes the setup procedure for the tools and tokens required to publish the extension: https://code.visualstudio.com/docs/tools/vscecli

```bash
# Install the dependencies for the project
$ npm install
# Publish a version of the extension
$ npm publish (major|minor|patch)
```

## Contributions

Contributions are welcomed, please create an issue and a pull requests via the [project homepage](https://github.com/chef-training/extension-inspec).

## Version History

Review the [CHANGELOG.md](CHANGELOG.md)