# Documentation
Official documentation for messaging

## Project structure
```plain
- core/
    - classes/
    - interfaces/
    - phpmailer/
    - autoloader.php
- .htaccess
- index.php
- key.json
```

### core/
This folder contains core files for the program. In it you will find the request class, mail class, router class, upload class, and interfaces, and phpmailer.

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
This folder contains a PHP Library for sending secure emails. It's abstracted by the ```Mail::class``` with additional methods for flexibility. Please visit ```core/classes/Mail.php``` for SMTP connection configuration.

### autoloader.php
This file includes all the required PHP files for our application.


### index.php
This file is responsible for autoloading app classes, interfaces and global configuration. It's actively involved in sending out mails and sms.

### Help us make this doc great!

See something that's wrong or unclear? Submit a pull request.

Thanks.
