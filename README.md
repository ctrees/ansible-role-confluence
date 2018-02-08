# Ansible role `confluence`

[//]: # todo [![Travis](https://img.shields.io/travis/ctrees/ansible-role-confluence.svg)](https://travis-ci.org/ctrees/ansible-role-confluence)
[//]: # todo [![GitHub release](https://img.shields.io/github/release/ctrees/ansible-role-confluence.svg)](https://github.com/ctrees/ansible-role-confluence)
[//]: # todo [![GitHub license](https://img.shields.io/github/license/ctrees/ansible-role-confluence.svg)](https://github.com/ctrees/ansible-role-confluence/blob/master/LICENSE)
[//]: # todo [![Ansible Role](https://img.shields.io/badge/galaxy-ctrees.confluence-blue.svg)](https://galaxy.ansible.com/ctrees/confluence)

Ansible Role for Atlassian Confluence Installation.

An Ansible role for installing an Atlassian Confluence Server. Specifically, the responsibilities of this role are to:

-

## Requirements

- java
- mariadb

## Role Variables

| Variable   | Default | Comments (type)  |
| :---       | :---    | :---             |
| `confluence_owner` | confluence | owner |
| `confluence_group` | confluence | group |
| `confluence_home` | "/var/atlassian/application-data/confluence" | Location for the $CONFLUENCE_HOME directory. |
| `confluence_catalina` | "/opt/atlassian/confluence" | Location for the $CONFLUENCE_CATALINA directory. |
| `confluence_connector_port` | "8090" | Confluence Apache Tomcat connector and server port. |
| `confluence_server_port` | "8000" | Confluence Apache Tomcat connector and server port. |
| `confluence_jvm_minimum_memory` | "1024m" | Confluence JVM minimal memory usage. |
| `confluence_jvm_maximum_memory` | "1024m" | Confluence JVM maximum memory usage. |
| `confluence_context_path` | "~" | Context path for Confluence isntallation. |
| `confluence_proxy_name` | "~" | `http` or `https`, and supply `confluence_proxy_name` with its domain name. |
| `confluence_schema` | "~" | If Confluence running behide reverse proxy, setup `confluence_scheme` with whatever |
| `confluence_jvm_support_recommended_args` | "-Datlassian.plugins.enable.wait=300" | Atlassian Support recommended JVM arguments. |
| `confluence_url` | "https://downloads.atlassian.com/software/confluence/downloads/atlassian-confluence-6.6.2.tar.gz" | URL for download Confluence archive. |

## Dependencies

- src: https://github.com/bertvv/ansible-role-rh-base
- src: https://github.com/geerlingguy/ansible-role-java
- src: https://github.com/bertvv/ansible-role-mariadb

## Example Playbook

[//]: # todo - See the test playbooks in either the [Vagrant](https://github.com/ctrees/ansible-role-confluence/blob/vagrant-tests/test.yml) or [Docker](https://github.com/ctrees/ansible-role-confluence/blob/docker-tests/test.yml) test environment. See the section Testing for details.

## Testing

There are two types of test environments available. One powered by Vagrant, another by Docker. The latter is suitable for running automated tests on Travis-CI. Test code is kept in separate orphan branches. For details of how to set up these test environments on your own machine, see the README files in the respective branches:

- Vagrant: [vagrant-tests](https://github.com/ctrees/ansible-role-confluence/tree/vagrant-tests)
- Docker: [docker-tests](https://github.com/ctrees/ansible-role-confluence/tree/docker-tests)

## Contributing

Issues, feature requests, ideas are appreciated and can be posted in the Issues section.

Pull requests are also very welcome. The best way to submit a PR is by first creating a fork of this Github project, then creating a topic branch for the suggested change and pushing that branch to your own fork. Github can then easily create a PR based on that branch. Don't forget to add your name to the contributor list below!

## Contributors

- [Chris Trees](https://github.com/ctrees/) (maintainer)

