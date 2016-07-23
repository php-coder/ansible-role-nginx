Ansible role for Nginx installation
===================================

Installs nginx from official repository at http://nginx.org (http://nginx.org/en/linux_packages.html#stable).

Role Variables
--------------

* `remove_default_vhost`

  Whether to remove default virtual host. Default is `no`.

* `state`

  State of the service after installation. Possible values: `started`, `stopped`, `restarted`,
  `reloaded`. Default is `started`.

Actions role
------------

* imports GPG key for APT
* adds repo
* updates `apt`s cache
* installs package
* removes default virtual host (only when `remove_default_vhost` is set to `yes`)
* runs nginx (default behavior that can be changed by `state` parameter)
* adds nginx to start on boot

How to install
--------------

    ansible-galaxy install php-coder.nginx

For more installation's options/variants read the documentation: http://docs.ansible.com/galaxy.html

Example Playbook
----------------

Example of usage with default parameters:

    - hosts: all
      roles:
         - php-coder.nginx

License
-------

GPLv2

Author Information
------------------

Slava Semushin (slava.semushin@gmail.com)
