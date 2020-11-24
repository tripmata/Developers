# Progress Report
Offical progress report for client services. Created 24/10/2020

## index.php 
We noticed naked queries, unsafe parameters in the sql queries as a result of unsanitized user input. Take for example, an hacker may send this to the server;
```http
{
    "usersess" : "<script>alert('You have been hacked');</script>"
}
```

Looking at the ```User::Initialize``` method, it reads like this;

```php
public function Initialize($arg=null)
{
    if($arg != null)
    {
        $db = DB::GetDB();

        // total unsafe..
        $res = $db->query("SELECT * FROM user WHERE userid='$arg' OR username='$arg'");

        // see what would be sent to the server 
        // SELECT * FROM user WHERE userid='<script>alert('You have been hacked');</script>' OR username='<script>alert('You have been hacked');</script>'

        // This may be an INSERT, UPDATE or DELETE query

        // other code....
    }
}
```

To overcome this, we created two classes that would sanitize and clean all inputs in ```core/validation```.

## core/DB.php
The database file was refactored to use external configuration file. see ```/config.php``` for database connection settings.

Placeholder | Value | Description
------------|-------|------------
host | string | Database connection host
user | string | Authorized user to database
pass | string | Authorized user password to database
name | string | Database name