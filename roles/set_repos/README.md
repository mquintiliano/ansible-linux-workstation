# Ansible Role: pkg-repos

An Ansible role that install and enable extra repositories like RPM Fusion free and non-free (optional, check Role Variables and Example Playbook below) along with the Fedora Workstation / third party repositories package. It also enables by default the Google Chrome repository.

## Requirements

* Ansible version (ansible-core) 2.16.0+

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    add_rpmfusion_nonfree: true
    enable_chrome_repo: true

Note: For the list of third-party repositories to be installed, see `vars/main.yml`

## Dependencies

None.

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: workstation
      roles:
        - { role: pkg-repos, vars: {enable_chrome_repo: "false"}} 

## License

Apache License 2.0
