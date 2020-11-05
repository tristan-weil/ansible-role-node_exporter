# Ansible Role: node_exporter

An Ansible Role that installs and configures `node_exporter`.

**NOTE**: this role uses the integrated package system for the folowing OS:
- OpenBSD

[![Actions Status](https://github.com/tristan-weil/ansible-role-node_exporter/workflows/molecule/badge.svg?branch=master)](https://github.com/tristan-weil/ansible-role-node_exporter/actions)

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

Mandatory variables:

| Variable      | Description |
| :------------ | :---------- |

Optional variables:

| Variable      | Default | Description |
| :------------ | :------ | :---------- |
| node_exporter_options | []    | a list of extra-configurations |

If the package system is not used, the following variables are available to handle directly the artifacts:

| Variable      | Default | Description |
| :------------ | :------ | :---------- |
| node_exporter_artifact_version | 1.0.1 | the version |
| node_exporter_artifact_url | https://github.com/prometheus/node_exporter/rele...tar.gz | the path to the artifacts to install |
| node_exporter_artifact_sum_url  | https://github.com/prometheus/node_exporter/relea.../sha256sums.txt | the path to the SUMS file |
| node_exporter_artifact_sum_algo | sha256 | the hash algorithm used in `node_exporter_artifact_sum_url` |
| node_exporter_artifact_version_flag_path | /etc/node_exporter.version | the files prevents reinstallation of the artifacts |
| node_exporter_artifact_tmpdir | /tmp/node_exporter | the installation work directory |
| node_exporter_force_update | False | *True/False* to force the update of the artifacts |
| node_exporter_daemon_nofiles | 65536 | the maximum number of files the daemon can open |
| node_exporter_daemon_nproc | 512  | the maximum number of processes the daemon can have |

## Example Playbook

    - hosts: 'webservers'
      roles:
        - role: 'ansible-role-node_exporter'

## Todo

None.

## Dependencies

See [requirements_galaxy.yml](https://github.com/tristan-weil/ansible-role-node_exporter/blob/master/requirements_galaxy.yml)

## Supported platforms

See [meta/main.yml](https://github.com/tristan-weil/ansible-role-node_exporter/blob/master/meta/main.yml)

## License

See [LICENSE.md](LICENSE.md)
