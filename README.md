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
| *InSpec Resource* | *Extension Snippet* |
|-------------------|---------------------|
![aws_billing_report](http://inspec.io//docs/reference/resources/aws_billing_report)| :white_check_mark: [aws_billing_report](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_billing_report.json)|
![aws_billing_reports](http://inspec.io//docs/reference/resources/aws_billing_reports)| :white_check_mark: [aws_billing_reports](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_billing_reports.json)|
![aws_cloudtrail_trail](http://inspec.io//docs/reference/resources/aws_cloudtrail_trail)| :white_check_mark: [aws_cloudtrail_trail](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_cloudtrail_trail.json)|
![aws_cloudtrail_trails](http://inspec.io//docs/reference/resources/aws_cloudtrail_trails)| :white_check_mark: [aws_cloudtrail_trails](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_cloudtrail_trails.json)|
![aws_cloudwatch_alarm](http://inspec.io//docs/reference/resources/aws_cloudwatch_alarm)| :white_check_mark: [aws_cloudwatch_alarm](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_cloudwatch_alarm.json)|
![aws_cloudwatch_log_metric_filter](http://inspec.io//docs/reference/resources/aws_cloudwatch_log_metric_filter)| :white_check_mark: [aws_cloudwatch_log_metric_filter](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_cloudwatch_log_metric_filter.json)|
![aws_config_delivery_channel](http://inspec.io//docs/reference/resources/aws_config_delivery_channel)| :white_check_mark: [aws_config_delivery_channel](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_config_delivery_channel.json)|
![aws_config_recorder](http://inspec.io//docs/reference/resources/aws_config_recorder)| :white_check_mark: [aws_config_recorder](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_config_recorder.json)|
![aws_ec2_instance](http://inspec.io//docs/reference/resources/aws_ec2_instance)| :white_check_mark: [aws_ec2_instance](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_ec2_instance.json)|
![aws_ebs_volume](http://inspec.io//docs/reference/resources/aws_ebs_volume)| :white_check_mark: [aws_ebs_volume](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_ebs_volume.json)|
![aws_ebs_volumes](http://inspec.io//docs/reference/resources/aws_ebs_volumes)| :white_check_mark: [aws_ebs_volumes](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_ebs_volumes.json)|
![aws_flow_log](http://inspec.io//docs/reference/resources/aws_flow_log)| :white_check_mark: [aws_flow_log](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_flow_log.json)|
![aws_ec2_instances](http://inspec.io//docs/reference/resources/aws_ec2_instances)| :white_check_mark: [aws_ec2_instances](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_ec2_instances.json)|
![aws_ecs_cluster](http://inspec.io//docs/reference/resources/aws_ecs_cluster)| :white_check_mark: [aws_ecs_cluster](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_ecs_cluster.json)|
![aws_eks_cluster](http://inspec.io//docs/reference/resources/aws_eks_cluster)| :white_check_mark: [aws_eks_cluster](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_eks_cluster.json)|
![aws_elb](http://inspec.io//docs/reference/resources/aws_elb)| :white_check_mark: [aws_elb](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_elb.json)|
![aws_elbs](http://inspec.io//docs/reference/resources/aws_elbs)| :white_check_mark: [aws_elbs](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_elbs.json)|
![aws_iam_access_key](http://inspec.io//docs/reference/resources/aws_iam_access_key)| :white_check_mark: [aws_iam_access_key](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_iam_access_key.json)|
![aws_iam_access_keys](http://inspec.io//docs/reference/resources/aws_iam_access_keys)| :white_check_mark: [aws_iam_access_keys](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_iam_access_keys.json)|
![aws_iam_group](http://inspec.io//docs/reference/resources/aws_iam_group)| :white_check_mark: [aws_iam_group](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_iam_group.json)|
![aws_iam_groups](http://inspec.io//docs/reference/resources/aws_iam_groups)| :white_check_mark: [aws_iam_groups](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_iam_groups.json)|
![aws_iam_password_policy](http://inspec.io//docs/reference/resources/aws_iam_password_policy)| :white_check_mark: [aws_iam_password_policy](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_iam_password_policy.json)|
![aws_iam_policies](http://inspec.io//docs/reference/resources/aws_iam_policies)| :white_check_mark: [aws_iam_policies](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_iam_policies.json)|
![aws_iam_policy](http://inspec.io//docs/reference/resources/aws_iam_policy)| :white_check_mark: [aws_iam_policy](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_iam_policy.json)|
![aws_iam_role](http://inspec.io//docs/reference/resources/aws_iam_role)| :white_check_mark: [aws_iam_role](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_iam_role.json)|
![aws_iam_root_user](http://inspec.io//docs/reference/resources/aws_iam_root_user)| :white_check_mark: [aws_iam_root_user](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_iam_root_user.json)|
![aws_iam_user](http://inspec.io//docs/reference/resources/aws_iam_user)| :white_check_mark: [aws_iam_user](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_iam_user.json)|
![aws_iam_users](http://inspec.io//docs/reference/resources/aws_iam_users)| :white_check_mark: [aws_iam_users](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_iam_users.json)|
![aws_kms_key](http://inspec.io//docs/reference/resources/aws_kms_key)| :white_check_mark: [aws_kms_key](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_kms_key.json)|
![aws_kms_keys](http://inspec.io//docs/reference/resources/aws_kms_keys)| :white_check_mark: [aws_kms_keys](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_kms_keys.json)|
![aws_rds_instance](http://inspec.io//docs/reference/resources/aws_rds_instance)| :white_check_mark: [aws_rds_instance](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_rds_instance.json)|
![aws_route_table](http://inspec.io//docs/reference/resources/aws_route_table)| :white_check_mark: [aws_route_table](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_route_table.json)|
![aws_route_tables](http://inspec.io//docs/reference/resources/aws_route_tables)| :white_check_mark: [aws_route_tables](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_route_tables.json)|
![aws_s3_bucket](http://inspec.io//docs/reference/resources/aws_s3_bucket)| :white_check_mark: [aws_s3_bucket](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_s3_bucket.json)|
![aws_s3_bucket_object](http://inspec.io//docs/reference/resources/aws_s3_bucket_object)| :white_check_mark: [aws_s3_bucket_object](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_s3_bucket_object.json)|
![aws_s3_buckets](http://inspec.io//docs/reference/resources/aws_s3_buckets)| :white_check_mark: [aws_s3_buckets](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_s3_buckets.json)|
![aws_security_group](http://inspec.io//docs/reference/resources/aws_security_group)| :white_check_mark: [aws_security_group](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_security_group.json)|
![aws_security_groups](http://inspec.io//docs/reference/resources/aws_security_groups)| :white_check_mark: [aws_security_groups](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_security_groups.json)|
![aws_sns_subscription](http://inspec.io//docs/reference/resources/aws_sns_subscription)| :white_check_mark: [aws_sns_subscription](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_sns_subscription.json)|
![aws_sns_topic](http://inspec.io//docs/reference/resources/aws_sns_topic)| :white_check_mark: [aws_sns_topic](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_sns_topic.json)|
![aws_sns_topics](http://inspec.io//docs/reference/resources/aws_sns_topics)| :white_check_mark: [aws_sns_topics](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_sns_topics.json)|
![aws_sqs_queue](http://inspec.io//docs/reference/resources/aws_sqs_queue)| :white_check_mark: [aws_sqs_queue](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_sqs_queue.json)|
![aws_subnet](http://inspec.io//docs/reference/resources/aws_subnet)| :white_check_mark: [aws_subnet](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_subnet.json)|
![aws_subnets](http://inspec.io//docs/reference/resources/aws_subnets)| :white_check_mark: [aws_subnets](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_subnets.json)|
![aws_vpc](http://inspec.io//docs/reference/resources/aws_vpc)| :white_check_mark: [aws_vpc](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_vpc.json)|
![aws_vpcs](http://inspec.io//docs/reference/resources/aws_vpcs)| :white_check_mark: [aws_vpcs](https://github.com/chef-training/extension-inspec/tree/master/snippets/aws_vpcs.json)|
![azure_generic_resource](http://inspec.io//docs/reference/resources/azure_generic_resource)| :white_check_mark: [azure_generic_resource](https://github.com/chef-training/extension-inspec/tree/master/snippets/azure_generic_resource.json)|
![azure_resource_group](http://inspec.io//docs/reference/resources/azure_resource_group)| :white_check_mark: [azure_resource_group](https://github.com/chef-training/extension-inspec/tree/master/snippets/azure_resource_group.json)|
![azure_virtual_machine](http://inspec.io//docs/reference/resources/azure_virtual_machine)| :white_check_mark: [azure_virtual_machine](https://github.com/chef-training/extension-inspec/tree/master/snippets/azure_virtual_machine.json)|
![azure_virtual_machine_data_disk](http://inspec.io//docs/reference/resources/azure_virtual_machine_data_disk)| :white_check_mark: [azure_virtual_machine_data_disk](https://github.com/chef-training/extension-inspec/tree/master/snippets/azure_virtual_machine_data_disk.json)|
![aide_conf](http://inspec.io//docs/reference/resources/aide_conf)| :white_check_mark: [aide_conf](https://github.com/chef-training/extension-inspec/tree/master/snippets/aide_conf.json)|
![apache](http://inspec.io//docs/reference/resources/apache)| :white_check_mark: [apache](https://github.com/chef-training/extension-inspec/tree/master/snippets/apache.json)|
![apache_conf](http://inspec.io//docs/reference/resources/apache_conf)| :white_check_mark: [apache_conf](https://github.com/chef-training/extension-inspec/tree/master/snippets/apache_conf.json)|
![apt](http://inspec.io//docs/reference/resources/apt)| :white_check_mark: [apt](https://github.com/chef-training/extension-inspec/tree/master/snippets/apt.json)|
![ppa](http://inspec.io//docs/reference/resources/ppa)| :white_check_mark: [ppa](https://github.com/chef-training/extension-inspec/tree/master/snippets/ppa.json)|
![audit_policy](http://inspec.io//docs/reference/resources/audit_policy)| :white_check_mark: [audit_policy](https://github.com/chef-training/extension-inspec/tree/master/snippets/audit_policy.json)|
![auditd](http://inspec.io//docs/reference/resources/auditd)| :white_check_mark: [auditd](https://github.com/chef-training/extension-inspec/tree/master/snippets/auditd.json)|
![auditd_conf](http://inspec.io//docs/reference/resources/auditd_conf)| :white_check_mark: [auditd_conf](https://github.com/chef-training/extension-inspec/tree/master/snippets/auditd_conf.json)|
![command](http://inspec.io//docs/reference/resources/command)| :white_check_mark: [command](https://github.com/chef-training/extension-inspec/tree/master/snippets/command.json)|
![bash](http://inspec.io//docs/reference/resources/bash)| :white_check_mark: [bash](https://github.com/chef-training/extension-inspec/tree/master/snippets/bash.json)|
![file](http://inspec.io//docs/reference/resources/file)| :white_check_mark: [file](https://github.com/chef-training/extension-inspec/tree/master/snippets/file.json)|
![bond](http://inspec.io//docs/reference/resources/bond)| :white_check_mark: [bond](https://github.com/chef-training/extension-inspec/tree/master/snippets/bond.json)|
![bridge](http://inspec.io//docs/reference/resources/bridge)| :white_check_mark: [bridge](https://github.com/chef-training/extension-inspec/tree/master/snippets/bridge.json)|
![chocolatey_package](http://inspec.io//docs/reference/resources/chocolatey_package)| :white_check_mark: [chocolatey_package](https://github.com/chef-training/extension-inspec/tree/master/snippets/chocolatey_package.json)|
![cran](http://inspec.io//docs/reference/resources/cran)| :white_check_mark: [cran](https://github.com/chef-training/extension-inspec/tree/master/snippets/cran.json)|
![cpan](http://inspec.io//docs/reference/resources/cpan)| :white_check_mark: [cpan](https://github.com/chef-training/extension-inspec/tree/master/snippets/cpan.json)|
![crontab](http://inspec.io//docs/reference/resources/crontab)| :white_check_mark: [crontab](https://github.com/chef-training/extension-inspec/tree/master/snippets/crontab.json)|
![dh_params](http://inspec.io//docs/reference/resources/dh_params)| :white_check_mark: [dh_params](https://github.com/chef-training/extension-inspec/tree/master/snippets/dh_params.json)|
![directory](http://inspec.io//docs/reference/resources/directory)| :white_check_mark: [directory](https://github.com/chef-training/extension-inspec/tree/master/snippets/directory.json)|
![docker](http://inspec.io//docs/reference/resources/docker)| :white_check_mark: [docker](https://github.com/chef-training/extension-inspec/tree/master/snippets/docker.json)|
![docker_container](http://inspec.io//docs/reference/resources/docker_container)| :white_check_mark: [docker_container](https://github.com/chef-training/extension-inspec/tree/master/snippets/docker_container.json)|
![docker_image](http://inspec.io//docs/reference/resources/docker_image)| :white_check_mark: [docker_image](https://github.com/chef-training/extension-inspec/tree/master/snippets/docker_image.json)|
![docker_plugin](http://inspec.io//docs/reference/resources/docker_plugin)| :white_check_mark: [docker_plugin](https://github.com/chef-training/extension-inspec/tree/master/snippets/docker_plugin.json)|
![docker_service](http://inspec.io//docs/reference/resources/docker_service)| :white_check_mark: [docker_service](https://github.com/chef-training/extension-inspec/tree/master/snippets/docker_service.json)|
![package](http://inspec.io//docs/reference/resources/package)| :white_check_mark: [package](https://github.com/chef-training/extension-inspec/tree/master/snippets/package.json)|
![elasticsearch](http://inspec.io//docs/reference/resources/elasticsearch)| :white_check_mark: [elasticsearch](https://github.com/chef-training/extension-inspec/tree/master/snippets/elasticsearch.json)|
![etc_fstab](http://inspec.io//docs/reference/resources/etc_fstab)| :white_check_mark: [etc_fstab](https://github.com/chef-training/extension-inspec/tree/master/snippets/etc_fstab.json)|
![etc_group](http://inspec.io//docs/reference/resources/etc_group)| :white_check_mark: [etc_group](https://github.com/chef-training/extension-inspec/tree/master/snippets/etc_group.json)|
![etc_hosts_allow](http://inspec.io//docs/reference/resources/etc_hosts_allow)| :white_check_mark: [etc_hosts_allow](https://github.com/chef-training/extension-inspec/tree/master/snippets/etc_hosts_allow.json)|
![etc_hosts_deny](http://inspec.io//docs/reference/resources/etc_hosts_deny)| :white_check_mark: [etc_hosts_deny](https://github.com/chef-training/extension-inspec/tree/master/snippets/etc_hosts_deny.json)|
![etc_hosts](http://inspec.io//docs/reference/resources/etc_hosts)| :white_check_mark: [etc_hosts](https://github.com/chef-training/extension-inspec/tree/master/snippets/etc_hosts.json)|
![filesystem](http://inspec.io//docs/reference/resources/filesystem)| :white_check_mark: [filesystem](https://github.com/chef-training/extension-inspec/tree/master/snippets/filesystem.json)|
![firewalld](http://inspec.io//docs/reference/resources/firewalld)| :white_check_mark: [firewalld](https://github.com/chef-training/extension-inspec/tree/master/snippets/firewalld.json)|
![gem](http://inspec.io//docs/reference/resources/gem)| :white_check_mark: [gem](https://github.com/chef-training/extension-inspec/tree/master/snippets/gem.json)|
![groups](http://inspec.io//docs/reference/resources/groups)| :white_check_mark: [groups](https://github.com/chef-training/extension-inspec/tree/master/snippets/groups.json)|
![group](http://inspec.io//docs/reference/resources/group)| :white_check_mark: [group](https://github.com/chef-training/extension-inspec/tree/master/snippets/group.json)|
![grub_conf](http://inspec.io//docs/reference/resources/grub_conf)| :white_check_mark: [grub_conf](https://github.com/chef-training/extension-inspec/tree/master/snippets/grub_conf.json)|
![host](http://inspec.io//docs/reference/resources/host)| :white_check_mark: [host](https://github.com/chef-training/extension-inspec/tree/master/snippets/host.json)|
![http](http://inspec.io//docs/reference/resources/http)| :white_check_mark: [http](https://github.com/chef-training/extension-inspec/tree/master/snippets/http.json)|
![iis_app](http://inspec.io//docs/reference/resources/iis_app)| :white_check_mark: [iis_app](https://github.com/chef-training/extension-inspec/tree/master/snippets/iis_app.json)|
![iis_app_pool](http://inspec.io//docs/reference/resources/iis_app_pool)| :white_check_mark: [iis_app_pool](https://github.com/chef-training/extension-inspec/tree/master/snippets/iis_app_pool.json)|
![iis_site](http://inspec.io//docs/reference/resources/iis_site)| :white_check_mark: [iis_site](https://github.com/chef-training/extension-inspec/tree/master/snippets/iis_site.json)|
![iis_website](http://inspec.io//docs/reference/resources/iis_website)| :white_check_mark: [iis_website](https://github.com/chef-training/extension-inspec/tree/master/snippets/iis_website.json)|
![inetd_conf](http://inspec.io//docs/reference/resources/inetd_conf)| :white_check_mark: [inetd_conf](https://github.com/chef-training/extension-inspec/tree/master/snippets/inetd_conf.json)|
![interface](http://inspec.io//docs/reference/resources/interface)| :white_check_mark: [interface](https://github.com/chef-training/extension-inspec/tree/master/snippets/interface.json)|
![iptables](http://inspec.io//docs/reference/resources/iptables)| :white_check_mark: [iptables](https://github.com/chef-training/extension-inspec/tree/master/snippets/iptables.json)|
![json](http://inspec.io//docs/reference/resources/json)| :white_check_mark: [json](https://github.com/chef-training/extension-inspec/tree/master/snippets/json.json)|
![kernel_module](http://inspec.io//docs/reference/resources/kernel_module)| :white_check_mark: [kernel_module](https://github.com/chef-training/extension-inspec/tree/master/snippets/kernel_module.json)|
![kernel_parameter](http://inspec.io//docs/reference/resources/kernel_parameter)| :white_check_mark: [kernel_parameter](https://github.com/chef-training/extension-inspec/tree/master/snippets/kernel_parameter.json)|
![linux_kernel_parameter](http://inspec.io//docs/reference/resources/linux_kernel_parameter)| :white_check_mark: [linux_kernel_parameter](https://github.com/chef-training/extension-inspec/tree/master/snippets/linux_kernel_parameter.json)|
![key_rsa](http://inspec.io//docs/reference/resources/key_rsa)| :white_check_mark: [key_rsa](https://github.com/chef-training/extension-inspec/tree/master/snippets/key_rsa.json)|
![ksh](http://inspec.io//docs/reference/resources/ksh)| :white_check_mark: [ksh](https://github.com/chef-training/extension-inspec/tree/master/snippets/ksh.json)|
![limits_conf](http://inspec.io//docs/reference/resources/limits_conf)| :white_check_mark: [limits_conf](https://github.com/chef-training/extension-inspec/tree/master/snippets/limits_conf.json)|
![login_defs](http://inspec.io//docs/reference/resources/login_defs)| :white_check_mark: [login_defs](https://github.com/chef-training/extension-inspec/tree/master/snippets/login_defs.json)|
![mount](http://inspec.io//docs/reference/resources/mount)| :white_check_mark: [mount](https://github.com/chef-training/extension-inspec/tree/master/snippets/mount.json)|
![mssql_session](http://inspec.io//docs/reference/resources/mssql_session)| :white_check_mark: [mssql_session](https://github.com/chef-training/extension-inspec/tree/master/snippets/mssql_session.json)|
![mysql](http://inspec.io//docs/reference/resources/mysql)| :white_check_mark: [mysql](https://github.com/chef-training/extension-inspec/tree/master/snippets/mysql.json)|
![mysql_conf](http://inspec.io//docs/reference/resources/mysql_conf)| :white_check_mark: [mysql_conf](https://github.com/chef-training/extension-inspec/tree/master/snippets/mysql_conf.json)|
![mysql_session](http://inspec.io//docs/reference/resources/mysql_session)| :white_check_mark: [mysql_session](https://github.com/chef-training/extension-inspec/tree/master/snippets/mysql_session.json)|
![nginx](http://inspec.io//docs/reference/resources/nginx)| :white_check_mark: [nginx](https://github.com/chef-training/extension-inspec/tree/master/snippets/nginx.json)|
![nginx_conf](http://inspec.io//docs/reference/resources/nginx_conf)| :white_check_mark: [nginx_conf](https://github.com/chef-training/extension-inspec/tree/master/snippets/nginx_conf.json)|
![npm](http://inspec.io//docs/reference/resources/npm)| :white_check_mark: [npm](https://github.com/chef-training/extension-inspec/tree/master/snippets/npm.json)|
![ntp_conf](http://inspec.io//docs/reference/resources/ntp_conf)| :white_check_mark: [ntp_conf](https://github.com/chef-training/extension-inspec/tree/master/snippets/ntp_conf.json)|
![oneget](http://inspec.io//docs/reference/resources/oneget)| :white_check_mark: [oneget](https://github.com/chef-training/extension-inspec/tree/master/snippets/oneget.json)|
![oracledb_session](http://inspec.io//docs/reference/resources/oracledb_session)| :white_check_mark: [oracledb_session](https://github.com/chef-training/extension-inspec/tree/master/snippets/oracledb_session.json)|
![platform](http://inspec.io//docs/reference/resources/platform)| :white_check_mark: [platform](https://github.com/chef-training/extension-inspec/tree/master/snippets/platform.json)|
![os](http://inspec.io//docs/reference/resources/os)| :white_check_mark: [os](https://github.com/chef-training/extension-inspec/tree/master/snippets/os.json)|
![os_env](http://inspec.io//docs/reference/resources/os_env)| :white_check_mark: [os_env](https://github.com/chef-training/extension-inspec/tree/master/snippets/os_env.json)|
![packages](http://inspec.io//docs/reference/resources/packages)| :white_check_mark: [packages](https://github.com/chef-training/extension-inspec/tree/master/snippets/packages.json)|
![parse_config](http://inspec.io//docs/reference/resources/parse_config)| :white_check_mark: [parse_config](https://github.com/chef-training/extension-inspec/tree/master/snippets/parse_config.json)|
![parse_config_file](http://inspec.io//docs/reference/resources/parse_config_file)| :white_check_mark: [parse_config_file](https://github.com/chef-training/extension-inspec/tree/master/snippets/parse_config_file.json)|
![passwd](http://inspec.io//docs/reference/resources/passwd)| :white_check_mark: [passwd](https://github.com/chef-training/extension-inspec/tree/master/snippets/passwd.json)|
![pip](http://inspec.io//docs/reference/resources/pip)| :white_check_mark: [pip](https://github.com/chef-training/extension-inspec/tree/master/snippets/pip.json)|
![port](http://inspec.io//docs/reference/resources/port)| :white_check_mark: [port](https://github.com/chef-training/extension-inspec/tree/master/snippets/port.json)|
![postgres](http://inspec.io//docs/reference/resources/postgres)| :white_check_mark: [postgres](https://github.com/chef-training/extension-inspec/tree/master/snippets/postgres.json)|
![postgres_conf](http://inspec.io//docs/reference/resources/postgres_conf)| :white_check_mark: [postgres_conf](https://github.com/chef-training/extension-inspec/tree/master/snippets/postgres_conf.json)|
![postgres_hba_conf](http://inspec.io//docs/reference/resources/postgres_hba_conf)| :white_check_mark: [postgres_hba_conf](https://github.com/chef-training/extension-inspec/tree/master/snippets/postgres_hba_conf.json)|
![postgres_ident_conf](http://inspec.io//docs/reference/resources/postgres_ident_conf)| :white_check_mark: [postgres_ident_conf](https://github.com/chef-training/extension-inspec/tree/master/snippets/postgres_ident_conf.json)|
![postgres_session](http://inspec.io//docs/reference/resources/postgres_session)| :white_check_mark: [postgres_session](https://github.com/chef-training/extension-inspec/tree/master/snippets/postgres_session.json)|
![powershell](http://inspec.io//docs/reference/resources/powershell)| :white_check_mark: [powershell](https://github.com/chef-training/extension-inspec/tree/master/snippets/powershell.json)|
![script](http://inspec.io//docs/reference/resources/script)| :white_check_mark: [script](https://github.com/chef-training/extension-inspec/tree/master/snippets/script.json)|
![processes](http://inspec.io//docs/reference/resources/processes)| :white_check_mark: [processes](https://github.com/chef-training/extension-inspec/tree/master/snippets/processes.json)|
![rabbitmq_config](http://inspec.io//docs/reference/resources/rabbitmq_config)| :white_check_mark: [rabbitmq_config](https://github.com/chef-training/extension-inspec/tree/master/snippets/rabbitmq_config.json)|
![registry_key](http://inspec.io//docs/reference/resources/registry_key)| :white_check_mark: [registry_key](https://github.com/chef-training/extension-inspec/tree/master/snippets/registry_key.json)|
![windows_registry_key](http://inspec.io//docs/reference/resources/windows_registry_key)| :white_check_mark: [windows_registry_key](https://github.com/chef-training/extension-inspec/tree/master/snippets/windows_registry_key.json)|
![security_identifier](http://inspec.io//docs/reference/resources/security_identifier)| :white_check_mark: [security_identifier](https://github.com/chef-training/extension-inspec/tree/master/snippets/security_identifier.json)|
![security_policy](http://inspec.io//docs/reference/resources/security_policy)| :white_check_mark: [security_policy](https://github.com/chef-training/extension-inspec/tree/master/snippets/security_policy.json)|
![service](http://inspec.io//docs/reference/resources/service)| :white_check_mark: [service](https://github.com/chef-training/extension-inspec/tree/master/snippets/service.json)|
![systemd_service](http://inspec.io//docs/reference/resources/systemd_service)| :white_check_mark: [systemd_service](https://github.com/chef-training/extension-inspec/tree/master/snippets/systemd_service.json)|
![upstart_service](http://inspec.io//docs/reference/resources/upstart_service)| :white_check_mark: [upstart_service](https://github.com/chef-training/extension-inspec/tree/master/snippets/upstart_service.json)|
![sysv_service](http://inspec.io//docs/reference/resources/sysv_service)| :white_check_mark: [sysv_service](https://github.com/chef-training/extension-inspec/tree/master/snippets/sysv_service.json)|
![bsd_service](http://inspec.io//docs/reference/resources/bsd_service)| :white_check_mark: [bsd_service](https://github.com/chef-training/extension-inspec/tree/master/snippets/bsd_service.json)|
![launchd_service](http://inspec.io//docs/reference/resources/launchd_service)| :white_check_mark: [launchd_service](https://github.com/chef-training/extension-inspec/tree/master/snippets/launchd_service.json)|
![runit_service](http://inspec.io//docs/reference/resources/runit_service)| :white_check_mark: [runit_service](https://github.com/chef-training/extension-inspec/tree/master/snippets/runit_service.json)|
![shadow](http://inspec.io//docs/reference/resources/shadow)| :white_check_mark: [shadow](https://github.com/chef-training/extension-inspec/tree/master/snippets/shadow.json)|
![ssh_config](http://inspec.io//docs/reference/resources/ssh_config)| :white_check_mark: [ssh_config](https://github.com/chef-training/extension-inspec/tree/master/snippets/ssh_config.json)|
![sshd_config](http://inspec.io//docs/reference/resources/sshd_config)| :white_check_mark: [sshd_config](https://github.com/chef-training/extension-inspec/tree/master/snippets/sshd_config.json)|
![ssl](http://inspec.io//docs/reference/resources/ssl)| :white_check_mark: [ssl](https://github.com/chef-training/extension-inspec/tree/master/snippets/ssl.json)|
![sys_info](http://inspec.io//docs/reference/resources/sys_info)| :white_check_mark: [sys_info](https://github.com/chef-training/extension-inspec/tree/master/snippets/sys_info.json)|
![toml](http://inspec.io//docs/reference/resources/toml)| :white_check_mark: [toml](https://github.com/chef-training/extension-inspec/tree/master/snippets/toml.json)|
![users](http://inspec.io//docs/reference/resources/users)| :white_check_mark: [users](https://github.com/chef-training/extension-inspec/tree/master/snippets/users.json)|
![user](http://inspec.io//docs/reference/resources/user)| :white_check_mark: [user](https://github.com/chef-training/extension-inspec/tree/master/snippets/user.json)|
![vbscript](http://inspec.io//docs/reference/resources/vbscript)| :white_check_mark: [vbscript](https://github.com/chef-training/extension-inspec/tree/master/snippets/vbscript.json)|
![virtualization](http://inspec.io//docs/reference/resources/virtualization)| :white_check_mark: [virtualization](https://github.com/chef-training/extension-inspec/tree/master/snippets/virtualization.json)|
![windows_feature](http://inspec.io//docs/reference/resources/windows_feature)| :white_check_mark: [windows_feature](https://github.com/chef-training/extension-inspec/tree/master/snippets/windows_feature.json)|
![windows_hotfix](http://inspec.io//docs/reference/resources/windows_hotfix)| :white_check_mark: [windows_hotfix](https://github.com/chef-training/extension-inspec/tree/master/snippets/windows_hotfix.json)|
![windows_task](http://inspec.io//docs/reference/resources/windows_task)| :white_check_mark: [windows_task](https://github.com/chef-training/extension-inspec/tree/master/snippets/windows_task.json)|
![wmi](http://inspec.io//docs/reference/resources/wmi)| :white_check_mark: [wmi](https://github.com/chef-training/extension-inspec/tree/master/snippets/wmi.json)|
![x509_certificate](http://inspec.io//docs/reference/resources/x509_certificate)| :white_check_mark: [x509_certificate](https://github.com/chef-training/extension-inspec/tree/master/snippets/x509_certificate.json)|
![xinetd_conf](http://inspec.io//docs/reference/resources/xinetd_conf)| :white_check_mark: [xinetd_conf](https://github.com/chef-training/extension-inspec/tree/master/snippets/xinetd_conf.json)|
![yum](http://inspec.io//docs/reference/resources/yum)| :white_check_mark: [yum](https://github.com/chef-training/extension-inspec/tree/master/snippets/yum.json)|
![zfs_dataset](http://inspec.io//docs/reference/resources/zfs_dataset)| :white_check_mark: [zfs_dataset](https://github.com/chef-training/extension-inspec/tree/master/snippets/zfs_dataset.json)|
![zfs_pool](http://inspec.io//docs/reference/resources/zfs_pool)| :white_check_mark: [zfs_pool](https://github.com/chef-training/extension-inspec/tree/master/snippets/zfs_pool.json)|
![yaml](http://inspec.io//docs/reference/resources/yaml)| :white_check_mark: [yaml](https://github.com/chef-training/extension-inspec/tree/master/snippets/yaml.json)|
![csv](http://inspec.io//docs/reference/resources/csv)| :white_check_mark: [csv](https://github.com/chef-training/extension-inspec/tree/master/snippets/csv.json)|
![ini](http://inspec.io//docs/reference/resources/ini)| :white_check_mark: [ini](https://github.com/chef-training/extension-inspec/tree/master/snippets/ini.json)|
![xml](http://inspec.io//docs/reference/resources/xml)| :white_check_mark: [xml](https://github.com/chef-training/extension-inspec/tree/master/snippets/xml.json)|

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