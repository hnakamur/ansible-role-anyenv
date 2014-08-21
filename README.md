anyenv
======

An Ansible role to install anyenv

Requirements
------------

For the initial setup, you need to run this role with tag anyenv_initial_setup.
The script to initialize anyenv will be added to "{{ anyenv_shell_rc_file }}"

```
ansible-playbook your_playbook.yml --tag anyenv_initial_setup
```

Then exec your shell to initialize anyenv.

```
exec $SHELL -l
```

After that, you can run this role normally.

```
ansible-playbook your_playbook.yml
```

Role Variables
--------------

- anyenv_git_url: https://github.com/riywo/anyenv
    - The url of the anyenv git repository.
- anyenv_install_dir: ~/.anyenv
    - The install directory.
- anyenv_shell_rc_file: ~/.zshrc
    - The shell config file to add anyenv initialization.
- anyenv_rbenv_version: 2.1.2
    - The rbenv version to install. Does not install when empty.
- anyenv_ndenv_version: v0.10.30
    - The ndenv version to install. Does not install when empty.

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
