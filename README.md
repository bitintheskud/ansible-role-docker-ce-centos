# ansible-docker-ce-centos

ansible role to install Docker CE on CentOS 7

## Requirements

Nothing.

## Role Variables

name | required | default | example | description
--- | --- | --- | --- | ---
docker_centos_users | no | [] | ["vagrant"] | users added to docker group
docker_version | no | [] | "17.12.1" | install a specific version. Default is to install latest available.


## Dependencies

None

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
     docker_version:
       - 17.12.1

  roles:
    - ansible-role-docker-ce-centos
```

## License

[MIT](LICENSE)
