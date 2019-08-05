# Ansible Role - Install and configure otrs

## Variables

* install_mode: Choose between prepare, configure or install (default: "configure")
* vhost_domain: The domain in the apache configuration (required)
* otrs_login_password: initial password for root@localhost (required)
* vhost_user: User under which the vhost will run (default: otrs)
* otrs_database: Name of the database used (default: otrs)
* otrs_database_user: Name of the databaseuser (default: otrs)
* otrs_install_path: Directory where otrs will be installed (default: /opt/otrs)
* otrs_user: Name of the otrs linux user (default: otrs)
* otrs_group: Name of the group the webserver runs and the otrs_user is in (default: www-data)
* otrs_tar_file: Local path to the otrs installation file (default: otrs.tar.bz2)
* otrs_proxy: Configure otrs to use a proxy (only during the first run) (default: None)
* otrs_timezone: Configure the default timezone in otrs (only during the first run) (default: Europe/Berlin)

## Required files

If you want to install otrs with this role you have to put the current otrs installation tar to your local directory. The default path is
```bash
$PWD/otrs.tar.bz2
```

but this can be changed with the variable otrs_tar_file.

## install_mode

### prepare
* Install dependencies
* Create users, database, directory structure

### configure
* otrs daemon
* Permissions

### install
* Installs OTRS from the installation archive
