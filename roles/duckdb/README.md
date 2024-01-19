# Ansible Role: DuckDB

Installs the DuckDB binary from https://duckdb.org

## Requirements

* Ansible version (ansible-core) 2.16.0+
* Note: This role uses the builtin 'unarchive' module which requires `zipinfo` and `gtar`|`unzip` command on the target host.

## Role Variables

None.

## Dependencies

None. 

## Example Playbook

    - hosts: workstation
      roles:
         - role: duckdb

# License

Apache License 2.0
