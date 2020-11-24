# Controllers 
Documentation of all the avaliable controllers for public consumption. All responses are formatted in ```JSON```


## POST /adddrinkreservation
Make reservation for drinks from the property kitchen. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```drink``` | string | Name of the drink
```custsess``` | string | Loggedin customer session token
```quantity``` | int | Drink quantity
```date``` | string | Order date
```mins``` | int | Minute of the day
```hour``` | int | Hour of the day
```gmt``` | string | GMT for date


## POST /addfoodreservation
Make reservation for food from the property kitchen. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```food``` | string | Name of the food
```custsess``` | string | Loggedin customer session token
```quantity``` | int | Drink quantity
```date``` | string | Order date
```mins``` | int | Minute of the day
```hour``` | int | Hour of the day
```gmt``` | string | GMT for date


## POST /addpastryreservation
Make reservation for pastry from the property kitchen. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```pastry``` | string | Pastry name
```custsess``` | string | Loggedin customer session token
```quantity``` | int | Drink quantity
```date``` | string | Order date
```mins``` | int | Minute of the day
```hour``` | int | Hour of the day
```gmt``` | string | GMT for date


## POST /addpayment
Record Card, Cash payment information. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```item_type``` | string | Souce of payment (kitchen, bar, pastry etc.)
```usersess``` | string | Loggedin customer session token
```transaction``` | string | Transaction token
```amount``` | float | Total amount paid
```method``` | string | Method of payment (Card, Cash)


## POST /addpospayment
Record POS payment information. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```item_type``` | string | Souce of payment (kitchen, bar, pastry etc.)
```usersess``` | string | Loggedin customer session token
```transaction``` | string | Transaction token
```amount``` | float | Total amount paid
```method``` | string | Method of payment (POS)


## POST /addposrefund
Record POS refunds. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```item_type``` | string | Souce of payment (kitchen, bar, pastry etc.)
```usersess``` | string | Loggedin customer session token
```transaction``` | string | Transaction token
```amount``` | float | Total amount paid
```method``` | string | Method of payment (POS)
```note``` | string | Reason for refunds


## POST /addrefund
Record Card, Cash refunds. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```item_type``` | string | Souce of payment (kitchen, bar, pastry etc.)
```usersess``` | string | Loggedin customer session token
```transaction``` | string | Transaction token
```amount``` | float | Total amount paid
```method``` | string | Method of payment (Card, Cash)
```note``` | string | Reason for refunds


## POST /addroom
Add room reservation for a guest. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```room``` | string | Room name
```checkin``` | string | Check in date
```checkout``` | string | Check out date
```guestcount``` | int | Total number of guests to occupy room


## POST /adminlogin
Authenticate administrator. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```user``` | string | Account username
```password``` | string | Account password
```platform``` | string | Platform to process for. (Web or Mobile)


## POST /adminuser
Get user account information. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```token``` | string | Loggedin customer session token


## POST /applycoupon
Apply coupon for reservation. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```code``` | string | Coupon code


## POST /cancelorder
Cancel self service order. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```item_type``` | string | Souce of payment (kitchen, bar, pastry etc.)
```order``` | string | Order id


## POST /cancelreservation
Cancel reservation. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```custsess``` | string | Loggedin customer session token
```reservation``` | int | Reservation ID 


## POST /changedriverstatus
Change driver status. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Driverid``` | int | Driver ID
```status``` | string | Driver status (Availiable, Busy, etc.)


## POST /changeeventstatus
Change event status. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```id``` | int | Event ID
```status``` | int | Event status (1 or 0)


## POST /changelaundrystatus
Change laundry status. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```id``` | int | Laundry ID
```status``` | int | Laundry status (1 or 0)


## POST /changelaundrystatus
Change laundry status. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```id``` | int | Laundry ID
```status``` | int | Laundry status (1 or 0)


## POST /changemessagestatus
Change message status. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Messageid``` | int | Message ID
```status``` | int | Message status (1 or 0)


## POST /changepartnerstatus
Change driver status. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Driverid``` | int | Driver ID
```status``` | string | Driver status (Availiable, Busy, etc.)


## POST /changepoolstatus
Change pool session status. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```id``` | int | Pool session ID
```status``` | string | Pool status (1 or 0)


## POST /changepropertystatus
Change property status. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Propertyid``` | int | Property ID
```status``` | string | Property status (1 or 0)


## POST /changevehiclestatus
Change vehicle status. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Vehicleid``` | int | Vehicle ID
```status``` | string | Vehicle status (1 or 0)


## POST /confirmpaystackpay
Confirm paystack payment. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```reference``` | string | Payment reference


## POST /createaccount
Create customer account. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```args``` | string | Request arguments
```email``` | string | Valid email address
```phone``` | string | Valid phone number
```names``` | string | First and Last name
```password``` | string | Account password


## POST /deleteadminuser
Delete admin user account. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Userid``` | string | Valid user ID


## POST /deletebanner
Delete banner. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Bannerid``` | string | Valid banner ID


## POST /deletecontact
Delete contact information. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Contactid``` | string | Valid contact ID


## POST /deletecontactfromlist
Delete contact information from a list. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```data``` | string | Valid contact list seperated by comma (,)


## POST /deletecoupon
Delete coupon code for a property. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Couponid``` | string | Valid coupon ID
```property``` | string | Valid property name or ID


## POST /deletecustomcontactlist
Delete custom contact list. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Contactcollectionid``` | int | Valid contact collection list ID


## POST /deletecustomer
Delete customer from a property. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Customerid``` | string | Valid customer ID
```property``` | string | Valid property name or ID


## POST /deletedepartment
Delete a department. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Departmentid``` | int | Valid department ID


## POST /deletediscount
Delete discount. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Discountid``` | int | Valid discount ID


## POST /deletedrink
Delete a drink. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Drinkid``` | int | Valid drink ID


## POST /deletedrinkcategory
Delete a drink category. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Drinkcategoryid``` | int | Valid drink category ID


## POST /deletedriver
Delete a driver. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Driverid``` | int | Valid driver ID


## POST /deleteevent
Delete event. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Eventlistenerid``` | int | Valid event listener ID


## POST /deleteextraservice
Delete extra service. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Extraserviceid``` | int | Valid extra service ID


## POST /deletefacilityitem
Delete facility item. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```facilityId``` | int | Valid facility ID


## POST /deletefaq
Delete a section from a list of frequently asked questions. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Faqid``` | int | Valid faq ID


## POST /deletefaqcategory
Delete frequently asked questions category. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Faqcategoryid``` | int | Valid faq category ID


## POST /deletefood
Delete food. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Foodid``` | int | Valid food ID


## POST /deletefoodcategory
Delete a food category. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Foodcategoryid``` | int | Valid food category ID


## POST /deletefundingrequest
Delete funding request. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```request``` | int | Funding request


## POST /deletegalleryitem
Delete gallery item. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```galleryId``` | int | Valid gallery id


## POST /deleteinventoryaudit
Delete inventory audit. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```item_type``` | string | Souce of inventory (kitchen, bar, pastry etc.)
```auditid``` | int | Valid Audit ID


## POST /deleteinventoryitem
Delete inventory item. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```item_type``` | string | Souce of inventory (kitchen, bar, pastry etc.)
```itemid``` | int | Valid Item ID


## POST /deleteinventoryitem
Delete inventory item. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```item_type``` | string | Souce of inventory (kitchen, bar, pastry etc.)
```itemid``` | int | Valid Item ID


