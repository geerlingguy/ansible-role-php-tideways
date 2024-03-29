# DEPRECATED Ansible Role: PHP-Tideways

> **DEPRECATED**: This Ansible role is no longer maintained and has been deprecated.

[![CI](https://github.com/geerlingguy/ansible-role-php-tideways/workflows/CI/badge.svg?event=push)](https://github.com/geerlingguy/ansible-role-php-tideways/actions?query=workflow%3ACI)

Installs the [Tideways PHP Profile Extension](https://github.com/tideways/php-xhprof-extension) on Linux servers.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    workspace: /root

Where Tideways setup files will be downloaded and built.

    tideways_download_url: https://github.com/tideways/php-xhprof-extension/archive/master.zip
    tideways_download_folder_name: php-xhprof-extension-master

The URL from which Tideways will be downloaded, and the resulting folder into which it is downloaded.

    tideways_extension_name: tideways_xhprof.so

The extension name for the Tideways PHP extension.

    tideways_api_key: ''

If you use the Tideways UI, set this variable to your API key. Otherwise the extension can be used along with the XHProf UI to view profiles.

    tideways_install_xhprof_ui: true

Tideways data-format is 100% compatible with XHProf so you can use the XHProf UI to browse profiles reports and the `XHProfRuns_Default` class to write the profile data to disk. If you use the Tideways UI, set this variable to `no`.

    xhprof_download_url: https://github.com/phacility/xhprof/archive/master.tar.gz
    xhprof_download_folder_name: xhprof-master

The URL from which XHProf will be downloaded.

    php_xhprof_lib_dir: /usr/share/php/xhprof_lib

Directory where the XHProf PHP library is stored.

    php_xhprof_html_dir: /usr/share/php/xhprof_html

Directory where the XHProf UI is stored.

## Dependencies

  - geerlingguy.php

## Example Playbook

    - hosts: webservers
      roles:
        - geerlingguy.php-tideways

## License

MIT / BSD

## Author Information

This role was created in 2017 by [Jeff Geerling](https://www.jeffgeerling.com/), author of [Ansible for DevOps](https://www.ansiblefordevops.com/).
