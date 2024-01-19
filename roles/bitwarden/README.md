# Ansible Role: Bitwarden CLI

Installs the Bitwarden Command-line Tool via NPM package manager.

## Requirements

* Ansible version (ansible-core) 2.16.0+
* Requires the nodejs-npm package installed. See the packages role on this repository.

## Role Variables

Available variable are listed below (see `defaults/main.yml`):

Add bitwarden cli to $HOME/.local/bin/ 

 - bitwarden_cli

## Dependencies

This role uses NPM to install Bitwarden CLI. Note: nodejs-npm is installed as part of the packages role on this repository.

## Example Playbook

    - hosts: fedora
      roles:
         - role: bitwarden

## License

Apache License 2.0
