# Documentation
Official documentation for client services

## Project structure
```plain
- controllers/
- core/
    - interfaces/
    - Types/
    - validation/
    ...
- .htaccess
- autoloader.php
- config.php
- error_log
- index.php
```

### core/
This folder contains core files for the program. In it you will find the database class, mail class, sanitize class, validation class, interfaces, and types.

### core/interfaces
This folder contains the following interfaces;

Interface | Methods | Description
----------|---------|------------
IBase | ```ToString(), ToInt(), ToBool()``` | These methods takes no parameter but can return a string, integer and boolean data
IRequest | ```AddParameter(), Execute(), AddRange(), GetURL()``` | This interface allows for client HTTP Request to a remote server.
IResponse | ```GetStatus(), ToBool(), ToInt(), ToString(), GetType()``` | These methods takes no parameter but can return a string, integer and boolean data

### core/Types
This folder contains the date class, boolean class, gender class, privacy class, span class and the user type class. Here is a complete breakdown of what they do.

Class | Description
------|------------
```Gender::class``` | It implements the IBase interface, and it take a gender during creation. 
```Boolean::class``` | It implements the IBase interface with some methods of its own, and it takes an input during creation and converts it to a boolean type if not.
```Privacy::class``` | It implements the IBase interface with some methods of its own, and internally it uses the ```Convert::class```. During creation it takes a long or short privacy text.
```Span::class``` | It's a class designed to return a range between a start and stop position. During creation it takes two parameters. start (int) and stop (int)
```WixDate::class``` | It implements the IBase interface with some methods of its own, and it takes a date string during creation.

### core/validation
This folder contains the sanitize class and validate class. Here is a complete breakdown of what they do.

Class | Description
------|------------
```Sanitize::class``` | It's a simple class that keeps all inputs sanitized and clean.
```Validate::class``` | It's a simple class that keeps all inputs validated.


### config.php
```config.php``` was created for global configuration. It has a constant MODE that could either be set to ```development``` or ```live```. Here are some of the methods available;
1. ```Configuration::database()```

This method would return the default database connection setting as an object. Can be toggled with the MODE constant. See array structure below;

Placeholder | Value | Description
------------|-------|------------
host | string | Database connection host
user | string | Authorized user to database
pass | string | Authorized user password to database
name | string | Database name 


### Help us make this doc great!

See something that's wrong or unclear? Submit a pull request.

Thanks.
