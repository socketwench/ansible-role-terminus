# Ansible Role: Pantheon Terminus

Installs the Pantheon CLI using the official installer.

## Requirements

* PHP must be already installed on the server and a compatible version. 
* The phar extension must be installed.
* Composer must be installed.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`).

### Installer URL

`pantheon_terminus_installer_url`

The full URL to download the Terminus installer. Default: `https://raw.githubusercontent.com/pantheon-systems/terminus-installer/master/builds/installer.phar`

### Installer options

`pantheon_terminus_install_dir`

Specifies the installation directory for the `terminus` executable. Default: `/usr/local/bin`.

`pantheon_terminus_operation`

The installer operation to perform. Default: `install`

`pantheon_terminus_bin_dir`

The location of the system bin directory. Default: `/usr/local/bin`.

`pantheon_terminus_version`

The version of Terminus to install. Default is empty, instructing the installer to use the latest version.

### PHP Executable

`pantheon_terminus_php_path`

Specifies the path to the PHP executable. Default: `php`

## Dependencies

None, but the following roles are recommended:

* geerlingguy.php
* geerlingguy.composer

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: socketwench.pantheon-terminus }

## License

GPL v3

## Author Information

This role was created by [socketwench](https://deninet.com/).
