# Database

[Back](./..)

- [Set the MySQL Path in Windows](#set-the-mysql-path-path-in-windows-️%EF%B8%8F)
- [Database Import](#database-import-️%EF%B8%8F)
- [Copy Database From One to Another](#copy-database-from-one-to-another-%EF%B8%8F)

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


Thank you for staying with me.  
Please follow and subscribe to my YouTube channel: [YouTube Channel Link](https://www.youtube.com/@MirzaMdGolamNabi)
