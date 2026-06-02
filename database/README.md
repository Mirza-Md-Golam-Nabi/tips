# Database

[Back](./..)

- [Set the MySQL Path in Windows](#set-the-mysql-path-path-in-windows-%EF%B8%8F)
- [Database Import](#database-import-%EF%B8%8F)
- [Copy Database From One to Another](#copy-database-from-one-to-another-%EF%B8%8F)
- [Enable phpMyAdmin Configuration Storage in Laragon](#enable-phpMyAdmin-configuration-storage-in-laragon-%EF%B8%8F)

## Set the MySQL Path (PATH) in Windows ([⬆️](#database))
Please, visit this [Link](./../laravel/installation/phpMyAdmin/README.md#set-the-mysql-path-path-in-windows-️)

## Database Import ([⬆️](#database))
If you want to import a database file using the terminal, make sure your database file is in **.sql** format. Then, run the following command:
```sh
mysql -u [username] -p [database_name] < [path/to/file.sql]
```

**After running the command, enter your MySQL password when prompted.**

**Example:**
* username = root
* database_name = laravel
* path/to/file.sql = "C:\Users\Nabi\Downloads\laravel.sql"

```sh
mysql -u root -p laravel < "C:\Users\Nabi\Downloads\laravel.sql"
```

## Copy Database from One to Another ([⬆️](#database))

If you want to copy data from one database to another, you can use the following command.

```sh
mysqldump -u [from_username] -p[FromPassword] [from_database_name] | mysql -u [to_username] -p[ToPassword] [to_database_name]
```

**N.B.** Follow the **Password** option. There is no space between **-p** and **Password**.

**Example:**
* from_username = mirza
* FromPassword = 12345
* from_database_name = production
* to_username = nabi
* ToPassword = 98765
* to_database_name = dev

```sh
mysqldump -u mirza -p12345 production | mysql -u nabi -p98765 dev
```

## Enable phpMyAdmin Configuration Storage in Laragon ([⬆️](#database))

### Problem:

- Internal Relations tab was not showing in phpMyAdmin Relation view
- Display Column option was not available

### Steps to fix:

- Open ***config.inc.php*** file from **D:\laragon\etc\apps\phpmyadmin\**
- Uncomment all lines in the **"phpMyAdmin configuration storage settings"** section (remove // from the beginning of each line)
- Create **phpmyadmin** database in phpMyAdmin SQL tab:

```sql
CREATE DATABASE IF NOT EXISTS `phpmyadmin` DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_bin;
```
- Select phpmyadmin database and run the following SQL to create required tables:

```sql
CREATE TABLE IF NOT EXISTS `pma__relation` (
  `master_db` varchar(64) NOT NULL DEFAULT '',
  `master_table` varchar(64) NOT NULL DEFAULT '',
  `master_field` varchar(64) NOT NULL DEFAULT '',
  `foreign_db` varchar(64) NOT NULL DEFAULT '',
  `foreign_table` varchar(64) NOT NULL DEFAULT '',
  `foreign_field` varchar(64) NOT NULL DEFAULT '',
  PRIMARY KEY (`master_db`,`master_table`,`master_field`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_bin;

CREATE TABLE IF NOT EXISTS `pma__column_info` (
  `id` int(5) unsigned NOT NULL AUTO_INCREMENT,
  `db_name` varchar(64) NOT NULL DEFAULT '',
  `table_name` varchar(64) NOT NULL DEFAULT '',
  `column_name` varchar(64) NOT NULL DEFAULT '',
  `comment` varchar(255) NOT NULL DEFAULT '',
  `mimetype` varchar(255) NOT NULL DEFAULT '',
  `transformation` varchar(255) NOT NULL DEFAULT '',
  `transformation_options` varchar(255) NOT NULL DEFAULT '',
  `input_transformation` varchar(255) NOT NULL DEFAULT '',
  `input_transformation_options` varchar(255) NOT NULL DEFAULT '',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_bin;

CREATE TABLE IF NOT EXISTS `pma__table_info` (
  `db_name` varchar(64) NOT NULL DEFAULT '',
  `table_name` varchar(64) NOT NULL DEFAULT '',
  `display_field` varchar(64) NOT NULL DEFAULT '',
  PRIMARY KEY (`db_name`,`table_name`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_bin;
```

- Restart Apache from Laragon

### Result:

- Internal Relations tab now visible in Relation view
- Display Column can now be set for foreign key fields


Thank you for staying with me.  
Please follow and subscribe to my YouTube channel: [YouTube Channel Link](https://www.youtube.com/@MirzaMdGolamNabi)
