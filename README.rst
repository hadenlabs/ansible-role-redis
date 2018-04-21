Ansible Role Redis
##################

|Build Status| |Ansible Galaxy| |GitHub issues| |Average time to resolve an issue| |Percentage of issues still open| |GitHub license|

:Version: 0.0.0
:Web: https://github.com/hadenlabs/ansible-role-redis
:Download: http://github.com/hadenlabs/ansible-role-redis
:Source: http://github.com/hadenlabs/ansible-role-redis
:Keywords: ansible-role-redis

.. contents:: Table of Contents:
    :local:

Ansible Galaxy role for `Redis`_.

Requirements:
=============

List of applications:

- `Python 3.6.1`_
- `Docker`_
- `Docker Compose`_

Install
=======

Install it with the following command:

.. code-block:: bash

    $ ansible-galaxy install hadenlabs.redis

Role Variables
==============

The default role variables in ``defaults/main.yml`` are:

.. code-block:: yaml

    nothing


Dependencies
============

None

Example Playbook
================

See the `examples <./examples/>`__ directory.

To run this playbook with default settings, create a basic playbook like
this:

.. code:: yaml

        - hosts: servers
          roles:
            - hadenlabs.redis

To install a specific version:

.. code:: yaml

      - hosts: servers
        roles:
          - { role: hadenlabs.redis }

.. code:: yaml

        - hosts: servers
          roles:
             - role: hadenlabs.redis
               python_pyenv_path: "{{ home }}/pyenv"
               python_pyenv_owner: "{{ instance_owner }}"
               python_pyenv_update_git_install: no
               python_pyenv_python_versions:
                 - "3.5.1"
                 - "2.7.9"
               python_pyenv_delete_virtualenvs:
                 - venv_name: "delete_venv_name"
               python_pyenv_virtualenvs:
                 - venv_name: "latest_v3"
                   py_version: "3.5.1"
                 - venv_name: "latest_v2"
                   py_version: "2.7.9"

License
=======

MIT

Changelog
=========

Please see `CHANGELOG`_ for more information what
has changed recently.

Contributing
============

Please see `CONTRIBUTING`_ for details.

Credits
=======

-  `author`_
-  `contributors`_

Made with :heart: :coffee: and :pizza: by `author`_ and `company`_.

.. Badges:

.. |Build Status| image:: https://travis-ci.org/hadenlabs/ansible-role-redis.svg
   :target: https://travis-ci.org/hadenlabs/ansible-role-redis
.. |Ansible Galaxy| image:: https://img.shields.io/badge/galaxy-hadenlabs.redis-blue.svg
   :target: https://galaxy.ansible.com/hadenlabs/ansible-role-redis/
.. |GitHub issues| image:: https://img.shields.io/github/issues/hadenlabs/ansible-role-redis.svg
   :target: https://github.com/hadenlabs/ansible-role-redis/issues
.. |Average time to resolve an issue| image:: http://isitmaintained.com/badge/resolution/hadenlabs/ansible-role-redis.svg
   :target: http://isitmaintained.com/project/hadenlabs/ansible-role-redis
.. |Percentage of issues still open| image:: http://isitmaintained.com/badge/open/hadenlabs/ansible-role-redis.svg
   :target: http://isitmaintained.com/project/hadenlabs/ansible-role-redis
.. |GitHub license| image:: https://img.shields.io/github/license/mashape/apistatus.svg?style=flat-square
   :target: LICENSE

.. Links
.. _`changelog`: CHANGELOG.rst
.. _`contributors`: AUTHORS
.. _`contributing`: CONTRIBUTING.rst

.. _`company`: https://github.com/hadenlabs
.. _`author`: https://github.com/luismayta

.. dependences
.. _Redis: https://redis.io
.. _Python: https://www.python.org
.. _Python 3.6.1: https://www.python.org/downloads/release/python-361
.. _Docker: https://www.docker.com/
.. _Docker Compose: https://docs.docker.com/compose/