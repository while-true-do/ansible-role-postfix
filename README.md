[![Build Status](https://travis-ci.org/while-true-do/ansible-role-postfix.svg?branch=master)](https://travis-ci.org/while-true-do/ansible-role-postfix)

# Ansible Role: postfix
| A short description **what** the role does goes here.

<!-- 
-  Explain a bit more, if needed.
-  You can use bullets or write a small text
-->

## Motivation

<!-- Explain a bit **why** this role is needed. -->

## Installation

Install from [Ansible Galaxy](https://galaxy.ansible.com/while-true-do/postfix)

```
ansible-galaxy install while-true-do.postfix
```

Install from [Github](https://github.com/while-true-do/ansible-role-postfix)

```
git clone https://github.com/while-true-do/ansible-role-postfix.git while-true-do.postfix
```

## Requirements

Used Modules:

-   [module1](link)
-   [module2](link)

## Dependencies

<!--
Describe, if other roles are needed and link them here.
You also have to put the dependencies in the requirements.yml.

```
ansible-galaxy install -r requirements.yml
```

If nothing is needed, please write "None."
-->

## Role Variables

<!-- 
The variable files should explain itself and pasted/linked here.
Explanation should be done **in** the files, if needed. 
-->

```yaml
# defaults/main.yml
foo: bar
```

```yaml
# vars/main.yml
bar: foo
```

## Example Playbook

Simple Example:

```yaml
- hosts: servers 
  roles:
    - { role: while-true-do.postfix }
```

Advanced Example:

```yaml
- hosts: servers 
  roles:
    - { role: while-true-do.postfix, foo: bar, bar: foo }
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