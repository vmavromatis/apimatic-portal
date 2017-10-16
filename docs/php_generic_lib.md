# Getting started

APItude complete postman collection, with both BookingAPI & ContentAPI. You have the full details of our API in our developer portal:
https://developer.hotelbeds.com/docs?hotel

## How to Build

The generated code has dependencies over external libraries like UniRest. These dependencies are defined in the ```composer.json``` file that comes with the SDK. 
To resolve these dependencies, we use the Composer package manager which requires PHP greater than 5.3.2 installed in your system. 
Visit [https://getcomposer.org/download/](https://getcomposer.org/download/) to download the installer file for Composer and run it in your system. 
Open command prompt and type ```composer --version```. This should display the current version of the Composer installed if the installation was successful.

* Using command line, navigate to the directory containing the generated files (including ```composer.json```) for the SDK. 
* Run the command ```composer install```. This should install all the required dependencies and create the ```vendor``` directory in your project directory.

![Building SDK - Step 1](https://apidocs.io/illustration/php?step=installDependencies&workspaceFolder=APItude%20BookingAPI%20Swagger-PHP)

### [For Windows Users Only] Configuring CURL Certificate Path in php.ini

CURL used to include a list of accepted CAs, but no longer bundles ANY CA certs. So by default it will reject all SSL certificates as unverifiable. You will have to get your CA's cert and point curl at it. The steps are as follows:

1. Download the certificate bundle (.pem file) from [https://curl.haxx.se/docs/caextract.html](https://curl.haxx.se/docs/caextract.html) on to your system.
2. Add curl.cainfo = "PATH_TO/cacert.pem" to your php.ini file located in your php installation. “PATH_TO” must be an absolute path containing the .pem file.

```ini
[curl]
; A default value for the CURLOPT_CAINFO option. This is required to be an
; absolute path.
;curl.cainfo =
```

## How to Use

The following section explains how to use the APItudeBookingAPISwagger library in a new project.

### 1. Open Project in an IDE

Open an IDE for PHP like PhpStorm. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

![Open project in PHPStorm - Step 1](https://apidocs.io/illustration/php?step=openIDE&workspaceFolder=APItude%20BookingAPI%20Swagger-PHP)

Click on ```Open``` in PhpStorm to browse to your generated SDK directory and then click ```OK```.

![Open project in PHPStorm - Step 2](https://apidocs.io/illustration/php?step=openProject0&workspaceFolder=APItude%20BookingAPI%20Swagger-PHP)     

### 2. Add a new Test Project

Create a new directory by right clicking on the solution name as shown below:

![Add a new project in PHPStorm - Step 1](https://apidocs.io/illustration/php?step=createDirectory&workspaceFolder=APItude%20BookingAPI%20Swagger-PHP)

Name the directory as "test"

![Add a new project in PHPStorm - Step 2](https://apidocs.io/illustration/php?step=nameDirectory&workspaceFolder=APItude%20BookingAPI%20Swagger-PHP)
   
Add a PHP file to this project

![Add a new project in PHPStorm - Step 3](https://apidocs.io/illustration/php?step=createFile&workspaceFolder=APItude%20BookingAPI%20Swagger-PHP)

Name it "testSDK"

![Add a new project in PHPStorm - Step 4](https://apidocs.io/illustration/php?step=nameFile&workspaceFolder=APItude%20BookingAPI%20Swagger-PHP)

Depending on your project setup, you might need to include composer's autoloader in your PHP code to enable auto loading of classes.

```PHP
require_once "../vendor/autoload.php";
```

It is important that the path inside require_once correctly points to the file ```autoload.php``` inside the vendor directory created during dependency installations.

![Add a new project in PHPStorm - Step 4](https://apidocs.io/illustration/php?step=projectFiles&workspaceFolder=APItude%20BookingAPI%20Swagger-PHP)

After this you can add code to initialize the client library and acquire the instance of a Controller class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

### 3. Run the Test Project

To run your project you must set the Interpreter for your project. Interpreter is the PHP engine installed on your computer.

Open ```Settings``` from ```File``` menu.

![Run Test Project - Step 1](https://apidocs.io/illustration/php?step=openSettings&workspaceFolder=APItude%20BookingAPI%20Swagger-PHP)

Select ```PHP``` from within ```Languages & Frameworks```

![Run Test Project - Step 2](https://apidocs.io/illustration/php?step=setInterpreter0&workspaceFolder=APItude%20BookingAPI%20Swagger-PHP)

Browse for Interpreters near the ```Interpreter``` option and choose your interpreter.

![Run Test Project - Step 3](https://apidocs.io/illustration/php?step=setInterpreter1&workspaceFolder=APItude%20BookingAPI%20Swagger-PHP)

Once the interpreter is selected, click ```OK```

![Run Test Project - Step 4](https://apidocs.io/illustration/php?step=setInterpreter2&workspaceFolder=APItude%20BookingAPI%20Swagger-PHP)

To run your project, right click on your PHP file inside your Test project and click on ```Run```

![Run Test Project - Step 5](https://apidocs.io/illustration/php?step=runProject&workspaceFolder=APItude%20BookingAPI%20Swagger-PHP)

## How to Test

Unit tests in this SDK can be run using PHPUnit. 

1. First install the dependencies using composer including the `require-dev` dependencies.
2. Run `vendor\bin\phpunit --verbose` from commandline to execute tests. If you have 
   installed PHPUnit globally, run tests using `phpunit --verbose` instead.

You can change the PHPUnit test configuration in the `phpunit.xml` file.

## Initialization

### 

API client can be initialized as following.

```php

$client = new APItudeBookingAPISwaggerLib\APItudeBookingAPISwaggerClient();
```


# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [PostBookingOperationsController](#post_booking_operations_controller)
* [BookingController](#booking_controller)
* [CheckRateController](#check_rate_controller)
* [AvailabilityController](#availability_controller)
* [MiscController](#misc_controller)

## <a name="post_booking_operations_controller"></a>![Class: ](https://apidocs.io/img/class.png ".PostBookingOperationsController") PostBookingOperationsController

### Get singleton instance

The singleton instance of the ``` PostBookingOperationsController ``` class can be accessed from the API Client.

```php
$postBookingOperations = $client->getPostBookingOperations();
```

### <a name="get_booking_list"></a>![Method: ](https://apidocs.io/img/method.png ".PostBookingOperationsController.getBookingList") getBookingList

> *Tags:*  ``` Skips Authentication ``` 

> BookingList


```php
function getBookingList(
        $start,
        $end,
        $filterType,
        $status,
        $from,
        $to,
        $accept,
        $apiKey,
        $xSignature)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| start |  ``` Required ```  | TODO: Add a parameter description |
| end |  ``` Required ```  | TODO: Add a parameter description |
| filterType |  ``` Required ```  | TODO: Add a parameter description |
| status |  ``` Required ```  | TODO: Add a parameter description |
| from |  ``` Required ```  | TODO: Add a parameter description |
| to |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |
| apiKey |  ``` Required ```  | TODO: Add a parameter description |
| xSignature |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$start = 2017-08-15;
$end = 2017-09-10;
$filterType = 'CREATION';
$status = 'ALL';
$from = 1;
$to = 25;
$accept = 'application/json';
$apiKey = '{{Api-key}}';
$xSignature = '{{X-Signature}}';

$postBookingOperations->getBookingList($start, $end, $filterType, $status, $from, $to, $accept, $apiKey, $xSignature);

```


### <a name="delete_booking_cancellation"></a>![Method: ](https://apidocs.io/img/method.png ".PostBookingOperationsController.deleteBookingCancellation") deleteBookingCancellation

> *Tags:*  ``` Skips Authentication ``` 

> BookingCancellation


```php
function deleteBookingCancellation(
        $cancellationFlag,
        $language,
        $accept,
        $apiKey,
        $xSignature,
        $bookingReference)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| cancellationFlag |  ``` Required ```  | TODO: Add a parameter description |
| language |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |
| apiKey |  ``` Required ```  | TODO: Add a parameter description |
| xSignature |  ``` Required ```  | TODO: Add a parameter description |
| bookingReference |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$cancellationFlag = 'cancellationFlag';
$language = 'language';
$accept = 'Accept';
$apiKey = 'Api-key';
$xSignature = 'X-Signature';
$bookingReference = 'booking_reference';

$postBookingOperations->deleteBookingCancellation($cancellationFlag, $language, $accept, $apiKey, $xSignature, $bookingReference);

```


### <a name="update_booking_change"></a>![Method: ](https://apidocs.io/img/method.png ".PostBookingOperationsController.updateBookingChange") updateBookingChange

> *Tags:*  ``` Skips Authentication ``` 

> BookingChange


```php
function updateBookingChange(
        $body,
        $accept,
        $apiKey,
        $xSignature,
        $contentType,
        $acceptEncoding,
        $bookingReference)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |
| apiKey |  ``` Required ```  | TODO: Add a parameter description |
| xSignature |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| acceptEncoding |  ``` Required ```  | TODO: Add a parameter description |
| bookingReference |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new BookingChangeRequest();
$accept = 'Accept';
$apiKey = 'Api-key';
$xSignature = 'X-Signature';
$contentType = 'Content-Type';
$acceptEncoding = 'Accept-Encoding';
$bookingReference = 'booking_reference';

$result = $postBookingOperations->updateBookingChange($body, $accept, $apiKey, $xSignature, $contentType, $acceptEncoding, $bookingReference);

```


### <a name="get_booking_detail"></a>![Method: ](https://apidocs.io/img/method.png ".PostBookingOperationsController.getBookingDetail") getBookingDetail

> *Tags:*  ``` Skips Authentication ``` 

> BookingDetail


```php
function getBookingDetail(
        $accept,
        $apiKey,
        $xSignature,
        $bookingReference)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| accept |  ``` Required ```  | TODO: Add a parameter description |
| apiKey |  ``` Required ```  | TODO: Add a parameter description |
| xSignature |  ``` Required ```  | TODO: Add a parameter description |
| bookingReference |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$accept = 'Accept';
$apiKey = 'Api-key';
$xSignature = 'X-Signature';
$bookingReference = 'booking_reference';

$postBookingOperations->getBookingDetail($accept, $apiKey, $xSignature, $bookingReference);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="booking_controller"></a>![Class: ](https://apidocs.io/img/class.png ".BookingController") BookingController

### Get singleton instance

The singleton instance of the ``` BookingController ``` class can be accessed from the API Client.

```php
$booking = $client->getBooking();
```

### <a name="create_booking"></a>![Method: ](https://apidocs.io/img/method.png ".BookingController.createBooking") createBooking

> *Tags:*  ``` Skips Authentication ``` 

> Booking


```php
function createBooking(
        $body,
        $accept,
        $apiKey,
        $xSignature,
        $contentType,
        $acceptEncoding)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |
| apiKey |  ``` Required ```  | TODO: Add a parameter description |
| xSignature |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| acceptEncoding |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$bodyValue = "{\n  \"holder\": {\n    \"name\": \"IntegrationTestFirstName\",\n    \"surname\": \"IntegrationTestLastName\"\n  },\n  \"rooms\": [{\n    \"rateKey\": \"20171115|20171120|W|52|1|DBL.ST|ID_B2B_25|RO|EM4TIES|1~1~0||N@1884739731\",\n    \"paxes\": [{\n      \"roomId\": \"1\",\n      \"type\": \"AD\",\n      \"name\": \"Adult Name\"\n    }]\n  }],\n  \"clientReference\": \"IntegrationAgency\"\n}";
$body = APIHelper::deserialize($bodyValue);
$accept = 'application/json';
$apiKey = '{{Api-key}}';
$xSignature = '{{X-Signature}}';
$contentType = 'application/json';
$acceptEncoding = 'gzip';

$result = $booking->createBooking($body, $accept, $apiKey, $xSignature, $contentType, $acceptEncoding);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="check_rate_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CheckRateController") CheckRateController

### Get singleton instance

The singleton instance of the ``` CheckRateController ``` class can be accessed from the API Client.

```php
$checkRate = $client->getCheckRate();
```

### <a name="create_check_rate"></a>![Method: ](https://apidocs.io/img/method.png ".CheckRateController.createCheckRate") createCheckRate

> *Tags:*  ``` Skips Authentication ``` 

> CheckRate


```php
function createCheckRate(
        $body,
        $accept,
        $apiKey,
        $xSignature,
        $contentType,
        $acceptEncoding)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |
| apiKey |  ``` Required ```  | TODO: Add a parameter description |
| xSignature |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| acceptEncoding |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$bodyValue = "{\n  \"rooms\": [{\n    \"rateKey\": \"20171115|20171120|W|52|1|SGL.ST|CG-EXT LONG RO|RO||1~1~0||N@A8921A639A0D46D88735806D109FA6E81544\"\n  }]\n}";
$body = APIHelper::deserialize($bodyValue);
$accept = 'application/json';
$apiKey = '{{Api-key}}';
$xSignature = '{{X-Signature}}';
$contentType = 'application/json';
$acceptEncoding = 'gzip';

$result = $checkRate->createCheckRate($body, $accept, $apiKey, $xSignature, $contentType, $acceptEncoding);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="availability_controller"></a>![Class: ](https://apidocs.io/img/class.png ".AvailabilityController") AvailabilityController

### Get singleton instance

The singleton instance of the ``` AvailabilityController ``` class can be accessed from the API Client.

```php
$availability = $client->getAvailability();
```

### <a name="create_other_filters"></a>![Method: ](https://apidocs.io/img/method.png ".AvailabilityController.createOtherFilters") createOtherFilters

> *Tags:*  ``` Skips Authentication ``` 

> Other filters


```php
function createOtherFilters(
        $body,
        $accept,
        $apiKey,
        $xSignature,
        $contentType,
        $acceptEncoding)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |
| apiKey |  ``` Required ```  | TODO: Add a parameter description |
| xSignature |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| acceptEncoding |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$bodyValue = "{\n  \"stay\": {\n    \"checkIn\": \"2017-11-15\",\n    \"checkOut\": \"2017-11-20\",\n    \"shiftDays\": \"2\"\n  },\n  \"occupancies\": [{\n    \"rooms\": 1,\n    \"adults\": 1,\n    \"children\": 0\n  }],\n  \"hotels\": {\n    \"hotel\": [1,\n    271]\n  },\n  \"filter\": {\n    \"minRate\": 100.000,\n    \"maxRate\": 1700.000,\n    \"minCategory\": 3,\n    \"maxCategory\": 5,\n    \"maxRooms\":3,\n    \"maxRatesPerRoom\": 3,\n    \"paymentType\": \"AT_HOTEL\",\n    \"packaging\": true,\n    \"hotelPackage\": \"YES\",\n    \"contract\": \"CG-FIT B2B\"\n  }\n}";
$body = APIHelper::deserialize($bodyValue);
$accept = 'application/json';
$apiKey = '{{Api-key}}';
$xSignature = '{{X-Signature}}';
$contentType = 'application/json';
$acceptEncoding = 'gzip';

$result = $availability->createOtherFilters($body, $accept, $apiKey, $xSignature, $contentType, $acceptEncoding);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="misc_controller"></a>![Class: ](https://apidocs.io/img/class.png ".MiscController") MiscController

### Get singleton instance

The singleton instance of the ``` MiscController ``` class can be accessed from the API Client.

```php
$misc = $client->getMisc();
```

### <a name="get0_status"></a>![Method: ](https://apidocs.io/img/method.png ".MiscController.get0Status") get0Status

> *Tags:*  ``` Skips Authentication ``` 

> 0. Status


```php
function get0Status(
        $accept,
        $apiKey,
        $xSignature)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| accept |  ``` Required ```  | TODO: Add a parameter description |
| apiKey |  ``` Required ```  | TODO: Add a parameter description |
| xSignature |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$accept = 'application/json';
$apiKey = '{{Api-key}}';
$xSignature = '{{X-Signature}}';

$misc->get0Status($accept, $apiKey, $xSignature);

```


[Back to List of Controllers](#list_of_controllers)



