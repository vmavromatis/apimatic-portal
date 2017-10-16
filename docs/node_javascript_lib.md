# Getting started

APItude complete postman collection, with both BookingAPI & ContentAPI. You have the full details of our API in our developer portal:
https://developer.hotelbeds.com/docs?hotel

## How to Build

The generated SDK relies on [Node Package Manager](https://www.npmjs.com/) (NPM) being available to resolve dependencies. If you don't already have NPM installed, please go ahead and follow instructions to install NPM from [here](https://nodejs.org/en/download/).
The SDK also requires Node to be installed. If Node isn't already installed, please install it from [here](https://nodejs.org/en/download/)
> NPM is installed by default when Node is installed

To check if node and npm have been successfully installed, write the following commands in command prompt:

* `node --version`
* `npm -version`

![Version Check](https://apidocs.io/illustration/nodejs?step=versionCheck&workspaceFolder=APItude%20BookingAPI%20Swagger-Node)

Now use npm to resolve all dependencies by running the following command in the root directory (of the SDK folder):

```bash
npm install
```

![Resolve Dependencies](https://apidocs.io/illustration/nodejs?step=resolveDependency1&workspaceFolder=APItude%20BookingAPI%20Swagger-Node)

![Resolve Dependencies](https://apidocs.io/illustration/nodejs?step=resolveDependency2)

This will install all dependencies in the `node_modules` folder.

Once dependencies are resolved, you will need to move the folder `APItudeBookingAPISwaggerLib ` in to your `node_modules` folder.

## How to Use

The following section explains how to use the library in a new project.

### 1. Open Project Folder
Open an IDE/Text Editor for JavaScript like Sublime Text. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

Click on `File` and select `Open Folder`.

![Open Folder](https://apidocs.io/illustration/nodejs?step=openFolder)

Select the folder of your SDK and click on `Select Folder` to open it up in Sublime Text. The folder will become visible in the bar on the left.

![Open Project](https://apidocs.io/illustration/nodejs?step=openProject&workspaceFolder=APItude%20BookingAPI%20Swagger-Node)

### 2. Creating a Test File

Now right click on the folder name and select the `New File` option to create a new test file. Save it as `index.js` Now import the generated NodeJS library using the following lines of code:

```js
var lib = require('lib');
```

Save changes.

![Create new file](https://apidocs.io/illustration/nodejs?step=createNewFile&workspaceFolder=APItude%20BookingAPI%20Swagger-Node)

![Save new file](https://apidocs.io/illustration/nodejs?step=saveNewFile&workspaceFolder=APItude%20BookingAPI%20Swagger-Node)

### 3. Running The Test File

To run the `index.js` file, open up the command prompt and navigate to the Path where the SDK folder resides. Type the following command to run the file:

```
node index.js
```

![Run file](https://apidocs.io/illustration/nodejs?step=runProject&workspaceFolder=APItude%20BookingAPI%20Swagger-Node)


## How to Test

These tests use Mocha framework for testing, coupled with Chai for assertions. These dependencies need to be installed for tests to run.
Tests can be run in a number of ways:

### Method 1 (Run all tests)

1. Navigate to the root directory of the SDK folder from command prompt.
2. Type `mocha --recursive` to run all the tests.

### Method 2 (Run all tests)

1. Navigate to the `../test/Controllers/` directory from command prompt.
2. Type `mocha *` to run all the tests.

### Method 3 (Run specific controller's tests)

1. Navigate to the `../test/Controllers/` directory from command prompt.
2. Type `mocha  APItude BookingAPI SwaggerController`  to run all the tests in that controller file.

> To increase mocha's default timeout, you can change the `TEST_TIMEOUT` parameter's value in `TestBootstrap.js`.

![Run Tests](https://apidocs.io/illustration/nodejs?step=runTests&controllerName=APItude%20BookingAPI%20SwaggerController)

## Initialization

### 

API client can be initialized as following:

```JavaScript
const lib = require('lib');


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

```javascript
var controller = lib.PostBookingOperationsController;
```

### <a name="get_booking_list"></a>![Method: ](https://apidocs.io/img/method.png ".PostBookingOperationsController.getBookingList") getBookingList

> *Tags:*  ``` Skips Authentication ``` 

> BookingList


```javascript
function getBookingList(start, end, filterType, status, from, to, accept, apiKey, xSignature, callback)
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

```javascript

    var start = "2017-08-15";
    var end = "2017-09-10";
    var filterType = 'CREATION';
    var status = 'ALL';
    var from = 1;
    var to = 25;
    var accept = 'application/json';
    var apiKey = '{{Api-key}}';
    var xSignature = '{{X-Signature}}';

    controller.getBookingList(start, end, filterType, status, from, to, accept, apiKey, xSignature, function(error, response, context) {

    
    });
```



### <a name="delete_booking_cancellation"></a>![Method: ](https://apidocs.io/img/method.png ".PostBookingOperationsController.deleteBookingCancellation") deleteBookingCancellation

> *Tags:*  ``` Skips Authentication ``` 

> BookingCancellation


```javascript
function deleteBookingCancellation(cancellationFlag, language, accept, apiKey, xSignature, bookingReference, callback)
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

```javascript

    var cancellationFlag = 'cancellationFlag';
    var language = 'language';
    var accept = 'Accept';
    var apiKey = 'Api-key';
    var xSignature = 'X-Signature';
    var bookingReference = booking_reference;

    controller.deleteBookingCancellation(cancellationFlag, language, accept, apiKey, xSignature, bookingReference, function(error, response, context) {

    
    });
```



### <a name="update_booking_change"></a>![Method: ](https://apidocs.io/img/method.png ".PostBookingOperationsController.updateBookingChange") updateBookingChange

> *Tags:*  ``` Skips Authentication ``` 

> BookingChange


```javascript
function updateBookingChange(body, accept, apiKey, xSignature, contentType, acceptEncoding, bookingReference, callback)
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

```javascript

    var body = new BookingChangeRequest({"key":"value"});
    var accept = 'Accept';
    var apiKey = 'Api-key';
    var xSignature = 'X-Signature';
    var contentType = 'Content-Type';
    var acceptEncoding = 'Accept-Encoding';
    var bookingReference = booking_reference;

    controller.updateBookingChange(body, accept, apiKey, xSignature, contentType, acceptEncoding, bookingReference, function(error, response, context) {

    
    });
```



### <a name="get_booking_detail"></a>![Method: ](https://apidocs.io/img/method.png ".PostBookingOperationsController.getBookingDetail") getBookingDetail

> *Tags:*  ``` Skips Authentication ``` 

> BookingDetail


```javascript
function getBookingDetail(accept, apiKey, xSignature, bookingReference, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| accept |  ``` Required ```  | TODO: Add a parameter description |
| apiKey |  ``` Required ```  | TODO: Add a parameter description |
| xSignature |  ``` Required ```  | TODO: Add a parameter description |
| bookingReference |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var accept = 'Accept';
    var apiKey = 'Api-key';
    var xSignature = 'X-Signature';
    var bookingReference = booking_reference;

    controller.getBookingDetail(accept, apiKey, xSignature, bookingReference, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="booking_controller"></a>![Class: ](https://apidocs.io/img/class.png ".BookingController") BookingController

### Get singleton instance

The singleton instance of the ``` BookingController ``` class can be accessed from the API Client.

```javascript
var controller = lib.BookingController;
```

### <a name="create_booking"></a>![Method: ](https://apidocs.io/img/method.png ".BookingController.createBooking") createBooking

> *Tags:*  ``` Skips Authentication ``` 

> Booking


```javascript
function createBooking(body, accept, apiKey, xSignature, contentType, acceptEncoding, callback)
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

```javascript

    var body = new BookingRequest({
  "holder": {
    "name": "IntegrationTestFirstName",
    "surname": "IntegrationTestLastName"
  },
  "rooms": [{
    "rateKey": "20171115|20171120|W|52|1|DBL.ST|ID_B2B_25|RO|EM4TIES|1~1~0||N@1884739731",
    "paxes": [{
      "roomId": "1",
      "type": "AD",
      "name": "Adult Name"
    }]
  }],
  "clientReference": "IntegrationAgency"
});
    var accept = 'application/json';
    var apiKey = '{{Api-key}}';
    var xSignature = '{{X-Signature}}';
    var contentType = 'application/json';
    var acceptEncoding = 'gzip';

    controller.createBooking(body, accept, apiKey, xSignature, contentType, acceptEncoding, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="check_rate_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CheckRateController") CheckRateController

### Get singleton instance

The singleton instance of the ``` CheckRateController ``` class can be accessed from the API Client.

```javascript
var controller = lib.CheckRateController;
```

### <a name="create_check_rate"></a>![Method: ](https://apidocs.io/img/method.png ".CheckRateController.createCheckRate") createCheckRate

> *Tags:*  ``` Skips Authentication ``` 

> CheckRate


```javascript
function createCheckRate(body, accept, apiKey, xSignature, contentType, acceptEncoding, callback)
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

```javascript

    var body = new CheckRateRequest({
  "rooms": [{
    "rateKey": "20171115|20171120|W|52|1|SGL.ST|CG-EXT LONG RO|RO||1~1~0||N@A8921A639A0D46D88735806D109FA6E81544"
  }]
});
    var accept = 'application/json';
    var apiKey = '{{Api-key}}';
    var xSignature = '{{X-Signature}}';
    var contentType = 'application/json';
    var acceptEncoding = 'gzip';

    controller.createCheckRate(body, accept, apiKey, xSignature, contentType, acceptEncoding, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="availability_controller"></a>![Class: ](https://apidocs.io/img/class.png ".AvailabilityController") AvailabilityController

### Get singleton instance

The singleton instance of the ``` AvailabilityController ``` class can be accessed from the API Client.

```javascript
var controller = lib.AvailabilityController;
```

### <a name="create_other_filters"></a>![Method: ](https://apidocs.io/img/method.png ".AvailabilityController.createOtherFilters") createOtherFilters

> *Tags:*  ``` Skips Authentication ``` 

> Other filters


```javascript
function createOtherFilters(body, accept, apiKey, xSignature, contentType, acceptEncoding, callback)
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

```javascript

    var body = new OtherFiltersRequest({
  "stay": {
    "checkIn": "2017-11-15",
    "checkOut": "2017-11-20",
    "shiftDays": "2"
  },
  "occupancies": [{
    "rooms": 1,
    "adults": 1,
    "children": 0
  }],
  "hotels": {
    "hotel": [1,
    271]
  },
  "filter": {
    "minRate": 100.000,
    "maxRate": 1700.000,
    "minCategory": 3,
    "maxCategory": 5,
    "maxRooms":3,
    "maxRatesPerRoom": 3,
    "paymentType": "AT_HOTEL",
    "packaging": true,
    "hotelPackage": "YES",
    "contract": "CG-FIT B2B"
  }
});
    var accept = 'application/json';
    var apiKey = '{{Api-key}}';
    var xSignature = '{{X-Signature}}';
    var contentType = 'application/json';
    var acceptEncoding = 'gzip';

    controller.createOtherFilters(body, accept, apiKey, xSignature, contentType, acceptEncoding, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="misc_controller"></a>![Class: ](https://apidocs.io/img/class.png ".MiscController") MiscController

### Get singleton instance

The singleton instance of the ``` MiscController ``` class can be accessed from the API Client.

```javascript
var controller = lib.MiscController;
```

### <a name="get0_status"></a>![Method: ](https://apidocs.io/img/method.png ".MiscController.get0Status") get0Status

> *Tags:*  ``` Skips Authentication ``` 

> 0. Status


```javascript
function get0Status(accept, apiKey, xSignature, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| accept |  ``` Required ```  | TODO: Add a parameter description |
| apiKey |  ``` Required ```  | TODO: Add a parameter description |
| xSignature |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var accept = 'application/json';
    var apiKey = '{{Api-key}}';
    var xSignature = '{{X-Signature}}';

    controller.get0Status(accept, apiKey, xSignature, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)