## POST /deletelaundryitem
Delete laundry item. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Laundryid``` | int | Valid laundry id


## POST /deletemessage
Delete a message. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Messageid``` | int | Valid message id


## POST /deletemessageschedule
Delete a message schedule. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Messagescheduleid``` | int | Valid message schedule id


## POST /deletepartner
Delete a partner. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Partnerid``` | int | Valid partner id


## POST /deletepastry
Delete a pastry record. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Pastryid``` | int | Valid pastry id


## POST /deletepastrycategory
Delete a pastry category. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Pastrycategoryid``` | int | Valid pastry category id


## POST /deletepoolsession
Delete a pool session. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Poolid``` | int | Valid pool id


## POST /deleteproperty
Delete a property. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Propertyid``` | int | Valid property id


## POST /deletepurchaserequest
Delete a purchase request. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```item_type``` | string | Souce of purchase (kitchen, bar, pastry etc.)
```prid``` | int | Valid purchase id


## POST /deletequotation
Delete a quotation. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```item_type``` | string | Souce of purchase (kitchen, bar, pastry etc.)
```quotationid``` | int | Valid quotation id


## POST /deletereview
Delete a review. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Reviewid``` | int | Valid review id


## POST /deleterole
Delete a role. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Roleid``` | int | Valid role id


## POST /deleteroom
Delete a room. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Roomid``` | int | Valid room id


## POST /deleteroomcategory
Delete a room category. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Roomcategoryid``` | int | Valid room category id


## POST /deleteserviceitem
Delete a service item. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```serviceId``` | int | Valid service item id


## POST /deleteshift
Delete a shift record. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Shiftid``` | int | Valid shift id


## POST /deletestaff
Delete a staff. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Staffid``` | int | Valid staff id


## POST /deletesupplier
Delete a supplier. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Supplierid``` | int | Valid supplier id


## POST /deleteteamitem
Delete a team item. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```teamId``` | int | Valid team id


## POST /deletetestimonialitem
Delete a testimonial item. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```testimonialId``` | int | Valid testimonial id


## POST /deletevehicle
Delete a vehicle information. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Vehicleid``` | int | Valid vehicle id


## POST /deletevehicle
Delete a vehicle information. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Vehicleid``` | int | Valid vehicle id


## POST /dowithdrawal
Make a withdrawal. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```month``` | string | Valid month
```year``` | string | Valid year
```item``` | string | Item name
```item_type``` | string | Valid item type (property, vehicle, leased-property)


## GET /driver
Get all drivers. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Page``` | string | Valid page name
```Perpage``` | int | Records to show per page
```Filter``` | string | Filter information
```Filtervalue``` | string | Filter from? (address, status, city, state, dob, etc.)


## GET /fetchcontactlist
Fetch contact lists. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```primers``` | string | A comma seperated value.


## GET /generatebarcode
Generates a new barcode.


## GET /generatecoupon
Generates a new coupon code.


## GET /generateitembarcode
Generates a new item barcode.


## POST /generatepurchaseorder
Generate a new purchase order. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```prid``` | int | Valid purchase ID
```items``` | string | Comma seperated items
```usersess``` | string | Loggedin customer session token


## GET /gensettings
Get site settings.


## GET /get-property
Fetch property information. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```property``` | string | Valid property ID.


## GET /get-reservation
Fetch reservation information. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```property``` | string | Valid property ID.
```Page``` | string | Valid page name
```Perpage``` | int | Records to show per page
```Filter``` | string | Filter information
```Filtervalue``` | string | Filter from? (address, status, city, state, dob, etc.)


## GET /getaboutus
Get about us information.


## GET /getadmintheme
Fetch admin theme. 


## GET /getadminusers
Fetch all admin users. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Page``` | string | Valid page name
```Perpage``` | int | Records to show per page
```Filter``` | string | Filter information
```Filtervalue``` | string | Filter from? (address, status, city, state, dob, etc.)


## GET /getallreceipts
Fetch all receipts. 


## GET /getbankaccount
Fetch the default bank account.


## GET /getbanner
Fetch banner information. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```banner``` | string | Valid banner information.


## GET /getbannerconfig
Fetch the default banner configuration


## GET /getbooking
Fetch all bookings.


## GET /getcategoryavailability
Fetch category availability. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```category``` | string | Valid category information.


## GET /getcontactlist
Fetch contact list. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```tab``` | string | Valid contact category (all, customer, guest, staff, subscribers, messaging, custom).


## GET /getcoupon
Fetch coupons. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```couponid``` | int | Valid coupon id


## GET /getcouponlist
Fetch coupon lists. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Page``` | string | Valid page name
```Perpage``` | int | Records to show per page
```Filter``` | string | Filter information
```Filtervalue``` | string | Filter from? (address, status, city, state, dob, etc.)
```property``` | string | Property name
```usestatus``` | string | A flag from any of the following (used, expired, unused)


## GET /getcurrency
Fetches the user default currency.


## GET /getcustomcontactslist
Fetches the user custom contacts list.


## GET /getcustomer
Fetches a customer information for a property. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```property``` | string | Property name or ID
```customerid``` | int | Valid customer ID


## GET /getcustomers
Fetch all customers for a property. You must send the following form data during request.

Key | Value | Description
----|-------|------------
```Page``` | string | Valid page name
```Perpage``` | int | Records to show per page
```Filter``` | string | Filter information
```Filtervalue``` | string | Filter from? (address, status, city, state, dob, etc.)
```property``` | string | Property name or ID


## GET /getdepartments
List all departments


## POST /getdiscount
You must send the following form data during request.

Key | Value 
----|-------
```property``` | string
```discountid``` | int


## POST /getdiscountlist
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string
```Filter``` | string
```Filtervalue``` | string


## POST /getdrinkcategory
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string
```Filter``` | string
```Filtervalue``` | string


## POST /getdrinklist
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string
```Filter``` | string
```Filtervalue``` | string


## POST /getdriver
You must send the following form data during request.

Key | Value 
----|-------
```Driverid``` | int


## POST /geteditreview
You must send the following form data during request.

Key | Value 
----|-------
```reviewid``` | int


## POST /getevent
You must send the following form data during request.

Key | Value 
----|-------
```eventid``` | int


## POST /geteventlog
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string
```Filter``` | string
```Filtervalue``` | string
```start_date``` | string
```stop_date``` | string


## POST /getevents
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string
```list``` | string


## POST /getextraservices
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string


## GET /getfacility
List all facilities


## POST /getfaq
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string
```Filter``` | string
```Filtervalue``` | string


## POST /getfaqcategory
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string
```Filter``` | string
```Filtervalue``` | string


## POST /getfoodcategory
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string
```Filter``` | string
```Filtervalue``` | string


## POST /getfoodlist
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string
```Filter``` | string
```Filtervalue``` | string


## GET /getgallery
Get images, videos from gallery


## GET /getgeneralsettings
Get general settings


## POST /getguest
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string
```Filter``` | string
```Filtervalue``` | string
```property``` | string
```tab``` | string


## GET /getintegrationdata
Get integration data


## POST /getinventoryaudit
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string
```searchterm``` | string
```auditid``` | int
```Page``` | string
```Perpage``` | string


## POST /getinventoryaudits
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string
```searchterm``` | string
```Page``` | string
```Perpage``` | string


## POST /getinventoryitem
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string
```itemid``` | int


