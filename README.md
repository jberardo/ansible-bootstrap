# Bootstrap Ansible Role

Boostrap tasks to prepare a Ubuntu machine for other roles.

Two main tasks are:
- Creation of personal user with ssh key, etc
- Tries to remove apt lock files so other roles can use apt and not run into errors

## Requirements

None.

## Variables

See `defaults/main.yml`.

`user`: User name to be created

`user_password`: User password

## Example

```yml
- hosts: host1
  become: yes
  vars_files:
    - vars/main.yml
  roles:
    - bootstrap
```