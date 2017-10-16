# Getting started

APItude complete postman collection, with both BookingAPI & ContentAPI. You have the full details of our API in our developer portal:
https://developer.hotelbeds.com/docs?hotel

## How to Build


The generated code has dependencies over external libraries like UniRest. These dependencies are defined in the ```PodFile``` file that comes with the SDK. 
To resolve these dependencies, we use the Cocoapods package manager.
Visit https://guides.cocoapods.org/using/getting-started.html to setup Cocoapods on your system.
Open command prompt and type ```pod --version```. This should display the current version of Cocoapods installed if the installation was successful.

Using command line, navigate to the directory containing the generated files (including ```PodFile```) for the SDK. 
Run the command ```pod install```. This should install all the required dependencies and create the ```pods``` directory in your project directory.

![Installing dependencies using Cocoapods](https://apidocs.io/illustration/objc?step=AddDependencies&workspaceFolder=APItude%20BookingAPI%20Swagger-ObjC&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwagger&rootNamespace=APItudeBookingAPISwagger)

Open the project workspace using the (APItudeBookingAPISwagger.xcworkspace) file. Invoke the build process using `Command(⌘)+B` shortcut key or using the `Build` menu as shown below.

![Building SDK using Xcode](https://apidocs.io/illustration/objc?step=BuildSDK&workspaceFolder=APItude%20BookingAPI%20Swagger-ObjC&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwagger&rootNamespace=APItudeBookingAPISwagger)


## How to Use

The generated code is a Cocoa Touch Static Library which can be used in any iOS project. The support for these generated libraries go all the way back to iOS 6.

The following section explains how to use the APItudeBookingAPISwagger library in a new iOS project.     
### 1. Starting a new project
To start a new project, left-click on the ```Create a new Xcode project```.
![Create Test Project - Step 1](https://apidocs.io/illustration/objc?step=Test1&workspaceFolder=APItude%20BookingAPI%20Swagger-ObjC&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwagger&rootNamespace=APItudeBookingAPISwagger)

Next, choose **Single View Application** and click ```Next```.
![Create Test Project - Step 2](https://apidocs.io/illustration/objc?step=Test2&workspaceFolder=APItude%20BookingAPI%20Swagger-ObjC&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwagger&rootNamespace=APItudeBookingAPISwagger)

Provide **Test-Project** as the product name click ```Next```.
![Create Test Project - Step 3](https://apidocs.io/illustration/objc?step=Test3&workspaceFolder=APItude%20BookingAPI%20Swagger-ObjC&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwagger&rootNamespace=APItudeBookingAPISwagger)

Choose the desired location of your project folder and click ```Create```.
![Create Test Project - Step 4](https://apidocs.io/illustration/objc?step=Test4&workspaceFolder=APItude%20BookingAPI%20Swagger-ObjC&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwagger&rootNamespace=APItudeBookingAPISwagger)

### 2. Adding the static library dependency
To add this dependency open a terminal and navigate to your project folder. Next, input ```pod init``` and press enter.
![Add dependency - Step 1](https://apidocs.io/illustration/objc?step=Add0&workspaceFolder=APItude%20BookingAPI%20Swagger-ObjC&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwagger&rootNamespace=APItudeBookingAPISwagger)

Next, open the newly created ```PodFile``` in your favourite text editor. Add the following line : pod 'APItudeBookingAPISwagger', :path => 'Vendor/APItudeBookingAPISwagger'
![Add dependency - Step 2](https://apidocs.io/illustration/objc?step=Add1&workspaceFolder=APItude%20BookingAPI%20Swagger-ObjC&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwagger&rootNamespace=APItudeBookingAPISwagger)

Execute `pod install` from terminal to install the dependecy in your project. This would add the dependency to the newly created test project.
![Add dependency - Step 3](https://apidocs.io/illustration/objc?step=Add2&workspaceFolder=APItude%20BookingAPI%20Swagger-ObjC&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwagger&rootNamespace=APItudeBookingAPISwagger)


## How to Test

Unit tests in this SDK can be run using Xcode. 

First build the SDK as shown in the steps above and naivgate to the project directory and open the APItudeBookingAPISwagger.xcworkspace file.

Go to the test explorer in Xcode as shown in the picture below and click on `run tests` from the menu. 
![Run tests](https://apidocs.io/illustration/objc?step=RunTests&workspaceFolder=APItude%20BookingAPI%20Swagger-ObjC&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwagger&rootNamespace=APItudeBookingAPISwagger)


## Initialization

### 

Configuration variables can be set as following.
```Objc

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
```objc
PostBookingOperations* postBookingOperations = [[PostBookingOperations alloc]init] ;
```

### <a name="get_booking_list_async_with_start"></a>![Method: ](https://apidocs.io/img/method.png ".PostBookingOperationsController.getBookingListAsyncWithStart") getBookingListAsyncWithStart

> *Tags:*  ``` Skips Authentication ``` 

> BookingList


```objc
function getBookingListAsyncWithStart:(NSDate*) start
                mend:(NSDate*) mend
                filterType:(NSString*) filterType
                status:(NSString*) status
                from:(int) from
                to:(int) to
                accept:(NSString*) accept
                apiKey:(NSString*) apiKey
                xSignature:(NSString*) xSignature
                completionBlock:(CompletedGetBookingList) onCompleted(start mend : mend filterType : filterType status : status from : from to : to accept : accept apiKey : apiKey xSignature : xSignature)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| start |  ``` Required ```  | TODO: Add a parameter description |
| mend |  ``` Required ```  | TODO: Add a parameter description |
| filterType |  ``` Required ```  | TODO: Add a parameter description |
| status |  ``` Required ```  | TODO: Add a parameter description |
| from |  ``` Required ```  | TODO: Add a parameter description |
| to |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |
| apiKey |  ``` Required ```  | TODO: Add a parameter description |
| xSignature |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSDate* start = [NSDate NSDateFromNSString: @"2017-08-15"];
    NSDate* mend = [NSDate NSDateFromNSString: @"2017-09-10"];
    NSString* filterType = @"CREATION";
    NSString* status = @"ALL";
    int from = [@"1" intValue];
    int to = [@"25" intValue];
    NSString* accept = @"application/json";
    NSString* apiKey = @"{{Api-key}}";
    NSString* xSignature = @"{{X-Signature}}";

    [self.postBookingOperations getBookingListAsyncWithStart: start mend : mend filterType : filterType status : status from : from to : to accept : accept apiKey : apiKey xSignature : xSignature  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="delete_booking_cancellation_async_with_cancellation_flag"></a>![Method: ](https://apidocs.io/img/method.png ".PostBookingOperationsController.deleteBookingCancellationAsyncWithCancellationFlag") deleteBookingCancellationAsyncWithCancellationFlag

> *Tags:*  ``` Skips Authentication ``` 

> BookingCancellation


```objc
function deleteBookingCancellationAsyncWithCancellationFlag:(NSString*) cancellationFlag
                language:(NSString*) language
                accept:(NSString*) accept
                apiKey:(NSString*) apiKey
                xSignature:(NSString*) xSignature
                bookingReference:(NSString*) bookingReference
                completionBlock:(CompletedDeleteBookingCancellation) onCompleted(cancellationFlag language : language accept : accept apiKey : apiKey xSignature : xSignature bookingReference : bookingReference)
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

```objc
    // Parameters for the API call
    NSString* cancellationFlag = @"cancellationFlag";
    NSString* language = @"language";
    NSString* accept = @"Accept";
    NSString* apiKey = @"Api-key";
    NSString* xSignature = @"X-Signature";
    NSString* bookingReference = @"booking_reference";

    [self.postBookingOperations deleteBookingCancellationAsyncWithCancellationFlag: cancellationFlag language : language accept : accept apiKey : apiKey xSignature : xSignature bookingReference : bookingReference  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="update_booking_change_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".PostBookingOperationsController.updateBookingChangeAsyncWithBody") updateBookingChangeAsyncWithBody

> *Tags:*  ``` Skips Authentication ``` 

> BookingChange


```objc
function updateBookingChangeAsyncWithBody:(BookingChangeRequest*) body
                accept:(NSString*) accept
                apiKey:(NSString*) apiKey
                xSignature:(NSString*) xSignature
                contentType:(NSString*) contentType
                acceptEncoding:(NSString*) acceptEncoding
                bookingReference:(NSString*) bookingReference
                completionBlock:(CompletedPutBookingChange) onCompleted(body accept : accept apiKey : apiKey xSignature : xSignature contentType : contentType acceptEncoding : acceptEncoding bookingReference : bookingReference)
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

```objc
    // Parameters for the API call
    BookingChangeRequest* body = [[BookingChangeRequest alloc]init];
    NSString* accept = @"Accept";
    NSString* apiKey = @"Api-key";
    NSString* xSignature = @"X-Signature";
    NSString* contentType = @"Content-Type";
    NSString* acceptEncoding = @"Accept-Encoding";
    NSString* bookingReference = @"booking_reference";

    [self.postBookingOperations updateBookingChangeAsyncWithBody: body accept : accept apiKey : apiKey xSignature : xSignature contentType : contentType acceptEncoding : acceptEncoding bookingReference : bookingReference  completionBlock:^(BOOL success, HttpContext* context, BookingChangeResponse* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_booking_detail_async_with_accept"></a>![Method: ](https://apidocs.io/img/method.png ".PostBookingOperationsController.getBookingDetailAsyncWithAccept") getBookingDetailAsyncWithAccept

> *Tags:*  ``` Skips Authentication ``` 

> BookingDetail


```objc
function getBookingDetailAsyncWithAccept:(NSString*) accept
                apiKey:(NSString*) apiKey
                xSignature:(NSString*) xSignature
                bookingReference:(NSString*) bookingReference
                completionBlock:(CompletedGetBookingDetail) onCompleted(accept apiKey : apiKey xSignature : xSignature bookingReference : bookingReference)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| accept |  ``` Required ```  | TODO: Add a parameter description |
| apiKey |  ``` Required ```  | TODO: Add a parameter description |
| xSignature |  ``` Required ```  | TODO: Add a parameter description |
| bookingReference |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* accept = @"Accept";
    NSString* apiKey = @"Api-key";
    NSString* xSignature = @"X-Signature";
    NSString* bookingReference = @"booking_reference";

    [self.postBookingOperations getBookingDetailAsyncWithAccept: accept apiKey : apiKey xSignature : xSignature bookingReference : bookingReference  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="booking_controller"></a>![Class: ](https://apidocs.io/img/class.png ".BookingController") BookingController

### Get singleton instance
```objc
Booking* booking = [[Booking alloc]init] ;
```

### <a name="create_booking_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".BookingController.createBookingAsyncWithBody") createBookingAsyncWithBody

> *Tags:*  ``` Skips Authentication ``` 

> Booking


```objc
function createBookingAsyncWithBody:(BookingRequest*) body
                accept:(NSString*) accept
                apiKey:(NSString*) apiKey
                xSignature:(NSString*) xSignature
                contentType:(NSString*) contentType
                acceptEncoding:(NSString*) acceptEncoding
                completionBlock:(CompletedPostBooking) onCompleted(body accept : accept apiKey : apiKey xSignature : xSignature contentType : contentType acceptEncoding : acceptEncoding)
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

```objc
    // Parameters for the API call
    BookingRequest* body = (BookingRequest*) [APIHelper jsonDeserialize: @"{
  \"holder\": {
    \"name\": \"IntegrationTestFirstName\",
    \"surname\": \"IntegrationTestLastName\"
  },
  \"rooms\": [{
    \"rateKey\": \"20171115|20171120|W|52|1|DBL.ST|ID_B2B_25|RO|EM4TIES|1~1~0||N@1884739731\",
    \"paxes\": [{
      \"roomId\": \"1\",
      \"type\": \"AD\",
      \"name\": \"Adult Name\"
    }]
  }],
  \"clientReference\": \"IntegrationAgency\"
}"
                toClass: BookingRequest.class];
    NSString* accept = @"application/json";
    NSString* apiKey = @"{{Api-key}}";
    NSString* xSignature = @"{{X-Signature}}";
    NSString* contentType = @"application/json";
    NSString* acceptEncoding = @"gzip";

    [self.booking createBookingAsyncWithBody: body accept : accept apiKey : apiKey xSignature : xSignature contentType : contentType acceptEncoding : acceptEncoding  completionBlock:^(BOOL success, HttpContext* context, BookingResponse* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="check_rate_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CheckRateController") CheckRateController

### Get singleton instance
```objc
CheckRate* checkRate = [[CheckRate alloc]init] ;
```

### <a name="create_check_rate_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".CheckRateController.createCheckRateAsyncWithBody") createCheckRateAsyncWithBody

> *Tags:*  ``` Skips Authentication ``` 

> CheckRate


```objc
function createCheckRateAsyncWithBody:(CheckRateRequest*) body
                accept:(NSString*) accept
                apiKey:(NSString*) apiKey
                xSignature:(NSString*) xSignature
                contentType:(NSString*) contentType
                acceptEncoding:(NSString*) acceptEncoding
                completionBlock:(CompletedPostCheckRate) onCompleted(body accept : accept apiKey : apiKey xSignature : xSignature contentType : contentType acceptEncoding : acceptEncoding)
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

```objc
    // Parameters for the API call
    CheckRateRequest* body = (CheckRateRequest*) [APIHelper jsonDeserialize: @"{
  \"rooms\": [{
    \"rateKey\": \"20171115|20171120|W|52|1|SGL.ST|CG-EXT LONG RO|RO||1~1~0||N@A8921A639A0D46D88735806D109FA6E81544\"
  }]
}"
                toClass: CheckRateRequest.class];
    NSString* accept = @"application/json";
    NSString* apiKey = @"{{Api-key}}";
    NSString* xSignature = @"{{X-Signature}}";
    NSString* contentType = @"application/json";
    NSString* acceptEncoding = @"gzip";

    [self.checkRate createCheckRateAsyncWithBody: body accept : accept apiKey : apiKey xSignature : xSignature contentType : contentType acceptEncoding : acceptEncoding  completionBlock:^(BOOL success, HttpContext* context, CheckRateResponse* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="availability_controller"></a>![Class: ](https://apidocs.io/img/class.png ".AvailabilityController") AvailabilityController

### Get singleton instance
```objc
Availability* availability = [[Availability alloc]init] ;
```

### <a name="create_other_filters_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".AvailabilityController.createOtherFiltersAsyncWithBody") createOtherFiltersAsyncWithBody

> *Tags:*  ``` Skips Authentication ``` 

> Other filters


```objc
function createOtherFiltersAsyncWithBody:(OtherFiltersRequest*) body
                accept:(NSString*) accept
                apiKey:(NSString*) apiKey
                xSignature:(NSString*) xSignature
                contentType:(NSString*) contentType
                acceptEncoding:(NSString*) acceptEncoding
                completionBlock:(CompletedPostOtherFilters) onCompleted(body accept : accept apiKey : apiKey xSignature : xSignature contentType : contentType acceptEncoding : acceptEncoding)
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

```objc
    // Parameters for the API call
    OtherFiltersRequest* body = (OtherFiltersRequest*) [APIHelper jsonDeserialize: @"{
  \"stay\": {
    \"checkIn\": \"2017-11-15\",
    \"checkOut\": \"2017-11-20\",
    \"shiftDays\": \"2\"
  },
  \"occupancies\": [{
    \"rooms\": 1,
    \"adults\": 1,
    \"children\": 0
  }],
  \"hotels\": {
    \"hotel\": [1,
    271]
  },
  \"filter\": {
    \"minRate\": 100.000,
    \"maxRate\": 1700.000,
    \"minCategory\": 3,
    \"maxCategory\": 5,
    \"maxRooms\":3,
    \"maxRatesPerRoom\": 3,
    \"paymentType\": \"AT_HOTEL\",
    \"packaging\": true,
    \"hotelPackage\": \"YES\",
    \"contract\": \"CG-FIT B2B\"
  }
}"
                toClass: OtherFiltersRequest.class];
    NSString* accept = @"application/json";
    NSString* apiKey = @"{{Api-key}}";
    NSString* xSignature = @"{{X-Signature}}";
    NSString* contentType = @"application/json";
    NSString* acceptEncoding = @"gzip";

    [self.availability createOtherFiltersAsyncWithBody: body accept : accept apiKey : apiKey xSignature : xSignature contentType : contentType acceptEncoding : acceptEncoding  completionBlock:^(BOOL success, HttpContext* context, OtherFiltersResponse* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="misc_controller"></a>![Class: ](https://apidocs.io/img/class.png ".MiscController") MiscController

### Get singleton instance
```objc
Misc* misc = [[Misc alloc]init] ;
```

### <a name="get0_status_async_with_accept"></a>![Method: ](https://apidocs.io/img/method.png ".MiscController.get0StatusAsyncWithAccept") get0StatusAsyncWithAccept

> *Tags:*  ``` Skips Authentication ``` 

> 0. Status


```objc
function get0StatusAsyncWithAccept:(NSString*) accept
                apiKey:(NSString*) apiKey
                xSignature:(NSString*) xSignature
                completionBlock:(CompletedGetM0Status) onCompleted(accept apiKey : apiKey xSignature : xSignature)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| accept |  ``` Required ```  | TODO: Add a parameter description |
| apiKey |  ``` Required ```  | TODO: Add a parameter description |
| xSignature |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* accept = @"application/json";
    NSString* apiKey = @"{{Api-key}}";
    NSString* xSignature = @"{{X-Signature}}";

    [self.misc get0StatusAsyncWithAccept: accept apiKey : apiKey xSignature : xSignature  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)



