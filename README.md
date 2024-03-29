# ROLE dginhoux.docker_compose



## DESCRIPTION

This ansible role install, configure and uninstall docker-compose.<br />
It grab the binary from github repository.



## REQUIREMENTS

#### SUPPORTED PLATFORMS

| Platform | Versions |
|----------|----------|
| Debian | all |
| EL | all |
| Fedora | all |
| Ubuntu | all |

#### ANSIBLE VERSION

Ansible >= 2.13

#### DEPENDENCIES

None.



## INSTALLATION

#### ANSIBLE GALAXY

```shell
ansible-galaxy install dginhoux.docker_compose
```
#### GIT

```shell
git clone https://github.com/dginhoux/ansible_role.docker_compose dginhoux.docker_compose
```


## USAGE

#### EXAMPLE PLAYBOOK

```yaml
- hosts: all
  tasks:
    - name: start role dginhoux.docker_compose
      ansible.builtin.include_role:
        name: dginhoux.docker_compose
```


## VARIABLES

#### DEFAULT VARIABLES

Defaults variables defined in `defaults/main.yml`

#### EXAMPLES VARIABLES

```yaml
docker_compose_action: install
docker_compose_executable: /usr/local/bin/docker-compose
docker_compose_github_repo: docker/compose
docker_compose_version: "
```

#### DEFAULT OS SPECIFIC VARIABLES

Those variables files are located in `vars/*.yml` are used to handle OS differences.<br />
One of theses is loaded dynamically during role runtime using the `include_vars` module and set OS specifics variable's.

`NOT USED BY THIS ROLE`


## AUTHOR

Dany GINHOUX - https://github.com/dginhoux



## LICENSE

MIT


## INSPIRED FROM

This role is inspired and forked from this role https://github.com/atosatto/ansible-dockerswarm created by atosatto