## POST /getinventoryitems
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string
```filter``` | string
```searchterm``` | string
```rangestart``` | string
```rangestop``` | string
```Page``` | string
```Perpage``` | string


## POST /getitemreport
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string
```item``` | string


## POST /getitemtimeline
You must send the following form data during request.

Key | Value 
----|-------
```starttime``` | string
```stoptime``` | string
```item_type``` | string
```filter``` | string
```itemid``` | int


## POST /getlaundryitem
You must send the following form data during request.

Key | Value 
----|-------
```id``` | int


## POST /getlaundryitems
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string


## POST /getmessage
You must send the following form data during request.

Key | Value 
----|-------
```messageid``` | int


## POST /getmessages
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string
```Filter``` | string
```Filtervalue``` | string
```tab``` | string


## POST /getmessageschedule
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string
```list``` | string


## GET /getmessagesettings
Get default message settings


## POST /getmessagetemplate
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string
```Filter``` | string
```Filtervalue``` | string


## GET /getmodulesettings
Get default module settings


## GET /getpagetext
Get page information


## POST /getpartner
You must send the following form data during request.

Key | Value 
----|-------
```Partnerid``` | int


## POST /getpastrycategory
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string
```Filter``` | string
```Filtervalue``` | string


## POST /getpastrylist
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string
```Filter``` | string
```Filtervalue``` | string


## POST /getpoolsession
You must send the following form data during request.

Key | Value 
----|-------
```id``` | int


## POST /getpoolsessions
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string


## POST /getposanalytics
You must send the following form data during request.

Key | Value 
----|-------
```period``` | string
```item_type``` | string
```usersess``` | string


## POST /getposdiscount
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string


## POST /getpositems
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string


## POST /getposreceipt
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string


## POST /getposreport
You must send the following form data during request.

Key | Value 
----|-------
```start_date``` | string
```stop_date``` | string
```item_type``` | string
```plotCriteria``` | string


## POST /getpossettings
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string


## POST /getpostransaction
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string
```sale``` | string


## POST /getpostransactions
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string
```Filtervalue``` | string
```Page``` | string
```Perpage``` | string


## POST /getpriceenquiries
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string
```searchterm``` | string
```Page``` | string
```Perpage``` | string


## POST /getpriceenquiry
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string
```quotid``` | int


## GET /getprivacypolicy
Get default privacy policy


## POST /getproperty
You must send the following form data during request.

Key | Value 
----|-------
```Propertyid``` | int


## POST /getpurchaseorder
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string
```reference``` | string


## POST /getpurchaserequest
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string
```prid``` | int


## POST /getpurchaserequests
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string
```filter``` | string
```searchterm``` | string
```Page``` | string
```Perpage``` | string


## POST /getreview
You must send the following form data during request.

Key | Value 
----|-------
```reviewid``` | int


## POST /getreviewitemlist
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string
```itemid``` | int


## POST /getreviews
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string
```Filter``` | string
```Filtervalue``` | string


## POST /getreviewsession
You must send the following form data during request.

Key | Value 
----|-------
```sessionid``` | int


## POST /getrole
You must send the following form data during request.

Key | Value 
----|------- 
```usersess``` | string (Loggedin customer session token)
```roleid``` | int


## POST /getroles
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string
```Filter``` | string
```Filtervalue``` | string
```property``` | string


## POST /getroomcategory
You must send the following form data during request.

Key | Value 
----|-------
```property``` | string
```Page``` | string
```Perpage``` | string
```Filter``` | string
```Filtervalue``` | string


## POST /getroomrate
You must send the following form data during request.

Key | Value 
----|-------
```category``` | string


## POST /getrooms
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string
```Filter``` | string
```Filtervalue``` | string


## GET /getseo
Get SEO configuration


## GET /getservices
Get all services


## POST /getsettings
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string


## GET /getshift
List all shifts


## POST /getsingleshift
You must send the following form data during request.

Key | Value 
----|-------
```Shiftid``` | int


## POST /getstaff
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string
```Filter``` | string
```Filtervalue``` | string


## POST /getsupplier
You must send the following form data during request.

Key | Value 
----|-------
```id``` | int


## POST /getsupplierslist
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string
```Filter``` | string
```Filtervalue``` | string


## POST /getsystemlog
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string
```Filter``` | string
```Filtervalue``` | string
```start_date``` | string
```stop_date``` | string


## GET /gett&c
Get terms and conditions


## POST /gettakenreviewsessions
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string
```reviewid``` | int


## GET /getteam
Get team information


## GET /gettestimonial
Get testimonials


## GET /gettheme
Get the client theme


## POST /getticket
You must send the following form data during request.

Key | Value 
----|-------
```ticket``` | string


## POST /gettickets
You must send the following form data during request.

Key | Value 
----|-------
```filter``` | string
```term``` | string
```Page``` | string
```Perpage``` | string


## POST /getuserposreport
You must send the following form data during request.

Key | Value 
----|-------
```start_date``` | string
```stop_date``` | string
```item_type``` | string
```user``` | string


## POST /getuserpostransactions
You must send the following form data during request.

Key | Value 
----|-------
```start_date``` | string
```stop_date``` | string
```item_type``` | string
```Filtervalue``` | string
```Filter``` | string
```user``` | string
```sale_span``` | string
```spanStart``` | string
```spanStop``` | string
```Page``` | string
```Perpage``` | string


## POST /getvehicle
You must send the following form data during request.

Key | Value 
----|-------
```Vehicleid``` | int


## POST /getweborder
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string


## GET /hotels-ranks
List all hotels rankss


## POST /initializereservationwebpay
You must send the following form data during request.

Key | Value 
----|-------
```amount``` | string


## POST /initpaystackpay
You must send the following form data during request.

Key | Value 
----|-------
```amount``` | string


## POST /laundryonsitestatus
You must send the following form data during request.

Key | Value 
----|-------
```id``` | int
```status``` | string


## GET /list-reservation
List all reservations


## GET /listbanks
List all banks


## POST /listbanner
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string
```Filter``` | string
```Filtervalue``` | string


## GET /listcities
List all cities 


## GET /listcountries
List all countries


## GET /listcurrency
List all currencies


## GET /listdepartments
List all departments


## GET /listdrink
List all drinks


## GET /listdrinkcategory
List all drinks categories


## POST /listdriver
You must send the following form data during request.

Key | Value 
----|-------
```names``` | string
```phone``` | string
```email``` | string
```sex``` | string
```dob``` | string
```address``` | string
```city``` | string
```state``` | string


## GET /listemailtemplate
Show default email template


## GET /listextraservices
List all extra services


## GET /listfaqcategory
List all FAQ categories


## GET /listfood
List foods 


## GET /listfoodcategory
List all food categories


## GET /listguest
List all guests for a property


## GET /listmessagetemplate
Show default message templatee


## GET /listpartner
List all partners


## GET /listpastry
List all pastries


## GET /listpastrycategory
List all pastry category


## POST /listproperty
You must send the following form data during request.

Key | Value 
----|-------
```name``` | string
```phone1``` | string
```phone2``` | string
```email1``` | string
```email2``` | string
```type``` | string
```state``` | string
```statename``` | string
```cityname``` | string
```city``` | string
```description``` | string
```address``` | string
```tandc``` | string
```cashonly``` | string
```formType``` | string
```cancellation``` | string
```canceldays``` | string
```cancelhour``` | string
```damagedeposit``` | string
```damageamount``` | string
```earlycheckout``` | string
```partialpayment``` | string
```partialpayamount``` | string
```percialpaypercent``` | string
```childpolicy``` | string
```banner``` | string
```rules``` | string
```images``` | string
```facilities``` | string
```checkoutH``` | string
```checkoutM``` | string
```checkinH``` | string
```checkinM``` | string


