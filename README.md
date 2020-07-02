# WeBid
The official WeBid github fork

Please post bugs at http://bugs.webidsupport.com/

Todo list: https://github.com/renlok/WeBid/wiki/To-DO

## Installation
### Permissions
```
git clone https://github.com/crazafimahatratra/WeBid.git
cd WeBid
sudo chown www cache/
sudo chown www uploaded/
sudo chown www uploaded/cache/
sudo chown www includes/config.inc.php.new
sudo chown www language/EN/categories.inc.php 
sudo chown www language/EN/categories_select_box.inc.php 
```

### Database
```
mysql -u root -p
mysql> create database wbd;
mysql> create user wbd identified with mysql_native_password by 'wbd';
mysql> grant all privileges on wbd.* to wbd;
```

### Config
```
vim includes/config.inc.php
```

```php
<?php
$DbHost  = "localhost";
$DbDatabase = "wbd";
$DbUser  = "wbd";
$DbPassword = "wbd";
$DBPrefix       = "webid_";
$main_path = "/usr/local/var/www/webid/";
$MD5_PREFIX = "XXXXXXXX"; // <-- replace with value displayed on installation page
?>
```

### Remove install folder
```
rm -rf install/