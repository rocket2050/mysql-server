# Ansible Role: Java

Installs mysql-server for RedHat/CentOS(6) and Ubuntu linux server.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values:

    # The defaults provided by this role are specific to each distribution.
    mysql_root_password:
       - root

Set the mysql_root_passowrd accordingly.


## Dependencies

None.

## Example Playbook (using default package, usually OpenJDK 7)

    - hosts: mysql-server
      roles:
        - mysql-server

## Example Playbook (install OpenJDK 7)

For RHEL / CentOS:

    - hosts: mysql-server
      roles:
        - role: mysql-server
          when: "ansible_os_family == 'RedHat'"
          mysql_root_password:
            - root

## License

MIT / BSD

## Author Information

www.opstree.com

blog.opstree.com
