# Progress Report
Offical progress report for the front desk services. Created 22/10/2020

## loader.php
We noticed that the ```loader.php``` file had lots of files required even when it's not needed, so we had to replace this proceedure with an autoloader.

Previous code.
```php
// Require Interfaces
require_once ("core/interfaces/IBase.php");
require_once ("core/interfaces/IRequest.php");
require_once ("core/interfaces/IResponse.php");

// Require Types
require_once ("core/Types/Privacy.php");
require_once ("core/Types/Boolean.php");
require_once ("core/Types/Gender.php");
require_once ("core/Types/WixDate.php");
require_once ("core/Types/UserType.php");
require_once ("core/Types/Span.php");

require_once ("core/User.php");
require_once ("core/Convert.php");
require_once ("core/DataPack.php");
require_once ("core/Menu.php");
require_once ("core/Menues.php");
require_once ("core/Stringer.php");
require_once ("core/Router.php");
require_once ("core/Random.php");
require_once ("core/Role.php");
require_once ("core/Access.php");
require_once ("core/Customer.php");
require_once ("core/Newsletter.php");
require_once ("core/Department.php");
require_once ("core/Shift.php");
require_once ("core/Staff.php");
require_once ("core/Country.php");
require_once ("core/Currency.php");
require_once ("core/Printer.php");
require_once ("core/States.php");
require_once ("core/City.php");
require_once ("core/File.php");
require_once ("core/Upload.php");
require_once ("core/Banner.php");
require_once ("core/Faqcategory.php");
require_once ("core/Faq.php");
require_once ("core/Gallery.php");
require_once ("core/Roomcategory.php");
require_once ("core/Room.php");
require_once ("core/Team.php");
require_once ("core/Modules.php");
require_once ("core/Integration.php");
require_once ("core/Paygateway.php");
require_once ("core/Coupon.php");
require_once ("core/Extraservice.php");
require_once ("core/Testimonial.php");
require_once ("core/Facilities.php");
require_once ("core/Services.php");
require_once ("core/Messagetemplate.php");
require_once ("core/Message.php");
require_once ("core/Contact.php");
require_once ("core/Contactcollection.php");
require_once ("core/Contactcollectionitem.php");
require_once ("core/Review.php");
require_once ("core/Reviewitem.php");
require_once ("core/Reviewresponse.php");
require_once ("core/Reviewsession.php");
require_once ("core/Seo.php");
require_once ("core/Discount.php");
require_once ("core/Timespan.php");
require_once ("core/Eventlistener.php");
require_once ("core/Event.php");
require_once ("core/Messageschedule.php");
require_once ("core/Schedule.php");
require_once ("core/Guest.php");
require_once ("core/Subguest.php");
require_once ("core/Supplier.php");
require_once ("core/Request.php");
require_once ("core/Response.php");
require_once ("core/NameValuePair.php");
require_once ("core/Mail.php");
require_once ("core/Context.php");
require_once ("core/Sms.php");
require_once ("core/Lodgepixel.php");
require_once ("core/Receipt.php");
require_once ("core/Order.php");
require_once ("core/Entity.php");
require_once ("core/Cart.php");
require_once ("core/Drinkorder.php");
require_once ("core/Foodorder.php");
require_once ("core/Invoice.php");
require_once ("core/Items.php");
require_once ("core/Laundryorder.php");
require_once ("core/Orderlist.php");
require_once ("core/Pastryorder.php");
require_once ("core/Poolorder.php");
require_once ("core/Roomorder.php");
require_once ("core/Guest.php");
require_once ("core/Food.php");
require_once ("core/Foodcategory.php");
require_once ("core/Drink.php");
require_once ("core/Drinkcategory.php");
require_once ("core/Pastry.php");
require_once ("core/Pastrycategory.php");
require_once ("core/Laundry.php");
require_once ("core/Pool.php");
require_once ("core/Baritem.php");
require_once ("core/Kitchenitem.php");
require_once ("core/Poolitem.php");
require_once ("core/Laundryitem.php");
require_once ("core/Pastryitem.php");
require_once ("core/Storeitem.php");
require_once ("core/Roomitem.php");

// Require Inventory activities
require_once ("core/Barinventoryactivity.php");
require_once ("core/Kitcheninventoryactivity.php");
require_once ("core/Poolinventoryactivity.php");
require_once ("core/Laundryinventoryactivity.php");
require_once ("core/Pastryinventoryactivity.php");
require_once ("core/Storeinventoryactivity.php");
require_once ("core/Roominventoryactivity.php");
require_once ("core/Inventoryactivity.php");

// Require Files for Quotations
require_once ("core/Barquotation.php");
require_once ("core/Kitchenquotation.php");
require_once ("core/Poolquotation.php");
require_once ("core/Laundryquotation.php");
require_once ("core/Pastryquotation.php");
require_once ("core/Storequotation.php");
require_once ("core/Roomquotation.php");
require_once ("core/Quotationitem.php");
require_once ("core/QuotationPixel.php");

// Require Files for Auditing
require_once ("core/Baraudit.php");
require_once ("core/Kitchenaudit.php");
require_once ("core/Poolaudit.php");
require_once ("core/Laundryaudit.php");
require_once ("core/Pastryaudit.php");
require_once ("core/Storeaudit.php");
require_once ("core/Roomaudit.php");
require_once ("core/Audititem.php");

require_once ("core/Barpr.php");
require_once ("core/Kitchenpr.php");
require_once ("core/Poolpr.php");
require_once ("core/Laundrypr.php");
require_once ("core/Pastrypr.php");
require_once ("core/Storepr.php");
require_once ("core/Roompr.php");
require_once ("core/Purchaserequestitem.php");

// Require Files for settings
require_once ("core/Barsettings.php");
require_once ("core/Kitchensettings.php");
require_once ("core/Laundrysettings.php");
require_once ("core/Pastrysettings.php");
require_once ("core/Poolsettings.php");
require_once ("core/Roomsettings.php");
require_once ("core/Messagesettings.php");

// Other files
require_once ("core/Quotationsession.php");
require_once ("core/Task.php");
require_once ("core/Sendmessage_task.php");
require_once ("core/Schedule.php");

// Require Files for logging
require_once ("core/Systemlog.php");
require_once ("core/Fraudlog.php");

// Require files for history
require_once ("core/Couponhistory.php");
require_once ("core/Discounthistory.php");

// Require files for reservation
require_once ("core/Reservation.php");
require_once ("core/Foodreservation.php");
require_once ("core/Drinkreservation.php");
require_once ("core/Pastryreservation.php");
require_once ("core/Roomreservation.php");

// Require files for orders
require_once ("core/Barorder.php");
require_once ("core/Kitchenorder.php");
require_once ("core/Bakeryorder.php");

// Require files for pixel
require_once ("core/Foodpixel.php");
require_once ("core/Drinkpixel.php");
require_once ("core/Pastrypixel.php");

// Require files for sales
require_once ("core/Bakerysale.php");
require_once ("core/Barsale.php");
require_once ("core/Kitchensale.php");
require_once ("core/Poolsale.php");
require_once ("core/Laundrysale.php");

// Require files for sales items
require_once ("core/Bakerysaleitem.php");
require_once ("core/Barsaleitem.php");
require_once ("core/Kitchensaleitem.php");
require_once ("core/Poolsaleitem.php");
require_once ("core/Laundrysaleitem.php");

// Require files for transaction
require_once ("core/Bakerytransaction.php");
require_once ("core/Bartransaction.php");
require_once ("core/Kitchentransaction.php");
require_once ("core/Laundrytransaction.php");
require_once ("core/Pooltransaction.php");

// Other files
require_once ("core/Pastrypo.php");
require_once ("core/Barpo.php");
require_once ("core/Kitchenpo.php");
require_once ("core/Laundrypo.php");
require_once ("core/Poolpo.php");
require_once ("core/Storepo.php");
require_once ("core/Roompo.php");

// Lodging files
require_once ("core/Lodging.php");
require_once ("core/Lodginghistory.php");
require_once ("core/Lodgingitem.php");
require_once ("core/Lodgingtransaction.php");
require_once ("core/Purchaseorderitem.php");

// Payment and credit files
require_once ("core/Suppliercredit.php");
require_once ("core/Itempixel.php");
require_once ("core/Payment.php");

// Other files
require_once ("core/Subscriber.php");
require_once ("core/Site.php");
require_once ("core/Property.php");
require_once ("core/DB.php");
```

It's like requesting for 50 files each time a request it made to this server, even when it's just 1 or 2 needed to complete an operation.

So we made it more elegant with few lines of codes.
```php 
spl_autoload_register(function(string $classOrInterface){

    // @var array $directories
    $directories = [
        'core/interfaces/', // base interface directory
        'core/Types/', // base directory for types
        'core/validation/', // base directory for validation
        'core/' // base core directory
    ];

    // now we ilterate through the list of directories
    foreach ($directories as $directory) :

        // create file path
        $filePath = $directory . $classOrInterface . '.php';

        // check if file exists
        if (file_exists($filePath)) :

            // require file
            require_once ($filePath);

            // break out of loop
            break;

        endif;

    endforeach;

    // clean up
    $directory = $directories = $filePath = null;
});
```

## page.php 
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

## scripts
Added ```storage``` and ```host``` address globally for all javascript files.