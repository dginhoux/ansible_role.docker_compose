# :computer: ROLE dginhoux.docker_compose

## :scroll: DESCRIPTION

This ansible role install, configure and uninstall docker-compose binary from github repository



## :nut_and_bolt: REQUIREMENTS

#### SUPPORTED PLATFORMS

This role require a supported platform. 
It will skip node with unsupported platform to avoid any compatibility problem.
This behaviour can be bypassed by settings this variable `asserts_bypass=True`.

| Platform | Versions |
|----------|----------|
| Debian | buster, bullseye |
| Fedora | 33, 34, 35, 36 |
| EL | 7, 8 |


#### ANSIBLE VERSION

Ansible >= 2.12


#### DEPENDENCIES

None.


## :inbox_tray: INSTALLATION

#### ANSIBLE GALAXY

```shell
ansible-galaxy install dginhoux.docker_compose
```

#### GIT

```shell
git clone https://github.com/dginhoux/ansible_role.docker_compose dginhoux.docker_compose
```


## :rocket: USAGE

#### EXAMPLE PLAYBOOK

```yaml
- hosts: all
  roles:
    - name: start role dginhoux.docker_compose
      ansible.builtin.include_role:
        name: dginhoux.docker_compose
      vars:
        docker_compose_action: install
        docker_compose_executable: /usr/local/bin/docker-compose
        docker_compose_github_repo: docker/compose
        docker_compose_version: ''
        
```


## :factory: VARIABLES
#### DEFAULT VARIABLES
Role default variables from `defaults/main.yml` : 

| Variable Name | Value |
|---------------|-------|
|docker_compose_action | <pre> install </pre> |
|docker_compose_version | <pre>  </pre> |
|docker_compose_github_repo | <pre> docker/compose </pre> |
|docker_compose_executable | <pre> /usr/local/bin/docker-compose </pre> |


#### CONTEXT VARIABLES

Those variables are located in `vars/*.yml` are used to handle OS differences ; One of theses is loaded dynamically during role
runtime using the `include_vars` module and set OS specifics variable's.





## :man: AUTHOR

[![Author](https://img.shields.io/badge/maintained%20by-dginhoux-e00000?style=flat-square)](https://github.com/dginhoux)


## :bookmark_tabs: LICENSE

[![License](https://img.shields.io/github/license/dginhoux/ansible_role.docker_compose?style=flat-square)](https://github.com/dginhoux/ansible_role.docker_compose/blob/master/LICENSE)