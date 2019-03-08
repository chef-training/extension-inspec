# CHANGELOG

This file describes the differences between all versions. At the moment this document is maintained by hand so there be omissions and errors.

### 0.5.2 - 03/08/2019

* Adds the ability to generate markdown table (Lynn Frank)
* Updates the README to show resource support matrix (Lynn Frank)
* Adds Ruby tooling to sync resources (Lynn Frank)

### 0.5.0 - 03/08/2019

* Adds `zfs_pool`, `zfs_dataset`, `xml`, `x509_certificate`, `windows_registry_key`, `windows_hotfix`, `virtualization`, `toml`, `shadow`, `security_identifier`, `script`, `rabbitmq_config`, `ppa`, `postgres_ident_conf`, `postgres_hba_conf`, `postgres`, `platform`, `passwd`, `packages`, `oracledb_session`, `nginx_conf`, `nginx`, `mysql`, `mssql_session`, `linux_kernel_parameter`, `ksh`, `key_rsa`, `kernel_parameter`, `iis_website`, `iis_app_pool`, `iis_app`, `http`, `groups`, `firewalld`, `filesystem`, `etc_hosts_deny`, `etc_hosts_allow`, `etc_hosts`, `etc_fstab`, `elasticsearch`, `docker_service`, `docker_plugin`, `docker_image`, `docker_container`, `docker`, `dh_params`, `crontab`, `cran`, `cpan`, `chocolatey_package`, `azure_virtual_machine_data_disk`, `azure_virtual_machine`, `azure_resource_group`, `azure_generic_resource`, `aws_vpcs`, `aws_vpc`, `aws_subnets`, `aws_subnet`, `aws_sqs_queue`, `aws_sns_topics`, `aws_sns_topic`, `aws_sns_subscription`, `aws_security_groups`, `aws_security_group`, `aws_s3_buckets`, `aws_s3_bucket_object`, `aws_s3_bucket`, `aws_route_tables`, `aws_route_table`, `aws_rds_instance`, `aws_kms_keys`, `aws_kms_key`, `aws_iam_users`, `aws_iam_user`, `aws_iam_root_user`, `aws_iam_role`, `aws_iam_policy`, `aws_iam_policies`, `aws_iam_password_policy`, `aws_iam_groups`, `aws_iam_group`, `aws_iam_access_keys`, `aws_iam_access_key`, `aws_flow_log`, `aws_elbs`, `aws_elb`, `aws_eks_cluster`, `aws_ecs_cluster`, `aws_ec2_instances`, `aws_ec2_instance`, `aws_ebs_volumes`, `aws_ebs_volume`, `aws_config_recorder`, `aws_config_delivery_channel`, `aws_cloudwatch_log_metric_filter`, `aws_cloudwatch_alarm`, `aws_cloudtrail_trails`, `aws_cloudtrail_trail`, `aws_billing_reports`, `aws_billing_report`, `auditd`, `apache`, and `aide_conf` generic resource snippet with (Lynn Frank)

* Removes `auditd_rules`, `etc_passwd`, and `etc_shadow` snippets (Lynn Frank)

### 0.4.4 - 03/08/2019

* Adds CHANGELOG.md as separate file.

### 0.4.3 - 03/08/2019

* Updates the host resource to use `protocol` instead of `proto` ([kmf](https://github.com/kmf))
* Adds snippets for `crontab`, `docker`, `docker_container`, `docker_image`, and `http` ([gordonbondon](https://github.com/gordonbondon))
* Adds Apache 2.0 License
* Adds publishing dependencies and tasks

### 0.1.2 - 06/12/2016
* Added a snippet for the```[windows_task]```resource ([username-is-already-taken2](https://github.com/username-is-already-taken2))

### 0.1.1 - 15/11/2016
* This was is the initial release of extension