## GET /listpropertyfacilities
List a property facility


## GET /listrole
list roles


## GET /listroomcategory
List all room categoriees


## GET /listshifts
List all shifts


## GET /listsmstemplate
List default sms templates


## GET /liststaff
List all staffs


## GET /liststates
List all states


## GET /listsuppliers
List all suppliers


## POST /listvehicle
You must send the following form data during request.

Key | Value 
----|-------
```images``` | string
```type``` | string
```model``` | string
```color``` | string
```seats``` | string
```description``` | string
```feature``` | string
```Driver``` | string
```mileage``` | string
```price``` | string
```extramile``` | string
```statename``` | string
```cityname``` | string
```state``` | string
```city``` | string


## GET /listvehiclefacilities
List all vehicle facilitiess


## GET /listvehiclefeatures
List all vehicle features


## POST /logfunding
You must send the following form data during request.

Key | Value 
----|-------
```method``` | string
```gateway``` | string
```amount``` | string
```name``` | string


## POST /loggedpartner
You must send the following form data during request.

Key | Value 
----|-------
```token``` | string  (Loggedin customer session token)


## POST /logincustomer
You must send the following form data during request.

Key | Value 
----|-------
```email``` | string
```password``` | string


## GET /main-contactus
Get contact us page


## GET /mylease
Get logged in user leases


## GET /myproperties
Get loggedin user properties


## GET /myvehicles
Get logged in user vehicles


## POST /open-reservation
You must send the following form data during request.

Key | Value 
----|-------
```booking``` | string


## POST /orderdrinknow
You must send the following form data during request.

Key | Value 
----|-------
```drink``` | string
```custsess``` | string (Loggedin customer session token)
```quantity``` | string


## POST /orderfoodnow
You must send the following form data during request.

Key | Value 
----|-------
```food``` | string
```custsess``` | string (Loggedin customer session token)
```quantity``` | string


## POST /orderpastrynow
You must send the following form data during request.

Key | Value 
----|-------
```pastry``` | string
```custsess``` | string (Loggedin customer session token)
```quantity``` | string


## GET /partner-faq
Get partner onboarding frequently asked questions.


## POST /partner
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string
```Filter``` | string
```Filtervalue``` | string


## GET /payinrequestlog
Get payin request log


## POST /payout-data
You must send the following form data during request.

Key | Value 
----|-------
```month``` | string
```year``` | string
```item``` | string
```item_type``` | string


## GET /payoutrequestlog
Get payout request log


## GET /ping
Ping API server


## POST /placeordernow
You must send the following form data during request.

Key | Value 
----|-------
```custsess``` | string (Loggedin customer session token)


## POST /postransactiondetail
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string
```transaction``` | string


## POST /printinventoryaudit
You must send the following form data during request.

Key | Value 
----|-------
```auditid``` | int
```itemtype``` | string


## POST /printitemtimeline
You must send the following form data during request.

Key | Value 
----|-------
```startdate``` | string
```stopdate``` | string
```itemid``` | int
```itemtype``` | string
```filter``` | string


## POST /printpurchaseorder
You must send the following form data during request.

Key | Value 
----|-------
```orderid``` | int
```itemtype``` | string


## POST /printquotation
You must send the following form data during request.

Key | Value 
----|-------
```quoteid``` | int
```itemtype``` | string
```filter``` | string


## POST /printsuppliercredit
You must send the following form data during request.

Key | Value 
----|-------
```noteid``` | int
```itemtype``` | string


## POST /processcoupon
You must send the following form data during request.

Key | Value 
----|-------
```code``` | string
```item_type``` | string


## POST /property-details
You must send the following form data during request.

Key | Value 
----|-------
```property``` | string


## POST /property
You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string
```Filter``` | string
```Filtervalue``` | string


## POST /receiveorder
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string
```order``` | string
```items``` | string
```usersess``` | string (Loggedin customer session token)


## POST /removeavailability
You must send the following form data during request.

Key | Value 
----|-------
```avail``` | string


## POST /removecoupon
You must send the following form data during request.

Key | Value 
----|-------
```coupon``` | string


## POST /removeitem
You must send the following form data during request.

Key | Value 
----|-------
```item``` | string


## POST /removerate
You must send the following form data during request.

Key | Value 
----|-------
```rate``` | string


## POST /request-corporate
You must send the following form data during request.

Key | Value 
----|-------
```company``` | string
```phone``` | string
```email``` | string
```state``` | string
```city``` | string


## POST /resendquotation
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string
```quoteid``` | int
```supplier``` | string


## POST /reservation-data
You must send the following form data during request.

Key | Value 
----|-------
```booking``` | string


## GET /reviewresponsedata
Get review response data.


## POST /save-cancellation
You must send the following form data during request.

Key | Value 
----|-------
```property``` | string
```status``` | string


## POST /save-online-pay
You must send the following form data during request.

Key | Value 
----|-------
```property``` | string
```status``` | string


## POST /save-self-checkin
You must send the following form data during request.

Key | Value 
----|-------
```property``` | string
```status``` | string


## POST /save-tag-handling
You must send the following form data during request.

Key | Value 
----|-------
```property``` | string
```status``` | string


## POST /saveaboutus
You must send the following form data during request.

Key | Value 
----|-------
```content``` | string


## POST /saveadminpassword
You must send the following form data during request.

Key | Value 
----|-------
```usersess``` | string (Loggedin customer session token) 
```password``` | string


## POST /saveadminuser
You must send the following form data during request.

Key | Value 
----|-------
```userid``` | int
```username``` | string
```name``` | string
```role``` | string
```staffid``` | int
```password``` | string


## POST /saveadminusername
You must send the following form data during request.

Key | Value 
----|-------
```usersess``` | string
```username``` | string


## POST /saveanalyticsintegration
You must send the following form data during request.

Key | Value 
----|-------
```analytics``` | string


## POST /saveauditcount
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string
```auditid``` | int
```itemid``` | int
```counted``` | string


## POST /saveautoseostatus
You must send the following form data during request.

Key | Value 
----|-------
```Autoseo``` | string


## POST /savebank
You must send the following form data during request.

Key | Value 
----|-------
```bank``` | string
```accountName``` | string
```accountNumber``` | string


## POST /savebanner
You must send the following form data during request.

Key | Value 
----|-------
```id``` | int
```image``` | string
```main``` | string
```sub``` | string
```status``` | string
```sort``` | string


## POST /savebarseo
You must send the following form data during request.

Key | Value 
----|-------
```keyword``` | string
```description``` | string


## POST /savecontact
You must send the following form data during request.

Key | Value 
----|-------
```names``` | string
```id``` | int
```email``` | string
```phone``` | string


## POST /savecontacttolist
You must send the following form data during request.

Key | Value 
----|-------
```data``` | string
```property``` | string


## POST /savecoupon
You must send the following form data during request.

Key | Value 
----|-------
```property``` | string
```id``` | int
```bypercent``` | string
```value``` | string
```use``` | string
```name``` | string
```code``` | string
```expires``` | string
```lodging``` | string
```food``` | string
```bakery``` | string
```bar``` | string
```laundry``` | string
```pool``` | string
```services``` | string


