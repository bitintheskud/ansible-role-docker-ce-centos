# ansible-docker-ce-centos

ansible role to install Docker CE on CentOS 7

## Requirements

Nothing.

## Role Variables

name | required | default | example | description
--- | --- | --- | --- | ---
docker_centos_users | no | [] | ["vagrant"] | users added to docker group
docker_version | no | "" (latest) | "17.12.1" | Install a specific docker version. 
docker_install_dir | no | "/var/docker/install" | "/tmp" | download script in this directory


## Dependencies

 - Centos 7 (see AWS market place) 

## Example Playbook

```yaml

---
- hosts: localhost
  connection: local
  gather_facts: true
  become: yes

  vars:
     docker_centos_users:
       - vagrant

  environment: 
    VERSION: "{{ docker_version }}"

  roles:
    - ansible-role-docker-ce-centos
```

## License

[MIT](LICENSE)
