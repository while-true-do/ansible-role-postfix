[![Build Status](https://travis-ci.org/while-true-do/ansible-role-postfix.svg?branch=master)](https://travis-ci.org/while-true-do/ansible-role-postfix)

# Ansible Role: postfix
| A role to install and configure postfix.

- can configure a local postfix mta

## Motivation

Mailing is one of the major communications for servers. Postfix is commonly used in RedHat Systems and CentOS.

## Installation

Install from [Ansible Galaxy](https://galaxy.ansible.com/while_true_do/postfix)

```
ansible-galaxy install while_true_do.postfix
```

Install from [Github](https://github.com/while-true-do/ansible-role-postfix)

```
git clone https://github.com/while-true-do/ansible-role-postfix.git while_true_do.postfix
```

## Requirements

Used Modules:

-   [template_module](https://docs.ansible.com/ansible/latest/template_module.html)
-   [include_module](https://docs.ansible.com/ansible/latest/include_tasks_module.html)
-   [service_module](http://docs.ansible.com/ansible/latest/service_module.html)
-   [packages_module](http://docs.ansible.com/ansible/latest/package_module.html)

## Dependencies

None.

## Role Variables

```yaml
# defaults/main.yml
# defaults/main.yml for postfix
#
# You can set the state to ["present"|"absent"|"latest"]
wtd_postfix_state: "present"
wtd_postfix_packages: "postfix"

# Usage can be ["localmta"]
# TODO: Implement other modes like "mailrelay"
wtd_postfix_usage: "localmta"

wtd_postfix_config_path: "/etc/postfix"

wtd_postfix_queue_directory: "/var/spool/postfix"
wtd_postfix_data_directory: "/var/lib/postfix"
wtd_postfix_mail_owner: "postfix"

wtd_postfix_myhostname: "{{ ansible_hostname }}"
wtd_postfix_mydomain: "{{ ansible_domain }}"
wtd_postfix_myorigin: ""

wtd_postfix_inet_interface: "all"
wtd_postfix_relayhost: ""

wtd_postfix_home_mailbox: "Maildir/"

# TODO: pcp-pmda-postfix + dependency for wtd.pcp should be implemented later
```

## Example Playbook

Simple Example:

```yaml
- hosts: servers 
  roles:
    - { role: while_true_do.postfix }
```

## Testing

All tests are located in [test directory](./tests/).

Basic testing:

```
bash ./tests/test-spelling.sh
bash ./tests/test-ansible.sh
```

## Contribute / Bugs

Thank you so much for considering to contribute. Every contribution helps us.
We are really happy, when somebody is joining the hard work. Please have a look 
at the links first.

-   [Code of Conduct](./docs/CODE_OF_CONDUCT.md)
-   [Contribution Guidelines](./docs/CONTRIBUTING.md)
-   [Create an issue or Request](https://github.com/while-true-do/ansible-role-postfix/issues)
-   [See who was contributing already](https://github.com/while-true-do/ansible-role-postfix/graphs/contributors)

## License

This work is licensed under a [BSD License](https://opensource.org/licenses/BSD-3-Clause).

## Author Information

Site: [while-true-do.org](https://while-true-do.org)

Mail: [hello@while-true-do.org](mailto:hello@while-true-do.org)
