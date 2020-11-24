# Documentation
Official documentation for the front desk area

## Project structure
```plain
- core/
    - classes/
    - interfaces/
    - phpmailer/
    - autoloader.php
- .htaccess
- config.php
- index.php
- key.json
```

### core/
This folder contains core files for the program. In it you will find the request class, mail class, router class, upload class, interfaces, and phpmailer.

### core/classes
This folder contains the core classes needed to comminucate with the front desk service. See a complete list of classes in this directory.

Class | Description
------|------------
```Mail::class``` | Responsible for sending mails out
```NameValuePair::class``` | Setter and Getter for ```Name``` and ```Value```
```Request::class``` | Responsible for HTTP Client requests
```Response::class``` | Responsible for handling HTTP Client request response
```Router::class``` | Responsible for managing route requests
```Serializer::class``` | Responsible for data serialization
```Upload::class``` | Responsible for File uploads

### core/interfaces
This folder contains the following interfaces;

Interface | Methods | Description
----------|---------|------------
IBase | ```ToString(), ToInt(), ToBool()``` | These methods takes no parameter but can return a string, integer and boolean data
IRequest | ```AddParameter(), Execute(), AddRange(), GetURL()``` | This interface allows for client HTTP Request to a remote server.
IResponse | ```GetStatus(), ToBool(), ToInt(), ToString(), GetType()``` | These methods takes no parameter but can return a string, integer and boolean data

### core/phpmailer
This folder contains a PHP Library for sending secure emails. It's abstracted by the ```Mail::class``` with additional methods for flexibility. 

### autoloader.php
This file includes all the required PHP files for our application.

### config.php
```config.php``` was created for global configuration. It has a constant ```MODE``` that could either be set to ```development``` or ```live```. Here are some of the methods available;

1. ```Configuration::url()```

This method would return the default URL configuration for worker, page, storage and the host url. 

Placeholder | Value | Description
------------|-------|------------
worker | string | Worker service endpoint.
page | string | Page service endpoint.
storage | string | Local and cloud storage url.
host | string | Base endpoint for front desk area.

### index.php
This file is responsible for autoloading app classes, interfaces and global configuration. It's actively involved in requesting for pages, submitting data to the front desk service ```worker``` and ```page``` handlers.

### Help us make this doc great!

See something that's wrong or unclear? Submit a pull request.

Thanks.
