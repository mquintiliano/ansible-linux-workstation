# Ansible Linux Workstaion

Ansible playbook that automates the ordinary tasks of setting up my Linux machines after a fresh install.

## Supported distros

Currently, the supported distros are:

- [x] Fedora
- [ ] Others

## Roles

The `post-install.yml` playbook relies on roles to take care of each post install related task.

- Available Roles
  - bitwarden   - Install the Bitwarden CLI Tool via NPM
  - duckdb      - Install the DuckDB from https://duckdb.org
  - omf         - Install Oh My Fish
  - packages    - Manage the availability of software on the Linux machine 
  - set_repos   - Enable extra repositories (includes RPM Fusion free/non-free)
  - starship    - Install the Starship prompt
  - tweaks      - Add Gnome Shell extensions and apply a few settings tweak
  - virt        - Add Virtualization (graphical environment)

## Usage

Once we get our Linux machine installed, clone this repo and run the bootstrap script. 
```
$ git clone https://github.com/mquintiliano/ansible-linux-workstation
```
The bootstrap config is a small script that ensures Ansible is installed on the workstation and then calls our Ansible playbook.
```
$ cd ansible-linux-workstation
$ ./bootstrap_config
```
> [!TIP]
> We can also select some specific role to be executed instead of all of them at once: 
```
$ ./bootstrap_config --help
Usage: bootstrap_config [-h | -l | TASKS]
  
  OPTIONS
    -h, --help         print this help
    -l, --list         list all configuration tasks

  Running specifics configuration tasks
    ./bootstrap_config repos,virt

  NOTE
    With no arguments, bootstrap_config will execute all configuration tasks.
```