## POST /savecurrency
You must send the following form data during request.

Key | Value 
----|-------
```currency``` | string


## POST /savecustomer
You must send the following form data during request.

Key | Value 
----|-------
```customerid``` | int
```email``` | string
```phone``` | string
```name``` | string
```surname``` | string
```country``` | string
```state``` | string
```city``` | string
```street``` | string
```sex``` | string
```guestid``` | int
```password``` | string
```newletter``` | string


## POST /savecustomerssettings
You must send the following form data during request.

Key | Value 
----|-------
```collectaddress``` | string
```allowselfmgt``` | string


## POST /savecustomlist
You must send the following form data during request.

Key | Value 
----|-------
```id``` | int
```name``` | string


## POST /savedepartment
You must send the following form data during request.

Key | Value 
----|-------
```dept_id``` | int
```name``` | string


## POST /savediscount
You must send the following form data during request.

Key | Value 
----|-------
```property``` | string
```id``` | int
```bypercent``` | string
```value``` | string
```name``` | string
```lodging``` | string
```food``` | string
```bakery``` | string
```bar``` | string
```laundry``` | string
```pool``` | string
```services``` | string
```status``` | string
```autoapply``` | string
```fromamount``` | string
```toamount``` | string
```fromcount``` | string
```tocount``` | string
```fromhour``` | string
```tohour``` | string
```fromminuite``` | string
```tominuite``` | string
```fromday``` | string
```today``` | string
```frommonth``` | string
```tomonth``` | string
```frommeridean``` | string
```tomeridean``` | string
```isstaff``` | string
```periodic``` | string
```timebased``` | string
```bookingcount``` | string
```formerorder``` | string
```onlineorder``` | string
```offlineorder``` | string
```quantity``` | string
```bookedroom``` | string
```bookeddays``` | string
```amountbased``` | string
```ontotal``` | string


## POST /savediscountstatus
You must send the following form data during request.

Key | Value 
----|-------
```property``` | string
```Discountid``` | int
```status``` | string


## POST /savedrink
You must send the following form data during request.

Key | Value 
----|-------
```drinkid``` | int
```name``` | string
```category``` | string
```showonsite``` | string
```status``` | string
```showpromo``` | string
```reservable``` | string
```inventory``` | string
```sort``` | string
```price``` | string
```tax``` | string
```compare``` | string
```pos``` | string
```barcode``` | string
```cost``` | string
```images``` | string
```description``` | string
```promotext``` | string
```unit``` | string
```pluralunit``` | string
```lowstockpoint``` | string
```suppliers``` | string
```openingstock``` | string
```usersess``` | string


## POST /savedrinkcategory
You must send the following form data during request.

Key | Value 
----|-------
```catid``` | int
```title``` | string
```sort``` | string
```status``` | string


## POST /savedrinkcategorystatus
You must send the following form data during request.

Key | Value 
----|-------


## POST /savedrinkinventorytracking
You must send the following form data during request.

Key | Value 
----|-------
```Drinkid``` | int
```inventory``` | string


## POST /savedrinkreservablity
You must send the following form data during request.

Key | Value 
----|-------
```Drinkid``` | int
```Reservable``` | string


## POST /savedrinkstatus
You must send the following form data during request.

Key | Value 
----|-------
```Drinkid``` | int
```Status``` | string


## POST /savedrinkvisibility
You must send the following form data during request.

Key | Value 
----|-------
```Drinkid``` | int
```Onsite``` | string


## POST /savedriver
You must send the following form data during request.

Key | Value 
----|-------
```Driverid``` | int
```Name``` | string
```Surname``` | string
```Phone``` | string
```Email``` | string
```Password``` | string
```Profilepic``` | string
```Gender``` | string
```Dob``` | string
```Address``` | string
```City``` | string
```State``` | string
```Available``` | string
```Status``` | string


## POST /saveevent
You must send the following form data during request.

Key | Value 
----|-------
```id``` | int
```title``` | string
```message``` | string
```event``` | string
```delayhours``` | string
```delaymins``` | string
```contextuser``` | string
```status``` | string
```contactcollection``` | string
```contacts``` | string


## POST /saveextraservice
You must send the following form data during request.

Key | Value 
----|-------
```id``` | int
```name``` | string
```price``` | string


## POST /savefacility
You must send the following form data during request.

Key | Value 
----|-------
```facilityid``` | int
```status``` | string
```body``` | string
```heading``` | string
```image``` | string
```icontype``` | string
```sort``` | string


## POST /savefaq
You must send the following form data during request.

Key | Value 
----|-------
```faqid``` | int
```question``` | string
```answer``` | string
```category``` | string
```sort``` | string
```status``` | string


## POST /savefaqcategory
You must send the following form data during request.

Key | Value 
----|-------
```catid``` | int
```title``` | string
```sort``` | string
```status``` | string


## POST /savefood
You must send the following form data during request.

Key | Value 
----|-------
```foodid``` | int
```name``` | string
```category``` | string
```showonsite``` | string
```status``` | string
```showpromo``` | string
```reservable``` | string
```inventory``` | string
```sort``` | string
```price``` | string
```tax``` | string
```compare``` | string
```pos``` | string
```barcode``` | string
```cost``` | string
```images``` | string
```description``` | string
```promotext``` | string
```unit``` | string
```pluralunit``` | string
```lowstockpoint``` | string
```suppliers``` | string
```openingstock``` | string
```usersess``` | string (Loggedin customer session token)


## POST /savefoodcategory
You must send the following form data during request.

Key | Value 
----|-------
```catid``` | int
```title``` | string
```sort``` | string
```status``` | string


## POST /savefoodcategorystatus
You must send the following form data during request.

Key | Value 
----|-------
```Foodcategoryid``` | int
```Status``` | string


## POST /savefoodinventorytracking
You must send the following form data during request.

Key | Value 
----|-------
```Foodid``` | int
```inventory``` | string


## POST /savefoodreservablity
You must send the following form data during request.

Key | Value 
----|-------
```Foodid``` | int
```Reservable``` | string


## POST /savefoodstatus
You must send the following form data during request.

Key | Value 
----|-------
```Foodid``` | int
```Status``` | string


## POST /savefoodvisibility
You must send the following form data during request.

Key | Value 
----|-------
```Foodid``` | int
```Onsite``` | string


## POST /savegallery
You must send the following form data during request.

Key | Value 
----|-------
```galleryid``` | int
```status``` | string
```description``` | string
```heading``` | string
```image``` | string
```sort``` | string


## POST /savegoogletagintegration
You must send the following form data during request.

Key | Value 
----|-------
```googletag``` | string


## POST /saveguestformsettings
You must send the following form data during request.

Key | Value 
----|-------
```collectaddress``` | string


## POST /savehomepageseo
You must send the following form data during request.

Key | Value 
----|-------
```keyword``` | string
```description``` | string


## POST /saveinterswitchintegration
You must send the following form data during request.

Key | Value 
----|-------
```marchantid``` | int


## POST /saveinventoryactivity
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string
```data``` | string
```activity``` | string
```usersess``` | string (Loggedin customer session token)
```note``` | string


## POST /saveinventoryaudit
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string
```id``` | int
```title``` | string


## POST /saveinventoryitem
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string
```itemid``` | int
```image``` | string
```name``` | string
```unit``` | string
```pluralunit``` | string
```sku``` | string
```productid``` | int
```lowstockpoint``` | string
```suppliers``` | string
```openingstock``` | string
```usersess``` | string


