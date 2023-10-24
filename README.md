# mirsg.docker

This role is for installing [docker-ce](https://docs.docker.com/engine/install/) on CentOS7 or RockyLinux8.

## Role Variables

All variables are nested in the `docker` dictionary. See [defaults/main.yml](defaults/main.yml).

| Name               | Description                                                                                             |
| ------------------ | ------------------------------------------------------------------------------------------------------- |
| `owner`            | The OS user that will have ownership of the Docker service file and directory. Defaults to `root`       |
| `group`            | The OS group that will have ownership of the Docker service file and directory. Defaults to `root`      |
| `service_file_dir` | The path to the Docker service. Defaults to `/etc/systemd/system/docker.service.d`                      |
| `service_name`     | The name of the Docker service. Defaults to `docker`                                                    |
| `repo_url`         | The url of the Docker repository. Defaults to `https://download.docker.com/linux/centos/docker-ce.repo` |
| `yum_package`      | The name of the Docker package. Defaults to `docker`                                                    |

## Installation

Include in a requirements.yml file as follows:

```yaml
roles:
  - src: https://github.com/UCL-MIRSG/ansible-role-docker.git
    version: vx.x.x
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
