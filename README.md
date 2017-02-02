# Ansible Role - Install and configure otrs

#### Variables

* vhost_user: User under which the vhost will run (default: otrs)
* otrs_database: Name of the database used (default: otrs)
* otrs_database_user: Name of the databaseuser (default: otrs)
* otrs_install_path: Directory where otrs will be installed (default: /opt/otrs)
* otrs_user: Name of the otrs linux user (default: otrs)
* otrs_group: Name of the group the webserver runs and the otrs_user is in (default: www-data)
* otrs_tar_file: Local path to the otrs installation file (default: otrs.tar.bz2)

#### Required files

If you want to install otrs with this role you have to put the current otrs installation tar to your local directory. The default path is
```bash
$PWD/otrs.tar.bz2
```
but this may be changed with the variable otrs_tar_file.
