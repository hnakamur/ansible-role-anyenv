anyenv
======

An Ansible role to install anyenv

Requirements
------------

None.

Role Variables
--------------

- anyenv_git_url: https://github.com/riywo/anyenv
    - The url of the anyenv git repository.
- anyenv_install_dir: ~/.anyenv
    - The install directory.
- anyenv_shell_rc_file: ~/.zshrc
    - The shell config file to add anyenv initialization.

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: hnakamur.anyenv, anyenv_shell_rc_file: ~/.bashrc }

License
-------

MIT

Author Information
------------------

[Hiroaki Nakamura]( http://hnakamur.github.io/ )
