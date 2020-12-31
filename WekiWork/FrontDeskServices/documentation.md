# Documentation
Official documentation for the front desk services

## Project structure
```plain
- core/
    - interfaces/
    - Types/
    - validation/
- manifest/
- pages/
- config.php
- loader.php
- page.php
- worker.php
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


2. ```Configuration::url()```

This method would return the default URL configuration for storage and the host url. You can also add and send the url settings in your HTTP request header as demostrated below.

```json
"x-url-config" : {
    "host" : "http://example.com/",
    "storage" : "http://static.example.com/",
    "messaging" : "http://messaging.example.com/",
}
```

### other files
Amongst other files, in the ```core/``` root directory is the ```DB::class```. You can alter the database configuration in the ```/config.php``` file. The rest of the files here are tightly couped together. Please refer to ```/worker.php``` and ```/page.php``` for trace of usage.


### loader.php
This file is responsible for autoloading app classes, interfaces and global configuration. It also provides a global variable ```$urlConfiguration``` that can be used directly in the ```worker.php``` and ```page.php``` file.

### page.php
This file takes a session value from ```GET``` or ```POST``` request method (prefarrably ```POST```) and would return the frontdesk dashboard if the user is authenticated or login page if not.

```http
POST https://example.com/page.php
usersess = 'ahsnbsgsyejssnsgsbsgstnaklsus'
```

### worker.php
This file is the base controller and it listens for a job to perform. And some jobs are unavailable publicly unless authenticated. Here is how a request is understood;

```http
POST https://example.com/worker.php
job = '<see jobs below>'
```

List of avaliable jobs.
Job | Description | Authenticate
----|-------------|-------------
```login``` | Authenticate a user | no
```frontdesk operation``` | Get front desk operations | yes
```process coupon``` | Process coupon codes | yes
```get pos items``` | Get point of sale items | yes
```get pos receipt``` | Get point of sale receipt | yes
```get pos discount``` | Get point of sale discounts | yes
```get customers``` | Get list of customers  | yes
```get guest info``` | Get a guest information | yes
```get inhouse``` | Get lodging information | yes
```add customer id``` | Add customer ID | yes
```get reservations``` | Get list of reservations | yes
```get pos settings``` | Get point of sale settings | yes

### Help us make this doc great!

See something that's wrong or unclear? Submit a pull request.

Thanks.
