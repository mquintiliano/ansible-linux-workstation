# Ansible Role: virt

A role to add Virtualization software support to the Fedora Workstation. For more details please check the Fedora [Getting started with virtualization](https://docs.fedoraproject.org/en-US/quick-docs/getting-started-with-virtualization/) guide.

## Requirements

KVM requires a CPU with virtualization extensions, found on most consumer CPUs. These extensions are called Intel VT or AMD-V. To check whether you have CPU support, run the following command:

    $ egrep '^flags.*(vmx|svm)' /proc/cpuinfo

## Role Variables

The variable below holds the list of virtualization related packages to be installed (see `defaults/main.yml`):

    virtualization_plus: true
    virt_supp (Hashicorp Vagrant) 

## Dependencies

None.

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: workstation
      roles:
         - role: virt

## License

Apache License 2.0
