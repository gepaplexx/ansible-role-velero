# Ansible Role: velero

![MIT](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)
![GitHub Workflow Status](https://img.shields.io/github/workflow/status/racqspace/ansible-role-velero/Main?style=flat-square)
![GitHub last commit](https://img.shields.io/github/last-commit/racqspace/ansible-role-velero?style=flat-square)
![GitHub Release Date](https://img.shields.io/github/release-date/racqspace/ansible-role-velero?style=flat-square)
![Maintenance](https://img.shields.io/maintenance/yes/2022?style=flat-square)

Installing velero.

## Role Variables

Variable Name | Default Value | Description
------------ | ------------- | -------------
velero_repository_url | https://vmware-tanzu.github.io/helm-charts | URL of the velero chart repository
velero_repository_name | vmware-tanzu | Name of the velero chart repository
velero_chart_name | velero | Name of the velero chart
velero_namespace | velero | Namespace of the velero installation
velero_s3_bucket | bucket | Name of the S3 bucket to use for backup storage
velero_s3_region | minio | Name of the S3 region to use for backup storage
velero_s3_url | https://10.20.26.45:9000 | URL of the S3 bucket to use for backup storage
velero_s3_access_key | miniouser | Access key of the S3 bucket to use for backup storage
velero_s3_secret_key | minio1234 | Secret key of the S3 bucket to use for backup storage


## Role Usage Examples

Example for installing velero in a dedicated namespace `velero`.

```yaml
- hosts: all
  roles:
  - role: gepaplexx.velero
```

## License

MIT

## Author Information

This role was created in 2021 by [Marcel Haupt](https://github.com/mahaupt).

Contributions by:

- [@mahaupt](https://github.com/mahaupt)