## POST /savelaundryitem
You must send the following form data during request.

Key | Value 
----|-------
```id``` | int
```name``` | string
```price``` | string
```status``` | string
```tax``` | string
```onsite``` | string


## POST /savelivechatintegration
You must send the following form data during request.

Key | Value 
----|-------
```livechat``` | string


## POST /savelodgingseo
You must send the following form data during request.

Key | Value 
----|-------
```keyword``` | string
```description``` | string


## POST /savelogo
You must send the following form data during request.

Key | Value 
----|-------
```logo``` | string


## POST /savelogonamesettings
You must send the following form data during request.

Key | Value 
----|-------
```showlogo``` | string
```showname``` | string


## POST /savemapintegration
You must send the following form data during request.

Key | Value 
----|-------
```longitude``` | string
```latitude``` | string
```apikey``` | string


## POST /savemessageschedule
You must send the following form data during request.

Key | Value 
----|-------
```id``` | int
```title``` | string
```message``` | string
```year``` | string
```month``` | string
```day``` | string
```hour``` | string
```min``` | string
```status``` | string
```gmt``` | string
```inifinity``` | string
```autodelete``` | string
```executions``` | string
```contactcollection``` | string
```contacts``` | string


## POST /savemessagesettings
You must send the following form data during request.

Key | Value 
----|-------
```lowunitphone``` | string
```tagprocessing``` | string
```ononiruapikey``` | string
```lowunitpoint``` | string


## POST /savemessagetemplate
You must send the following form data during request.

Key | Value 
----|-------
```messageid``` | int
```from``` | string
```fromname``` | string
```replyto``` | string
```attachment``` | string
```subject``` | string
```body``` | string
```status``` | string
```type``` | string
```title``` | string


## POST /savemodulesettings
You must send the following form data during request.

Key | Value 
----|-------
```aboutus``` | string
```bakery``` | string
```bar``` | string
```booking``` | string
```contactus``` | string
```customer``` | string
```discount``` | string
```facilities``` | string
```faq``` | string
```gallery``` | string
```kitchen``` | string
```laundry``` | string
```lodging``` | string
```newsletter``` | string
```testimonials``` | string
```terms``` | string
```team``` | string
```policy``` | string
```pagetext``` | string
```services``` | string


## POST /savepagetext
You must send the following form data during request.

Key | Value 
----|-------
```content``` | string


## POST /savepartner
You must send the following form data during request.

Key | Value 
----|-------
```Partnerid``` | int
```Salutation``` | string
```Name``` | string
```Surname``` | string
```Phone``` | string
```Email``` | string
```Profilepic``` | string
```Gender``` | string
```Country``` | string
```State``` | string
```City``` | string
```Address``` | string
```Status``` | string


## POST /savepassword
You must send the following form data during request.

Key | Value 
----|-------
```old``` | string
```newpassword``` | string


## POST /savepastry
You must send the following form data during request.

Key | Value 
----|-------
```pastryid``` | int
```name``` | string
```category``` | string
```showonsite``` | string
```status``` | string
```showpromo``` | string
```reservable``` | string
```inventory``` | string
```sort``` | string
```price``` | string
```tax``` | string
```compare``` | string
```pos``` | string
```barcode``` | string
```cost``` | string
```images``` | string
```description``` | string
```promotext``` | string
```unit``` | string
```pluralunit``` | string
```lowstockpoint``` | string
```suppliers``` | string
```openingstock``` | string
```usersess``` | string (Loggedin customer session token)


## POST /savepastrycategory
You must send the following form data during request.

Key | Value 
----|-------
```catid``` | int
```title``` | string
```sort``` | string
```status``` | string


## POST /savepastrycategorystatus
You must send the following form data during request.

Key | Value 
----|-------


## POST /savepastryinventorytracking
You must send the following form data during request.

Key | Value 
----|-------
```Pastryid``` | int
```inventory``` | string


## POST /savepastryreservablity
You must send the following form data during request.

Key | Value 
----|-------
```Pastryid``` | int
```Reservable``` | string


## POST /savepastryseo
You must send the following form data during request.

Key | Value 
----|-------
```keyword``` | string
```description``` | string


## POST /savepastrystatus
You must send the following form data during request.

Key | Value 
----|-------
```Pastryid``` | int
```Status``` | string


## POST /savepastryvisibility
You must send the following form data during request.

Key | Value 
----|-------
```Pastryid``` | int
```Onsite``` | string


## POST /savepaypalintegration
You must send the following form data during request.

Key | Value 
----|-------
```paypalid``` | int
```username``` | string
```password``` | string


## POST /savepaystackintegration
You must send the following form data during request.

Key | Value 
----|-------
```privatekey``` | string
```publickey``` | string


## POST /savepoolsession
You must send the following form data during request.

Key | Value 
----|-------
```id``` | int
```name``` | string
```price``` | string
```status``` | string
```tax``` | string


## POST /savepossale
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string
```paidAmount``` | string
```posuser``` | string
```time``` | string
```method``` | string
```total``` | string
```discount``` | string
```taxes``` | string
```entity``` | string
```isWeborder``` | string
```transId``` | int
```coupons``` | string
```discounts``` | string
```items``` | string
```weborder``` | string
```couponPixels``` | string
```discountPixels``` | string


## POST /saveprivacypolicy
You must send the following form data during request.

Key | Value 
----|-------
```content``` | string


## POST /saveprofile
You must send the following form data during request.

Key | Value 
----|-------
```name``` | string
```sname``` | string
```phone``` | string
```country``` | string
```city``` | string
```state``` | string
```gender``` | string


## POST /saveprofilepicture
You must send the following form data during request.

Key | Value 
----|-------
```custsess``` | string (Loggedin customer session token)
```img``` | string
```job``` | string


## POST /saveproperty
You must send the following form data during request.

Key | Value 
----|-------
```Propertyid``` | int
```Name``` | string
```Phone1``` | string
```Phone2``` | string
```Email1``` | string
```Email2``` | string
```Type``` | string
```State``` | string
```City``` | string
```Description``` | string
```Address``` | string
```Tandc``` | string
```Images``` | string
```Wifi``` | string
```Parking``` | string
```Gym``` | string
```Restaurant``` | string
```Bar``` | string
```Security``` | string
```Status``` | string


## POST /savepurchaserequest
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string
```prid``` | int
```data``` | string
```note``` | string
```usersess``` | string (Loggedin customer session token)


## POST /savereservation
You must send the following form data during request.

Key | Value 
----|-------
```custsess``` | string (Loggedin customer session token)


## POST /saverestaurantseo
You must send the following form data during request.

Key | Value 
----|-------
```keyword``` | string
```description``` | string


## POST /savereview
You must send the following form data during request.

Key | Value 
----|-------
```reviewid``` | int
```title``` | string
```body``` | string
```data``` | string


## POST /saverole
You must send the following form data during request.

