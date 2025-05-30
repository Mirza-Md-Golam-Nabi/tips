# Database

[Back](./..)

- [Set the MySQL Path in Windows](#set-the-mysql-path-path-in-windows-️)
- [Database Import](#database-import-️)

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


Thank you for staying with me.  
Please follow and subscribe to my YouTube channel: [YouTube Channel Link](https://www.youtube.com/@MirzaMdGolamNabi)
