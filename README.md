# ansible-docker-ce-centos

ansible role to install Docker CE on CentOS 7

## Requirements

Nothing.

## Role Variables

name | required | default | example | description
--- | --- | --- | --- | ---
docker_centos_users | no | [] | ["vagrant"] | users added to docker group


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
  roles:
    - ansible-role-docker-ce-centos
```

## License

[MIT](LICENSE)
