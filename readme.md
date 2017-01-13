#NotORM - http://www.notorm.com/

NotORM is a PHP library for simple working with data in the database. The most interesting feature is a very easy work with table relationships. The overall performance is also very important and NotORM can actually run faster than a native driver.

Requirements:
PHP 5.1+
any database supported by PDO (tested with MySQL, SQLite, PostgreSQL, MS SQL, Oracle)

Usage:
```php
<?php
include "NotORM.php";
$connection = new PDO("mysql:dbname=testdb");
$db = new NotORM($connection);


//inserting into table "user"
$user = array(
        'username' => 'testuser',
        'password' => 'hashedpass'
    );
$insertUser = $db->user()->insert(array);//returns true if inserted.

?>
```
