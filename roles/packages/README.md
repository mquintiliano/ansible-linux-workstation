# Ansible Role: packages

A simple role to manage software packages on Fedora workstation, adding extra packages and removing a few packages not frequently used.

## Requirements

No requirements at all.

## Role Variables

Available variable are listed below (see `defaults/main.yml`):

Controls whether you wish to remove some software installed by default within the workstation:

  - delete_software

## Dependencies

None.

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: workstation
      roles:
         - { role: packages, vars: {remove_packages: gnome-boxes }}

## License

Apache License 2.0
