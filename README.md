Ansible role for Nginx installation
===================================

Installs nginx from official repository at http://nginx.org (http://nginx.org/en/linux_packages.html#stable).

Actions role
------------

* imports GPG key for APT
* adds repo
* updates `apt`s cache
* installs package
* runs nginx
* adds nginx to start on boot

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
