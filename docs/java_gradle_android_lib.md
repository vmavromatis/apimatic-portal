# Getting started

APItude complete postman collection, with both BookingAPI & ContentAPI. You have the full details of our API in our developer portal:
https://developer.hotelbeds.com/docs?hotel

## How to Build

The generated code uses a few Gradle dependencies e.g., Jackson, Volley,
and Apache HttpClient. The reference to these dependencies is already
added in the build.gradle file will be installed automatically. Therefore,
you will need internet access for a successful build.

* In order to open the client library in Android Studio click on ``` Open an Existing Android Project ```.

![Importing SDK into Android Studio - Step 1](https://apidocs.io/illustration/android?step=import1&workspaceFolder=APItude%20BookingAPI%20Swagger&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwaggerLib&rootNamespace=com.example)

* Browse to locate the folder containing the source code. Select the location of the APItudeBookingAPISwagger gradle project and click ``` Ok ```.

![Importing SDK into Android Studio - Step 2](https://apidocs.io/illustration/android?step=import2&workspaceFolder=APItude%20BookingAPI%20Swagger&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwaggerLib&rootNamespace=com.example)

* Upon successful import, the project can be built by clicking on ``` Build > Make Project ``` or  pressing ``` Ctrl + F9 ```.

![Importing SDK into Android Studio - Step 3](https://apidocs.io/illustration/android?step=import3&workspaceFolder=APItude%20BookingAPI%20Swagger&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwaggerLib&rootNamespace=com.example)

## How to Use

The following section explains how to use the APItudeBookingAPISwagger library in a new project.

### 1. Starting a new project 

For starting a new project, click on ``` Create New Android Studio Project ```.

![Add a new project in Android Studio - Step 1](https://apidocs.io/illustration/android?step=createNewProject0&workspaceFolder=APItude%20BookingAPI%20Swagger&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwaggerLib&rootNamespace=com.example)

Here, configure the new project by adding the name, domain and location of the sample application followed by clicking ``` Next ```.

![Create a new Android Studio Project - Step 2](https://apidocs.io/illustration/android?step=createNewProject1&workspaceFolder=APItude%20BookingAPI%20Swagger&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwaggerLib&rootNamespace=com.example)

Following this, select the `Phone and Tablet` option as shown in the illustration below and click `Next`.

![Create a new Android Studio Project - Step 3](https://apidocs.io/illustration/android?step=createNewProject2&workspaceFolder=APItude%20BookingAPI%20Swagger&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwaggerLib&rootNamespace=com.example)

In the following step, choose ``` Empty Activity ``` as the activity type and click ``` Next ```.

![Create a new Android Studio Project - Step 4](https://apidocs.io/illustration/android?step=createNewProject3&workspaceFolder=APItude%20BookingAPI%20Swagger&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwaggerLib&rootNamespace=com.example)

In this step, provide an ``` Activity Name ``` and ``` Layout Name ``` and click ``` Finish ```.  This would take you to the newly created project.

![Create a new Android Studio Project - Step 4](https://apidocs.io/illustration/android?step=createNewProject4&workspaceFolder=APItude%20BookingAPI%20Swagger&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwaggerLib&rootNamespace=com.example)

### 2. Add reference of the library project

In order to add a dependency to this sample application, click on the android button shown in the project explorer on the left side as shown in the picture. Click on ``` Project ``` in the drop down that emerges.  

![Adding dependency to the client library - Step 1](https://apidocs.io/illustration/android?step=testProject0&workspaceFolder=APItude%20BookingAPI%20Swagger&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwaggerLib&rootNamespace=com.example)

Right click the sample application in the project explorer and click on ``` New > Module ```  as shown in the picture.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/android?step=testProject1&workspaceFolder=APItude%20BookingAPI%20Swagger&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwaggerLib&rootNamespace=com.example)

Choose ``` Import Gradle Project ``` and click ``` Next ```.

![Adding dependency to the client library - Step 3](https://apidocs.io/illustration/android?step=testProject2&workspaceFolder=APItude%20BookingAPI%20Swagger&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwaggerLib&rootNamespace=com.example)

Click on ``` Finish ``` which would take you back to the sample application with the refernced SDK. 

![Adding dependency to the client library - Step 4](https://apidocs.io/illustration/android?step=testProject3&workspaceFolder=APItude%20BookingAPI%20Swagger&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwaggerLib&rootNamespace=com.example)

In the following step naigate to the ``` SampleApplication >  app > build.gradle ``` file and add the following line ```compile project(path: ':APItudeBookingAPISwagger')``` to the dependencies section as shown in the illustration below.

![Adding dependency to the client library - Step 5](https://apidocs.io/illustration/android?step=testProject4&workspaceFolder=APItude%20BookingAPI%20Swagger&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwaggerLib&rootNamespace=com.example)

Finally, press ``` Sync Now ``` in the warning visible as shown in the picture below.

![Adding dependency to the client library - Step 6](https://apidocs.io/illustration/android?step=testProject5&workspaceFolder=APItude%20BookingAPI%20Swagger&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwaggerLib&rootNamespace=com.example)

### 3. Write sample code

Once the ``` SampleApplication ``` is created, a file named ``` SampleApplication > app > src > main > java > MainActivity ``` will be visible in the *Project Explorer* with an ``` onCreate ``` method. This is the entry point for the execution of the created project.
Here, you can add code to initialize the client library and instantiate a *Controller* class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

## How to Test

The generated code and the server can be tested using automatically generated test cases. 
JUnit is used as the testing framework and test runner.

In Android Studio, for running the tests do the following:

1. Right click on *SampleApplication > APItudeBookingAPISwaggerLib > androidTest > java)* from the project explorer.
2. Select "Run All Tests" or use "Ctrl + Shift + F10" to run the Tests.

## Initialization

### 

API client can be initialized as following. The `appContext` being passed is the Android application [`Context`](https://developer.android.com/reference/android/content/Context.html).

```java

com.example.Configuration.initialize(appContext);
APItudeBookingAPISwaggerClient client = new APItudeBookingAPISwaggerClient();
```


# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [PostBookingOperationsController](#post_booking_operations_controller)
* [BookingController](#booking_controller)
* [CheckRateController](#check_rate_controller)
* [AvailabilityController](#availability_controller)
* [MiscController](#misc_controller)

## <a name="post_booking_operations_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.controllers.PostBookingOperationsController") PostBookingOperationsController

### Get singleton instance

The singleton instance of the ``` PostBookingOperationsController ``` class can be accessed from the API Client.

```java
PostBookingOperationsController postBookingOperations = client.getPostBookingOperations();
```

### <a name="get_booking_list_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.PostBookingOperationsController.getBookingListAsync") getBookingListAsync

> *Tags:*  ``` Skips Authentication ``` 

> BookingList


```java
void getBookingListAsync(
        final Date start,
        final Date end,
        final String filterType,
        final String status,
        final int from,
        final int to,
        final String accept,
        final String apiKey,
        final String xSignature,
        final APICallBack<Object> callBack)
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

```java
Date start = 2017-08-15;
Date end = 2017-09-10;
String filterType = "CREATION";
String status = "ALL";
int from = 1;
int to = 25;
String accept = "application/json";
String apiKey = "{{Api-key}}";
String xSignature = "{{X-Signature}}";
// Invoking the API call with sample inputs
postBookingOperations.getBookingListAsync(start, end, filterType, status, from, to, accept, apiKey, xSignature, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="delete_booking_cancellation_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.PostBookingOperationsController.deleteBookingCancellationAsync") deleteBookingCancellationAsync

> *Tags:*  ``` Skips Authentication ``` 

> BookingCancellation


```java
void deleteBookingCancellationAsync(
        final String cancellationFlag,
        final String language,
        final String accept,
        final String apiKey,
        final String xSignature,
        final String bookingReference,
        final APICallBack<Object> callBack)
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

```java
String cancellationFlag = "cancellationFlag";
String language = "language";
String accept = "Accept";
String apiKey = "Api-key";
String xSignature = "X-Signature";
String bookingReference = "booking_reference";
// Invoking the API call with sample inputs
postBookingOperations.deleteBookingCancellationAsync(cancellationFlag, language, accept, apiKey, xSignature, bookingReference, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="update_booking_change_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.PostBookingOperationsController.updateBookingChangeAsync") updateBookingChangeAsync

> *Tags:*  ``` Skips Authentication ``` 

> BookingChange


```java
void updateBookingChangeAsync(
        final BookingChangeRequest body,
        final String accept,
        final String apiKey,
        final String xSignature,
        final String contentType,
        final String acceptEncoding,
        final String bookingReference,
        final APICallBack<BookingChangeResponse> callBack)
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

```java
try {
    BookingChangeRequest body = new BookingChangeRequest();
    String accept = "Accept";
    String apiKey = "Api-key";
    String xSignature = "X-Signature";
    String contentType = "Content-Type";
    String acceptEncoding = "Accept-Encoding";
    String bookingReference = "booking_reference";
    // Invoking the API call with sample inputs
    postBookingOperations.updateBookingChangeAsync(body, accept, apiKey, xSignature, contentType, acceptEncoding, bookingReference, new APICallBack<BookingChangeResponse>() {
        public void onSuccess(HttpContext context, BookingChangeResponse response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    });
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


### <a name="get_booking_detail_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.PostBookingOperationsController.getBookingDetailAsync") getBookingDetailAsync

> *Tags:*  ``` Skips Authentication ``` 

> BookingDetail


```java
void getBookingDetailAsync(
        final String accept,
        final String apiKey,
        final String xSignature,
        final String bookingReference,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| accept |  ``` Required ```  | TODO: Add a parameter description |
| apiKey |  ``` Required ```  | TODO: Add a parameter description |
| xSignature |  ``` Required ```  | TODO: Add a parameter description |
| bookingReference |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String accept = "Accept";
String apiKey = "Api-key";
String xSignature = "X-Signature";
String bookingReference = "booking_reference";
// Invoking the API call with sample inputs
postBookingOperations.getBookingDetailAsync(accept, apiKey, xSignature, bookingReference, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="booking_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.controllers.BookingController") BookingController

### Get singleton instance

The singleton instance of the ``` BookingController ``` class can be accessed from the API Client.

```java
BookingController booking = client.getBooking();
```

### <a name="create_booking_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.BookingController.createBookingAsync") createBookingAsync

> *Tags:*  ``` Skips Authentication ``` 

> Booking


```java
void createBookingAsync(
        final BookingRequest body,
        final String accept,
        final String apiKey,
        final String xSignature,
        final String contentType,
        final String acceptEncoding,
        final APICallBack<BookingResponse> callBack)
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

```java
try {
    String bodyValue = "{\n  \"holder\": {\n    \"name\": \"IntegrationTestFirstName\",\n    \"surname\": \"IntegrationTestLastName\"\n  },\n  \"rooms\": [{\n    \"rateKey\": \"20171115|20171120|W|52|1|DBL.ST|ID_B2B_25|RO|EM4TIES|1~1~0||N@1884739731\",\n    \"paxes\": [{\n      \"roomId\": \"1\",\n      \"type\": \"AD\",\n      \"name\": \"Adult Name\"\n    }]\n  }],\n  \"clientReference\": \"IntegrationAgency\"\n}";
    BookingRequest body = mapper.readValue(bodyValue,new TypeReference<BookingRequest> (){});
    String accept = "application/json";
    String apiKey = "{{Api-key}}";
    String xSignature = "{{X-Signature}}";
    String contentType = "application/json";
    String acceptEncoding = "gzip";
    // Invoking the API call with sample inputs
    booking.createBookingAsync(body, accept, apiKey, xSignature, contentType, acceptEncoding, new APICallBack<BookingResponse>() {
        public void onSuccess(HttpContext context, BookingResponse response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    });
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


[Back to List of Controllers](#list_of_controllers)

## <a name="check_rate_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.controllers.CheckRateController") CheckRateController

### Get singleton instance

The singleton instance of the ``` CheckRateController ``` class can be accessed from the API Client.

```java
CheckRateController checkRate = client.getCheckRate();
```

### <a name="create_check_rate_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.CheckRateController.createCheckRateAsync") createCheckRateAsync

> *Tags:*  ``` Skips Authentication ``` 

> CheckRate


```java
void createCheckRateAsync(
        final CheckRateRequest body,
        final String accept,
        final String apiKey,
        final String xSignature,
        final String contentType,
        final String acceptEncoding,
        final APICallBack<CheckRateResponse> callBack)
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

```java
try {
    String bodyValue = "{\n  \"rooms\": [{\n    \"rateKey\": \"20171115|20171120|W|52|1|SGL.ST|CG-EXT LONG RO|RO||1~1~0||N@A8921A639A0D46D88735806D109FA6E81544\"\n  }]\n}";
    CheckRateRequest body = mapper.readValue(bodyValue,new TypeReference<CheckRateRequest> (){});
    String accept = "application/json";
    String apiKey = "{{Api-key}}";
    String xSignature = "{{X-Signature}}";
    String contentType = "application/json";
    String acceptEncoding = "gzip";
    // Invoking the API call with sample inputs
    checkRate.createCheckRateAsync(body, accept, apiKey, xSignature, contentType, acceptEncoding, new APICallBack<CheckRateResponse>() {
        public void onSuccess(HttpContext context, CheckRateResponse response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    });
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


[Back to List of Controllers](#list_of_controllers)

## <a name="availability_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.controllers.AvailabilityController") AvailabilityController

### Get singleton instance

The singleton instance of the ``` AvailabilityController ``` class can be accessed from the API Client.

```java
AvailabilityController availability = client.getAvailability();
```

### <a name="create_other_filters_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.AvailabilityController.createOtherFiltersAsync") createOtherFiltersAsync

> *Tags:*  ``` Skips Authentication ``` 

> Other filters


```java
void createOtherFiltersAsync(
        final OtherFiltersRequest body,
        final String accept,
        final String apiKey,
        final String xSignature,
        final String contentType,
        final String acceptEncoding,
        final APICallBack<OtherFiltersResponse> callBack)
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

```java
try {
    String bodyValue = "{\n  \"stay\": {\n    \"checkIn\": \"2017-11-15\",\n    \"checkOut\": \"2017-11-20\",\n    \"shiftDays\": \"2\"\n  },\n  \"occupancies\": [{\n    \"rooms\": 1,\n    \"adults\": 1,\n    \"children\": 0\n  }],\n  \"hotels\": {\n    \"hotel\": [1,\n    271]\n  },\n  \"filter\": {\n    \"minRate\": 100.000,\n    \"maxRate\": 1700.000,\n    \"minCategory\": 3,\n    \"maxCategory\": 5,\n    \"maxRooms\":3,\n    \"maxRatesPerRoom\": 3,\n    \"paymentType\": \"AT_HOTEL\",\n    \"packaging\": true,\n    \"hotelPackage\": \"YES\",\n    \"contract\": \"CG-FIT B2B\"\n  }\n}";
    OtherFiltersRequest body = mapper.readValue(bodyValue,new TypeReference<OtherFiltersRequest> (){});
    String accept = "application/json";
    String apiKey = "{{Api-key}}";
    String xSignature = "{{X-Signature}}";
    String contentType = "application/json";
    String acceptEncoding = "gzip";
    // Invoking the API call with sample inputs
    availability.createOtherFiltersAsync(body, accept, apiKey, xSignature, contentType, acceptEncoding, new APICallBack<OtherFiltersResponse>() {
        public void onSuccess(HttpContext context, OtherFiltersResponse response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    });
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


[Back to List of Controllers](#list_of_controllers)

## <a name="misc_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.controllers.MiscController") MiscController

### Get singleton instance

The singleton instance of the ``` MiscController ``` class can be accessed from the API Client.

```java
MiscController misc = client.getMisc();
```

### <a name="get0_status_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.MiscController.get0StatusAsync") get0StatusAsync

> *Tags:*  ``` Skips Authentication ``` 

> 0. Status


```java
void get0StatusAsync(
        final String accept,
        final String apiKey,
        final String xSignature,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| accept |  ``` Required ```  | TODO: Add a parameter description |
| apiKey |  ``` Required ```  | TODO: Add a parameter description |
| xSignature |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String accept = "application/json";
String apiKey = "{{Api-key}}";
String xSignature = "{{X-Signature}}";
// Invoking the API call with sample inputs
misc.get0StatusAsync(accept, apiKey, xSignature, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)



