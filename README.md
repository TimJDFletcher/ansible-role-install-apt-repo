install-apt-repo
=========

Role to install apt repos

Requirements
------------

Role is currently targetted at Debian / Ubuntu but could be extended to RH/CentOS.

Role Variables
--------------

Call the role with the single variable `repository` for the repo to install.

The repo contains a set of pre-defined repos in defaults/main.yml in the hash 'configured_apt_repositories', to add to this list please open a PR.

Dependencies
------------

None

Example Playbook
----------------

Example to enable the Debian backports repo

    - hosts: servers
      roles:
         - { role: install-apt-repo, repository: backports }

Improvements
-------

The default list should be defined with a _var name and then merged with the main var name to allow for repos to be defined in a play.

License
-------

BSD

Author Information
------------------

Supported by I/O team, contact @timf on Slack
