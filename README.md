# UNDER CONSTRUCTION - DONT USE IT!!!

# Ansible Role Podman Containers

[![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT)
[![GitHub tag](https://img.shields.io/github/tag/OnkelDom/ansible-node-exporter.svg)](https://github.com/OnkelDom/ansible-node-exporter/tags)
[![GitHub issues](https://img.shields.io/github/issues/OnkelDom/ansible-role-podman-container)](https://github.com/OnkelDom/ansible-role-podman-container/issues)
[![GitHub license](https://img.shields.io/github/license/OnkelDom/ansible-role-podman-container)](https://github.com/OnkelDom/ansible-role-podman-container/blob/master/LICENSE)

## Description

Deploy podman containers with systemd and manage there configs.

## Requirements

- Ansible >= 2.5 (It might work on previous versions, but we cannot guarantee it)

## Role Variables

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) file as well as in table below.

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `proxy_env` | "[]" | Set proxy settings |
| `podman_container_base_config_dir` | "/etc/podman-container" | Set the root path for alle container configs. |
| `podman_container_base_data_dir` | "/var/lib/podman-container" | Set the root path for alle container data directories. |
| `podman_container_base_user` | podman | Set the default podman container running user. |
| `podman_container_base_group` | podman | Set the default podman container running group. |

## Example

### Playbook

```yaml
- hosts: all
  roles:
    - onkeldom.ansible-role-podman-container
  vars:
```

## Contributing

See [contributor guideline](CONTRIBUTING.md).

## License

This project is licensed under MIT License. See [LICENSE](/LICENSE) for more details.
