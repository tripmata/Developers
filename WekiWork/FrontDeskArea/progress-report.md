# Progress Report
Offical progress report for the front desk area. Created 23/10/2020

## core/Request.php
Added storage and host url to the request header for the front desk service. See [https://github.com/tripmata/Developers/blob/master/WekiWork/FrontDeskServices/documentation.md#configphp] for more information.
```php
// Request::Execute()

// get url
$urlConfiguration = Configuration::url();

// add storage and host
curl_setopt($curl, CURLOPT_HTTPHEADER, [
    'x-url-config:' . json_encode([
        'storage' => $urlConfiguration->storage,
        'host'    => $urlConfiguration->host
    ])
]);
```

## config.php 
```config.php``` was created for global configuration. It has a constant MODE that could either be set to development or live. Here are some of the methods available;

1. ```Configuration::url()```

This method would return the default URL configuration for worker, page, storage and the host url. 

Placeholder | Value | Description
------------|-------|------------
worker | string | Worker service endpoint.
page | string | Page service endpoint.
storage | string | Local and cloud storage url.
host | string | Base endpoint for front desk area.

## styling
Updated ```checked out, paid, unpaid, pending, no show``` status styles. Also updated the background color for action buttons

## scripts
Fixed some javascripts errors, updated ```frondesk1.js``` and ```outlets.js``` with global paths for CDN and HOST address.

## images
Added a default image for Customers, and Profile page.