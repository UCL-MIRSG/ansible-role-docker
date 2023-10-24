# mirsg.docker

This role is for installing [docker-ce](https://docs.docker.com/engine/install/) on CentOS 7 or Rocky Linux 8.

## Role Variables

| Name                       | Description                                                                                          |
| -------------------------- | ---------------------------------------------------------------------------------------------------- |
| `docker_owner`             | The OS user that will have ownership of the Docker service file and directory. Defaults to `root`    |
| `docker_group`             | The OS group that will have ownership of the Docker service file and directory. Defaults to `root`   |
| `docker_service_directory` | The path to the Docker service. Defaults to `/etc/systemd/system/docker.service.d`                   |
| `docker_service_name`      | The name of the Docker service. Defaults to `docker`                                                 |
| `docker_rpm_gpg_key_url`   | The url of the Docker repository GPG key. Defaults to `https://download.docker.com/linux/centos/gpg` |
| `docker_repo_baseurl`      | URL to the directory containing the repodata. Defaults to `https://download.docker.com/linux/centos` |
| `docker_yum_package`       | The name of the Docker package. Defaults to `docker`                                                 |

## Installation

Include in a requirements.yml file as follows:

```yaml
roles:
  - src: https://github.com/UCL-MIRSG/ansible-role-docker.git
    version: x.y.z
    name: mirsg.docker
```

## Example Playbook

```yaml
- hosts: servers
  roles:
    - { role: mirsg.docker }
```

## License

[BSD 3-Clause License](https://github.com/UCL-MIRSG/ansible-role-docker/blob/main/LICENSE).

## Author Information

This role was created by the [Medical Imaging Research Software Group](https://www.ucl.ac.uk/advanced-research-computing/expertise/research-software-development/medical-imaging-research-software-group) at [UCL](https://www.ucl.ac.uk/).
