# Ansible Role: tweaks

A simple role to install a few Gnome Shell extensions and apply some settings tweak. 

## Requirements

* Ansible version (ansible-core) 2.16.0+
* Note: This role usues the DConf module in order to change the dconf database, this module depends on `psutil` Python library (version 4.0.0 and upwards) so the tweaks role ensures the library package is installed (see `tasks/requirements.yml`)  

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    enable_tweaks: true
    install_gnome_extensions: true

## Dependencies

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: workstation
      roles:
         - { role: tweaks, vars: { install_gnome_extensions: false }}

## License

Apache License 2.0
