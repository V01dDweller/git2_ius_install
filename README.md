# git2_ius_install

**Last update:** 12/26/2022<br>
Ansible role that installs git version 2.x with git-lfs on EL 7 Linux via the
IUS yum repo. Note that it will automatically remove git 1.8.

## Requirements

* Internet connection

## Dependencies

None.

## Example Usage

### 1. Install the role

```cmd
ansible-galaxy install V01dDweller.git2_ius_install
```

### 2. Create a short playbook

```cmd
touch git2_install.yml
```

... add the following:

```yaml
# file: git2_install.yml
---
- name: Installing Git2 from IUS
  hosts: all
  become: yes
  roles:
    - role: V01dDweller.git2_ius_install
      tags: git
```

### 3. Run the playbook

```cmd
ansible-playbook git2_install.yml
```

### 4. Validate

```
$ git --version
git version 2.16.6
```

## License

BSD

## Author Information

by V01dDweller

