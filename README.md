README FIRST!!
--------------
Go to your application folder then clone this repo:
```
> git clone https://github.com/rezzafr33/bitnami_conf.git conf
> cd conf && rm -rf .git
```

- Replace INSTALL_DIR with your bitnami/xampp install path, e.g: /opt/lampp
- Replace APP_FOLDER with your apps folder
- for httpd-vhosts.conf &  php-fpm/pool.php replace DOMAIN with your domain name, by default domain suffix is ".dev"
- for php-fpm/pool.php change user and group to your user and group

For Bitnami:
------------
Edit INSTALL_DIR/apache2/conf/bitnami/bitnami-apps-vhosts.conf
Remove or comment out all include line then add this line:

`IncludeOptional "INSTALL_DIR/apps/*/conf/httpd-vhosts.con[f]"`

Edit INSTALL_DIR/apache2/conf/bitnami/bitnami-apps-prefix.conf
Remove or comment out all include line then add this line:

`IncludeOptional "INSTALL_DIR/apps/*/conf/httpd-prefix.con[f]"`

For Xampp:
----------
Dont forget to edit INSTALL_DIR/apache2/conf/bitnami/httpd.conf
Remove or comment out all include line then add this line:
```
IncludeOptional "INSTALL_DIR/apps/*/conf/httpd-prefix.con[f]"
IncludeOptional "INSTALL_DIR/apps/*/conf/httpd-vhosts.con[f]"
```