Key | Value 
----|-------
```Roleid``` | int
```name``` | string
```booking_read``` | string
```booking_write``` | string
```coupon_read``` | string
```coupon_write``` | string
```customer_read``` | string
```customer_write``` | string
```staff_read``` | string
```staff_write``` | string
```rooms_read``` | string
```rooms_write``` | string
```kitchen_read``` | string
```kitchen_write``` | string
```bakery_read``` | string
```bakery_write``` | string
```bar_read``` | string
```bar_write``` | string
```laundry_read``` | string
```laundry_write``` | string
```housekeeping_read``` | string
```housekeeping_write``` | string
```pool_read``` | string
```pool_write``` | string
```store_read``` | string
```store_write``` | string
```event_read``` | string
```event_write``` | string
```finance_read``` | string
```finance_write``` | string
```branch_read``` | string
```branch_write``` | string
```log_read``` | string
```log_write``` | string
```reporting_read``` | string
```reporting_write``` | string
```messaging_read``` | string
```messaging_write``` | string
```webfront_read``` | string
```webfront_write``` | string
```webconfig_read``` | string
```webconfig_write``` | string
```settings_read``` | string
```settings_write``` | string
```frontdesk``` | string
```bakery_pos``` | string
```kitchen_pos``` | string
```pools_pos``` | string
```laundry_pos``` | string
```bar_pos``` | string
```property``` | string


## POST /saveroom
You must send the following form data during request.

Key | Value 
----|-------
```property``` | string
```roomid``` | int
```number``` | string
```category``` | string
```status``` | string
```features``` | string


## POST /saveroomavailability
You must send the following form data during request.

Key | Value 
----|-------
```property``` | string
```available``` | string
```start``` | string
```stop``` | string
```category``` | string


## POST /saveroomcategory
You must send the following form data during request.

Key | Value 
----|-------
```property``` | string
```roomcatid``` | int
```sort``` | string
```description``` | string
```name``` | string
```compare``` | string
```features``` | string
```images``` | string
```showonsite``` | string
```price``` | string
```promotext``` | string
```reservable``` | string
```services``` | string
```showpromo``` | string
```extrapersonprice``` | string
```baseoccupancy``` | string
```maxoccupancy``` | string
```smoking``` | string
```children``` | string
```pets``` | string


## POST /saveroomcategoryreservable
You must send the following form data during request.

Key | Value 
----|-------
```property``` | string
```Roomcategoryid``` | int
```Reservable``` | string


## POST /saveroomcategorystatus
You must send the following form data during request.

Key | Value 
----|-------
```property``` | string
```Roomcategoryid``` | int
```Status``` | string


## POST /saveroomcategoryvisibility
You must send the following form data during request.

Key | Value 
----|-------
```property``` | string
```Roomcategoryid``` | int
```Onsite``` | string


## POST /saveroomrate
You must send the following form data during request.

Key | Value 
----|-------
```category``` | string
```start``` | string
```stop``` | string
```rate``` | string


## POST /saveroomstatus
You must send the following form data during request.

Key | Value 
----|-------
```property``` | string
```Roomid``` | int
```Status``` | string


## POST /saveservice
You must send the following form data during request.

Key | Value 
----|-------
```serviceid``` | int
```status``` | string
```body``` | string
```heading``` | string
```image``` | string
```icontype``` | string
```sort``` | string


## POST /savesettings
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string
```receipttemplate``` | string
```papertype``` | string
```lowstockemail``` | string
```lowstockphone``` | string
```onlineorderphone``` | string
```receiptaddess``` | string
```receiptemail``` | string
```receiptlogo``` | string
```receiptsalutation``` | string
```cash_pay``` | string
```pos_pay``` | string
```online_pay``` | string
```other_pay``` | string
```refund``` | string
```compound_tax``` | string
```salutation``` | string


## POST /saveshift
You must send the following form data during request.

Key | Value 
----|-------
```shiftid``` | int
```name``` | string
```monday``` | string
```tueday``` | string
```wedday``` | string
```thuday``` | string
```friday``` | string
```satday``` | string
```sunday``` | string
```starthour``` | string
```stophour``` | string
```startmin``` | string
```stopmin``` | string
```startgmt``` | string
```stopgmt``` | string


## POST /savesocialintegration
You must send the following form data during request.

Key | Value 
----|-------
```facebook``` | string
```twitter``` | string
```instagram``` | string
```google``` | string
```whatsapp``` | string
```telegram``` | string
```linkedin``` | string


## POST /savestaff
You must send the following form data during request.

Key | Value 
----|-------
```usersess``` | string (Loggedin customer session token)
```staffid``` | int
```name``` | string
```surname``` | string
```phone``` | string
```email``` | string
```country``` | string
```state``` | string
```address``` | string
```sex``` | string
```dateofbirth``` | string
```department``` | string
```shift``` | string
```position``` | string
```bank``` | string
```accname``` | string
```accountnum``` | string
```passport``` | string
```fullshot``` | string
```biodata``` | string
```salary``` | string


## POST /savesubscriberemail
You must send the following form data during request.

Key | Value 
----|-------
```email``` | string


## POST /savesupplier
You must send the following form data during request.

Key | Value 
----|-------
```id``` | int
```company``` | string
```phone``` | string
```email``` | string
```name``` | string
```surname``` | string
```address``` | string


## POST /savet&c
You must send the following form data during request.

Key | Value 
----|-------
```content``` | string


## POST /saveteam
You must send the following form data during request.

Key | Value 
----|-------
```teamid``` | int
```status``` | string
```description``` | string
```name``` | string
```image``` | string
```sort``` | string


## POST /savetestimonial
You must send the following form data during request.

Key | Value 
----|-------
```teamid``` | int
```status``` | string
```testimony``` | string
```name``` | string
```image``` | string
```sort``` | string
```rating``` | string


## POST /saveticket
You must send the following form data during request.

Key | Value 
----|-------
```Subject``` | string
```Body``` | string
```File``` | string


## POST /saveticketreply
You must send the following form data during request.

Key | Value 
----|-------
```ticket``` | string
```reply``` | string


## POST /savetranslatorintegration
You must send the following form data during request.

Key | Value 
----|-------
```translator``` | string


## POST /savevehicle
You must send the following form data during request.

Key | Value 
----|-------
```Vehicleid``` | int
```Image1``` | string
```Image2``` | string
```Image3``` | string
```Image4``` | string
```Type``` | string
```Model``` | string
```Color``` | string
```Seats``` | string
```Description``` | string
```Ac``` | string
```Automatic``` | string
```Tv``` | string
```Fridge``` | string
```Seatwarmer``` | string
```Cupholder``` | string
```Status``` | string
```Driver``` | string
```Milagecap``` | string
```Price``` | string
```Extramilage``` | string
```State``` | string
```City``` | string


## POST /savewebfrontinfo
You must send the following form data during request.

Key | Value 
----|-------
```phone1``` | string
```phone2``` | string
```email1``` | string
```email2``` | string


## POST /savewebfrontsettings
You must send the following form data during request.

Key | Value 
----|-------
```primarycolor``` | string
```secondarycolor``` | string
```primaryfont``` | string
```secondaryfont``` | string
```boldfont``` | string
```sleakfont``` | string


## POST /savewebpaystatus
You must send the following form data during request.

Key | Value 
----|-------
```webpay``` | string
```nopayreservation``` | string


## POST /search
You must send the following form data during request.

Key | Value 
----|-------
```city``` | string
```checkin``` | string
```checkout``` | string
```minprice``` | string
```maxprice``` | string
```hotel``` | string
```bandb``` | string
```apartment``` | string
```condor``` | string
```studio``` | string
```boutique``` | string
```partialpay``` | string
```cancellation``` | string
```earlycheckout``` | string
```cashonly``` | string
```damagedeposit``` | string
```policies``` | string
```facilities``` | string
```star1``` | string
```star2``` | string
```star3``` | string
```star4``` | string
```star5``` | string
```rating1``` | string
```rating2``` | string
```rating3``` | string
```rating4``` | string
```rating5``` | string


