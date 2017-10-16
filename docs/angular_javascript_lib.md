# Getting started

APItude complete postman collection, with both BookingAPI & ContentAPI. You have the full details of our API in our developer portal:
https://developer.hotelbeds.com/docs?hotel

## How to Build

The generated SDK requires AngularJS framework to work. If you do not already have angular downloaded, please go ahead and do it from [here](https://angularjs.org/).
If any of your models have `Date` or `Datetime` type fields or your endpoints have `Date`/`Datetime` type response, you will need to download and link [angular-moment](https://cdnjs.cloudflare.com/ajax/libs/angular-moment/1.0.1/angular-moment.min.js) and [moment.js](https://cdnjs.cloudflare.com/ajax/libs/moment.js/2.17.1/moment.min.js) with your project.

## How to Use

The following section describes how to use the generated SDK in an existing/new project.

### 1. Configure Angular and Generated SDK
Perform the following steps to configure angular and the SDK:
+ Make a `scripts` folder inside the root folder of the project. If you already have a `scripts` folder, skip to the next step.
+ Move the `angular.min.js` file inside the scripts folder. 
+ Move the `APItudeBookingAPISwaggerLib` folder inside the scripts folder.
+ If any of the Custom Types in your API have `Date`/`Datetime` type fields or any endpoint has `Date`/`Datetime` response, you will need to download angular-moment and moment.js. Move these 2 files into the `scripts` folder as well.

![folder-structure-image](https://apidocs.io/illustration/angularjs?step=folderStructure&workspaceFolder=APItude%20BookingAPI%20Swagger-Angular&projectName=APItudeBookingAPISwaggerLib)

### 2. Open Project Folder
Open an IDE/Text Editor for JavaScript like Sublime Text. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.  
Click on `File` and select `Open Folder`

Select the folder of your SDK and click on `Select Folder` to open it up in Sublime Text. The folder will become visible in the bar on the left.

![open-folder-image](https://apidocs.io/illustration/angularjs?step=openFolder&workspaceFolder=APItude%20BookingAPI%20Swagger-Angular)

### 3. Create an Angular Application
Since Angular JS is used for client-side web development, in order to use the generated library, you will have to develop an application first.
If you already have an angular application, [skip to Step 6](#6-include-sdk-references-in-html-file). Otherwise, follow these steps to create one:

+ In the IDE, click on `File` and choose `New File` to create a new file.
+ Add the following starting code in the file:
```js
var app = angular.module('myApp', []);
app.controller('testController', function($scope) 
{

});
```
+ Save it with the name `app.js` in the `scripts` folder.


### 4. Create HTML File
Skip to the next step if you are working with an existing project and already have an html file. Otherwise follow the steps to create one:
+ Inside the IDE, right click on the project folder name and select the `New File` option to create a new test file.
+ Save it with an appropriate name such as `index.html` in the root of your project folder.
`index.html` should look like this:
```html
<!DOCTYPE html>
<html>
<head>
	<title>Angular Project</title>
	<script></script>
</head>

<body>
</body>

</html>
```

![initial-html-code-image](https://apidocs.io/illustration/angularjs?step=initialCode&workspaceFolder=APItude%20BookingAPI%20Swagger-Angular)

### 5. Including links to Angular in HTML file
Your HTML file needs to have a link to `angular.min.js` file to use Angular-JS. Add the link using `script` tags inside the `head` section of `index.html` like:
```html
<script src="scripts/angular.min.js" ></script>
```
If any of the Custom Types that you have defined have `Date`/`Datetime` type fields or any endpoint has `Date`/`Datetime` response, you will also need to link to angular-moment and moment.js like:
```html
<script src="scripts/angular.min.js" ></script>
<script src="scripts/moment.min.js" ></script>
<script src="scripts/angular-moment.min.js" ></script>
```

### 6. Include SDK references in HTML file
Import the reference to the generated SDK files inside your html file like:
```html
<head>
    ...
    <!-- Helper files -->
    <script src="scripts/APItudeBookingAPISwaggerLib/Module.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Configuration.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/ModelFactory.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/ObjectMapper.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/APIHelper.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Http/Client/HttpContext.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Http/Client/RequestClient.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Http/Request/HttpRequest.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Http/Response/HttpResponse.js"></script>

    <!-- API Controllers -->
    <script src="scripts/APItudeBookingAPISwaggerLib/Controllers/BaseController.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Controllers/PostBookingOperationsController.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Controllers/BookingController.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Controllers/CheckRateController.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Controllers/AvailabilityController.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Controllers/MiscController.js"></script>


    <!-- Models -->
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/BaseModel.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/BookingChangeResponse.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Hotel108.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Booking105.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/BookingChangeRequest.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Rate101.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Hotel98.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Booking.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/BookingResponse.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Rate84.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Hotel.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/CheckRateResponse.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Hotels74.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Filter.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Rate63.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Hotels61.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Hotels30.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/AvailabilityByGeolocationResponse.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Hotels19.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/AvailabilityByDestinationResponse.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Rate.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Supplier.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Paxis100.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/ModificationPolicies.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Paxis.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Rooms91.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Holder.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/RateDiscount.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Hotels7.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Rooms83.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/CheckRateRequest.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Rooms75.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Rooms62.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Boards.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Rooms.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Room31.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Room20.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Stay13.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Offer.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/CancellationPolicy.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Room.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Occupancy.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Stay.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/AvailabilityByHotelCodeRequest.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/RateBreakDown.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Rooms79.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Keywords.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Destination.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Hotels.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/FilterByAccommodationTypeRequest.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/FilterByKeywordRequest.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/FilterByRoomTypeRequest.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Rate32.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Hotels29.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Geolocation.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/AvailabilityByGeolocationRequest.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/ShiftRate.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Rate21.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Hotels18.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/AvailabilityByDestinationRequest.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Hotels6.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/AuditData.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/AvailabilityByHotelCodeResponse.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Review.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/FilterByReviewRatingRequest.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/FilterByBoardCodeRequest.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Paxis110.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Rooms109.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Rooms99.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/BookingRequest.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Hotels73.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/OtherFiltersResponse.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/OtherFiltersRequest.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/Hotels60.js"></script>
    <script src="scripts/APItudeBookingAPISwaggerLib/Models/FilterByReviewRatingResponse.js"></script>

    ...
</head>
```
> The `Module.js` file should be imported before the other files. After `Module.js`, `Configuration.js` should be imported.
> The `ModelFactory.js` file is needed by `ObjectMapper.js` file. The `ObjectMapper` in turn, is needed by `BaseController.js`.

### 7. Including link to `app.js` in HTML file
Link your `app.js` file to your `index.html` file like:
```html
<head>
	...
	<script src="scripts/app.js"></script>
</head>
```
> The link to app.js needs to be included at the very end of the head tag, after the SDK references have been added

### 8. Initializing the Angular App
You need to initialize your app and the controller associated with your view inside your `index.html` file. Do so like:
+ Add ng-app directive to initialize your app inside the `body` tag.
```html
<body ng-app="myApp">
```
+ Add ng-controller directive to initialize your controller and bind it with your view (`index.html` file).
```html
...
<body ng-app="myApp">
	<div ng-controller="testController">
		...
	</div>
	...
</body>
...
```

### 9. Consuming the SDK 
In order to use the generated SDK's modules, controllers and factories, the project needs to be added as a dependency in your angular app's module. This will be done inside the `app.js` file.
Add the dependency like this:

```js
var app = angular.module('myApp', ['APItudeBookingAPISwaggerLib']);
```
At this point, the SDK has been successfully included in your project. Further steps include using a service/factory from the generated SDK. To see working example of this, please head on [over here](#list-of-controllers) and choose any class to see its functions and example usage.  

### 10. Running The App
To run the app, simply open up the `index.html` file in a browser.

![app-running](https://apidocs.io/illustration/angularjs?step=appRunning)

## Initialization


The Angular Application can be initialized as following:
```JavaScript
var app = angular.module('myApp', [APItudeBookingAPISwaggerLib]);
// now controllers/services can be created which import
// the factories provided by the sdk
```
### 




# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [PostBookingOperationsController](#post_booking_operations_controller)
* [BookingController](#booking_controller)
* [CheckRateController](#check_rate_controller)
* [AvailabilityController](#availability_controller)
* [MiscController](#misc_controller)

## <a name="post_booking_operations_controller"></a>![Class: ](https://apidocs.io/img/class.png ".PostBookingOperationsController") PostBookingOperationsController

### Get singleton instance

The singleton instance of the ``` PostBookingOperationsController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, PostBookingOperationsController, BookingChangeResponse){
	});
```

### <a name="get_booking_list"></a>![Method: ](https://apidocs.io/img/method.png ".PostBookingOperationsController.getBookingList") getBookingList

> *Tags:*  ``` Skips Authentication ``` 

> BookingList


```javascript
function getBookingList(start, end, filterType, status, from, to, accept, apiKey, xSignature)
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


	app.controller("testController", function($scope, PostBookingOperationsController){
        var start = '2017-08-15';
        var end = '2017-09-10';
        var filterType = 'CREATION';
        var status = 'ALL';
        var from = 1;
        var to = 25;
        var accept = 'application/json';
        var apiKey = '{{Api-key}}';
        var xSignature = '{{X-Signature}}';


		var result = PostBookingOperationsController.getBookingList(start, end, filterType, status, from, to, accept, apiKey, xSignature);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="delete_booking_cancellation"></a>![Method: ](https://apidocs.io/img/method.png ".PostBookingOperationsController.deleteBookingCancellation") deleteBookingCancellation

> *Tags:*  ``` Skips Authentication ``` 

> BookingCancellation


```javascript
function deleteBookingCancellation(cancellationFlag, language, accept, apiKey, xSignature, bookingReference)
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


	app.controller("testController", function($scope, PostBookingOperationsController){
        var cancellationFlag = 'cancellationFlag';
        var language = 'language';
        var accept = 'Accept';
        var apiKey = 'Api-key';
        var xSignature = 'X-Signature';
        var bookingReference = booking_reference;


		var result = PostBookingOperationsController.deleteBookingCancellation(cancellationFlag, language, accept, apiKey, xSignature, bookingReference);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="update_booking_change"></a>![Method: ](https://apidocs.io/img/method.png ".PostBookingOperationsController.updateBookingChange") updateBookingChange

> *Tags:*  ``` Skips Authentication ``` 

> BookingChange


```javascript
function updateBookingChange(body, accept, apiKey, xSignature, contentType, acceptEncoding, bookingReference)
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


	app.controller("testController", function($scope, PostBookingOperationsController, BookingChangeResponse){
        var body = new BookingChangeRequest({"key":"value"});
        var accept = 'Accept';
        var apiKey = 'Api-key';
        var xSignature = 'X-Signature';
        var contentType = 'Content-Type';
        var acceptEncoding = 'Accept-Encoding';
        var bookingReference = booking_reference;


		var result = PostBookingOperationsController.updateBookingChange(body, accept, apiKey, xSignature, contentType, acceptEncoding, bookingReference);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="get_booking_detail"></a>![Method: ](https://apidocs.io/img/method.png ".PostBookingOperationsController.getBookingDetail") getBookingDetail

> *Tags:*  ``` Skips Authentication ``` 

> BookingDetail


```javascript
function getBookingDetail(accept, apiKey, xSignature, bookingReference)
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


	app.controller("testController", function($scope, PostBookingOperationsController){
        var accept = 'Accept';
        var apiKey = 'Api-key';
        var xSignature = 'X-Signature';
        var bookingReference = booking_reference;


		var result = PostBookingOperationsController.getBookingDetail(accept, apiKey, xSignature, bookingReference);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="booking_controller"></a>![Class: ](https://apidocs.io/img/class.png ".BookingController") BookingController

### Get singleton instance

The singleton instance of the ``` BookingController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, BookingController, BookingResponse){
	});
```

### <a name="create_booking"></a>![Method: ](https://apidocs.io/img/method.png ".BookingController.createBooking") createBooking

> *Tags:*  ``` Skips Authentication ``` 

> Booking


```javascript
function createBooking(body, accept, apiKey, xSignature, contentType, acceptEncoding)
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


	app.controller("testController", function($scope, BookingController, BookingResponse){
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


		var result = BookingController.createBooking(body, accept, apiKey, xSignature, contentType, acceptEncoding);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="check_rate_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CheckRateController") CheckRateController

### Get singleton instance

The singleton instance of the ``` CheckRateController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, CheckRateController, CheckRateResponse){
	});
```

### <a name="create_check_rate"></a>![Method: ](https://apidocs.io/img/method.png ".CheckRateController.createCheckRate") createCheckRate

> *Tags:*  ``` Skips Authentication ``` 

> CheckRate


```javascript
function createCheckRate(body, accept, apiKey, xSignature, contentType, acceptEncoding)
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


	app.controller("testController", function($scope, CheckRateController, CheckRateResponse){
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


		var result = CheckRateController.createCheckRate(body, accept, apiKey, xSignature, contentType, acceptEncoding);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="availability_controller"></a>![Class: ](https://apidocs.io/img/class.png ".AvailabilityController") AvailabilityController

### Get singleton instance

The singleton instance of the ``` AvailabilityController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, AvailabilityController, OtherFiltersResponse){
	});
```

### <a name="create_other_filters"></a>![Method: ](https://apidocs.io/img/method.png ".AvailabilityController.createOtherFilters") createOtherFilters

> *Tags:*  ``` Skips Authentication ``` 

> Other filters


```javascript
function createOtherFilters(body, accept, apiKey, xSignature, contentType, acceptEncoding)
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


	app.controller("testController", function($scope, AvailabilityController, OtherFiltersResponse){
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


		var result = AvailabilityController.createOtherFilters(body, accept, apiKey, xSignature, contentType, acceptEncoding);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="misc_controller"></a>![Class: ](https://apidocs.io/img/class.png ".MiscController") MiscController

### Get singleton instance

The singleton instance of the ``` MiscController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, MiscController){
	});
```

### <a name="get0_status"></a>![Method: ](https://apidocs.io/img/method.png ".MiscController.get0Status") get0Status

> *Tags:*  ``` Skips Authentication ``` 

> 0. Status


```javascript
function get0Status(accept, apiKey, xSignature)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| accept |  ``` Required ```  | TODO: Add a parameter description |
| apiKey |  ``` Required ```  | TODO: Add a parameter description |
| xSignature |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, MiscController){
        var accept = 'application/json';
        var apiKey = '{{Api-key}}';
        var xSignature = '{{X-Signature}}';


		var result = MiscController.get0Status(accept, apiKey, xSignature);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)