## POST /searchcars
You must send the following form data during request.

Key | Value 
----|-------
```city``` | string
```pickup``` | string
```dropoff``` | string
```minprice``` | string
```maxprice``` | string
```sedan``` | string
```suv``` | string
```station_wagon``` | string
```hatch_back``` | string
```truck``` | string
```van``` | string
```small``` | string
```sports``` | string
```electric``` | string
```motocycle``` | string
```convertible``` | string
```partialpay``` | string
```cancellation``` | string
```earlycheckout``` | string
```cashonly``` | string
```damagedeposit``` | string
```policies``` | string
```facilities``` | string
```rating1``` | string
```rating2``` | string
```rating3``` | string
```rating4``` | string
```rating5``` | string


## POST /searchcountries
You must send the following form data during request.

Key | Value 
----|-------
```q``` | string


## POST /searchdrink
You must send the following form data during request.

Key | Value 
----|-------
```q``` | string


## POST /searchfood
You must send the following form data during request.

Key | Value 
----|-------
```q``` | string


## POST /searchpastry
You must send the following form data during request.

Key | Value 
----|-------
```q``` | string


## POST /sendmail
You must send the following form data during request.

Key | Value 
----|-------
```user``` | string
```type``` | string
```from``` | string
```name``` | string
```subject``` | string
```replyto``` | string
```replytoname``` | string
```attachment``` | string
```message``` | string


## POST /sendmessage
You must send the following form data during request.

Key | Value 
----|-------
```names``` | string
```email``` | string
```phone``` | string
```message``` | string


## POST /sendorder
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string
```reference``` | string


## POST /sendquotationrequest
You must send the following form data during request.

Key | Value 
----|-------
```item_type``` | string
```prid``` | int
```data``` | string
```toassociatedSp``` | string
```suppliers``` | string
```sendsms``` | string
```sendmail``` | string
```note``` | string


## POST /sendquotationresponse
You must send the following form data during request.

Key | Value 
----|-------
```sessionid``` | int
```data``` | string


## POST /sendreviewresponse
You must send the following form data during request.

Key | Value 
----|-------
```sessionid``` | int
```channel``` | string
```data``` | string


## POST /sendsms
You must send the following form data during request.

Key | Value 
----|-------
```user``` | string
```type``` | string
```fromname``` | string
```message``` | string


## POST /set-item
You must send the following form data during request.

Key | Value 
----|-------
```customer``` | string
```itemname``` | string
```itemvalue``` | string


## POST /set-property-status
You must send the following form data during request.

Key | Value 
----|-------
```property``` | string
```status``` | string


## POST /setadmintheme
You must send the following form data during request.

Key | Value 
----|-------
```theme``` | string


## POST /setbannerstatus
You must send the following form data during request.

Key | Value 
----|-------
```Bannerid``` | int
```Status``` | string


## POST /setclienttheme
You must send the following form data during request.

Key | Value 
----|-------
```theme``` | string


## POST /setfaqcategorystatus
You must send the following form data during request.

Key | Value 
----|-------
```usersess``` | string (Loggedin customer session token)
```Faqcategoryid``` | int
```Status``` | string


## POST /setfaqstatus
You must send the following form data during request.

Key | Value 
----|-------
```Faqid``` | int
```Status``` | string


## POST /setuserstatus
You must send the following form data during request.

Key | Value 
----|-------
```userid``` | int
```status``` | string


## POST /signin
You must send the following form data during request.

Key | Value 
----|-------
```user``` | string
```password``` | string
```args``` | string


## POST /signup
You must send the following form data during request.

Key | Value 
----|-------
```email``` | string
```phone``` | string
```names``` | string
```password``` | string


## POST /single-room
You must send the following form data during request.

Key | Value 
----|-------
```property``` | string
```roomid``` | int


## POST /singledrink
You must send the following form data during request.

Key | Value 
----|-------
```drinkid``` | int


## POST /singlefood
You must send the following form data during request.

Key | Value 
----|-------
```foodid``` | int


## POST /singlemessageschedule
You must send the following form data during request.

Key | Value 
----|-------
```scheduleid``` | int


## POST /singlemessagetemplate
You must send the following form data during request.

Key | Value 
----|-------
```messageid``` | int


## POST /singlepastry
You must send the following form data during request.

Key | Value 
----|-------
```Pastryid``` | int


## POST /singleroomcategory
You must send the following form data during request.

Key | Value 
----|-------
```property``` | string
```roomcategoryid``` | int


## POST /soft-search
You must send the following form data during request.

Key | Value 
----|-------
```q``` | string


## POST /starmessage
You must send the following form data during request.

Key | Value 
----|-------
```Messageid``` | int


## POST /start-reservation
You must send the following form data during request.

Key | Value 
----|-------
```property``` | string
```checkin``` | string
```checkout``` | string
```adult``` | string
```children``` | string
```rooms``` | string


## POST /startbooking
You must send the following form data during request.

Key | Value 
----|-------
```room``` | string
```checkin``` | string
```checkout``` | string


## POST /startdrinkreservation
You must send the following form data during request.

Key | Value 
----|-------
```drink``` | string
```custsess``` | string (Loggedin customer session token)


## POST /startfoodreservation
You must send the following form data during request.

Key | Value 
----|-------
```food``` | string
```custsess``` | string (Loggedin customer session token)


## POST /startpastryreservation
You must send the following form data during request.

Key | Value 
----|-------
```pastry``` | string
```custsess``` | string (Loggedin customer session token)


## GET /token
Returns a random token


## POST /ui-blocks
You must send the following form data during request.

Key | Value 
----|-------
```customer``` | string


## POST /unstarmessage
You must send the following form data during request.

Key | Value 
----|-------
```Messageid``` | int


## POST /updateadminuserpassword
You must send the following form data during request.

Key | Value 
----|-------
```old``` | string
```new``` | string


## POST /updatedrinkquantity
You must send the following form data during request.

Key | Value 
----|-------
```itemid``` | int
```quantity``` | string


## POST /updatefoodquantity
You must send the following form data during request.

Key | Value 
----|-------
```itemid``` | int
```quantity``` | string


## POST /updatepassword
You must send the following form data during request.

Key | Value 
----|-------
```custsess``` | string (Loggedin customer session token)
```oldpassword``` | string
```newpassword``` | string


## POST /updatepastryquantity
You must send the following form data during request.

Key | Value 
----|-------
```itemid``` | int
```quantity``` | string


## POST /updateprofile
You must send the following form data during request.

Key | Value 
----|-------
```token``` | string
```custsess``` | string (Loggedin customer session token)
```name``` | string
```sname``` | string
```dob``` | string
```state``` | string
```country``` | string
```street``` | string
```occupation``` | string
```kin_name``` | string
```kin_address``` | string


## POST /updateroombooking
You must send the following form data during request.

Key | Value 
----|-------
```itemid``` | int
```guest``` | string
```start_date``` | string
```stop_date``` | string


## POST /vehicle-details
Get a vehicle detail. You must send the following form data during request.

Key | Value 
----|-------
```vehicle``` | string


## POST /vehicle
Get vehicles. You must send the following form data during request.

Key | Value 
----|-------
```Page``` | string
```Perpage``` | string
```Filter``` | string
```Filtervalue``` | string


## POST /wallet-balance
Get wallet balance. You must send the following form data during request.

Key | Value 
----|-------
```filter``` | string