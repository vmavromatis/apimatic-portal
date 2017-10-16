# Getting started

APItude complete postman collection, with both BookingAPI & ContentAPI. You have the full details of our API in our developer portal:
https://developer.hotelbeds.com/docs?hotel

## How to Build

The generated code uses the Newtonsoft Json.NET NuGet Package. If the automatic NuGet package restore
is enabled, these dependencies will be installed automatically. Therefore,
you will need internet access for build.

1. Open the solution (APItudeBookingAPISwagger.sln) file.
2. Invoke the build process using `Ctrl+Shift+B` shortcut key or using the `Build` menu as shown below.

![Building SDK using Visual Studio](https://apidocs.io/illustration/cs?step=buildSDK&workspaceFolder=APItude%20BookingAPI%20Swagger-CSharp&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwagger.Tests)

## How to Use

The build process generates a portable class library, which can be used like a normal class library. The generated library is compatible with Windows Forms, Windows RT, Windows Phone 8,
Silverlight 5, Xamarin iOS, Xamarin Android and Mono. More information on how to use can be found at the [MSDN Portable Class Libraries documentation](http://msdn.microsoft.com/en-us/library/vstudio/gg597391%28v=vs.100%29.aspx).

The following section explains how to use the APItudeBookingAPISwagger library in a new console project.

### 1. Starting a new project

For starting a new project, right click on the current solution from the *solution explorer* and choose  ``` Add -> New Project ```.

![Add a new project in the existing solution using Visual Studio](https://apidocs.io/illustration/cs?step=addProject&workspaceFolder=APItude%20BookingAPI%20Swagger-CSharp&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwagger.Tests)

Next, choose "Console Application", provide a ``` TestConsoleProject ``` as the project name and click ``` OK ```.

![Create a new console project using Visual Studio](https://apidocs.io/illustration/cs?step=createProject&workspaceFolder=APItude%20BookingAPI%20Swagger-CSharp&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwagger.Tests)

### 2. Set as startup project

The new console project is the entry point for the eventual execution. This requires us to set the ``` TestConsoleProject ``` as the start-up project. To do this, right-click on the  ``` TestConsoleProject ``` and choose  ``` Set as StartUp Project ``` form the context menu.

![Set the new cosole project as the start up project](https://apidocs.io/illustration/cs?step=setStartup&workspaceFolder=APItude%20BookingAPI%20Swagger-CSharp&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwagger.Tests)

### 3. Add reference of the library project

In order to use the APItudeBookingAPISwagger library in the new project, first we must add a projet reference to the ``` TestConsoleProject ```. First, right click on the ``` References ``` node in the *solution explorer* and click ``` Add Reference... ```.

![Open references of the TestConsoleProject](https://apidocs.io/illustration/cs?step=addReference&workspaceFolder=APItude%20BookingAPI%20Swagger-CSharp&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwagger.Tests)

Next, a window will be displayed where we must set the ``` checkbox ``` on ``` APItudeBookingAPISwagger.Tests ``` and click ``` OK ```. By doing this, we have added a reference of the ```APItudeBookingAPISwagger.Tests``` project into the new ``` TestConsoleProject ```.

![Add a reference to the TestConsoleProject](https://apidocs.io/illustration/cs?step=createReference&workspaceFolder=APItude%20BookingAPI%20Swagger-CSharp&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwagger.Tests)

### 4. Write sample code

Once the ``` TestConsoleProject ``` is created, a file named ``` Program.cs ``` will be visible in the *solution explorer* with an empty ``` Main ``` method. This is the entry point for the execution of the entire solution.
Here, you can add code to initialize the client library and acquire the instance of a *Controller* class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

![Add a reference to the TestConsoleProject](https://apidocs.io/illustration/cs?step=addCode&workspaceFolder=APItude%20BookingAPI%20Swagger-CSharp&workspaceName=APItudeBookingAPISwagger&projectName=APItudeBookingAPISwagger.Tests)

## How to Test

The generated SDK also contain one or more Tests, which are contained in the Tests project.
In order to invoke these test cases, you will need *NUnit 3.0 Test Adapter Extension for Visual Studio*.
Once the SDK is complied, the test cases should appear in the Test Explorer window.
Here, you can click *Run All* to execute these test cases.

## Initialization

### 

API client can be initialized as following.

```csharp

APItudeBookingAPISwaggerClient client = new APItudeBookingAPISwaggerClient();
```



# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [PostBookingOperationsController](#post_booking_operations_controller)
* [BookingController](#booking_controller)
* [CheckRateController](#check_rate_controller)
* [AvailabilityController](#availability_controller)
* [MiscController](#misc_controller)

## <a name="post_booking_operations_controller"></a>![Class: ](https://apidocs.io/img/class.png "APItudeBookingAPISwagger.Tests.Controllers.PostBookingOperationsController") PostBookingOperationsController

### Get singleton instance

The singleton instance of the ``` PostBookingOperationsController ``` class can be accessed from the API Client.

```csharp
PostBookingOperationsController postBookingOperations = client.PostBookingOperations;
```

### <a name="get_booking_list"></a>![Method: ](https://apidocs.io/img/method.png "APItudeBookingAPISwagger.Tests.Controllers.PostBookingOperationsController.GetBookingList") GetBookingList

> *Tags:*  ``` Skips Authentication ``` 

> BookingList


```csharp
Task GetBookingList(
        DateTime start,
        DateTime end,
        string filterType,
        string status,
        int mfrom,
        int to,
        string accept,
        string apiKey,
        string xSignature)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| start |  ``` Required ```  | TODO: Add a parameter description |
| end |  ``` Required ```  | TODO: Add a parameter description |
| filterType |  ``` Required ```  | TODO: Add a parameter description |
| status |  ``` Required ```  | TODO: Add a parameter description |
| mfrom |  ``` Required ```  | TODO: Add a parameter description |
| to |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |
| apiKey |  ``` Required ```  | TODO: Add a parameter description |
| xSignature |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
DateTime start = 2017-08-15;
DateTime end = 2017-09-10;
string filterType = "CREATION";
string status = "ALL";
int mfrom = 1;
int to = 25;
string accept = "application/json";
string apiKey = "{{Api-key}}";
string xSignature = "{{X-Signature}}";

await postBookingOperations.GetBookingList(start, end, filterType, status, mfrom, to, accept, apiKey, xSignature);

```


### <a name="delete_booking_cancellation"></a>![Method: ](https://apidocs.io/img/method.png "APItudeBookingAPISwagger.Tests.Controllers.PostBookingOperationsController.DeleteBookingCancellation") DeleteBookingCancellation

> *Tags:*  ``` Skips Authentication ``` 

> BookingCancellation


```csharp
Task DeleteBookingCancellation(
        string cancellationFlag,
        string language,
        string accept,
        string apiKey,
        string xSignature,
        string bookingReference)
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

```csharp
string cancellationFlag = "cancellationFlag";
string language = "language";
string accept = "Accept";
string apiKey = "Api-key";
string xSignature = "X-Signature";
string bookingReference = "booking_reference";

await postBookingOperations.DeleteBookingCancellation(cancellationFlag, language, accept, apiKey, xSignature, bookingReference);

```


### <a name="update_booking_change"></a>![Method: ](https://apidocs.io/img/method.png "APItudeBookingAPISwagger.Tests.Controllers.PostBookingOperationsController.UpdateBookingChange") UpdateBookingChange

> *Tags:*  ``` Skips Authentication ``` 

> BookingChange


```csharp
Task<PCL.Models.BookingChangeResponse> UpdateBookingChange(
        PCL.Models.BookingChangeRequest body,
        string accept,
        string apiKey,
        string xSignature,
        string contentType,
        string acceptEncoding,
        string bookingReference)
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

```csharp
var body = new PCL.Models.BookingChangeRequest();
string accept = "Accept";
string apiKey = "Api-key";
string xSignature = "X-Signature";
string contentType = "Content-Type";
string acceptEncoding = "Accept-Encoding";
string bookingReference = "booking_reference";

PCL.Models.BookingChangeResponse result = await postBookingOperations.UpdateBookingChange(body, accept, apiKey, xSignature, contentType, acceptEncoding, bookingReference);

```


### <a name="get_booking_detail"></a>![Method: ](https://apidocs.io/img/method.png "APItudeBookingAPISwagger.Tests.Controllers.PostBookingOperationsController.GetBookingDetail") GetBookingDetail

> *Tags:*  ``` Skips Authentication ``` 

> BookingDetail


```csharp
Task GetBookingDetail(
        string accept,
        string apiKey,
        string xSignature,
        string bookingReference)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| accept |  ``` Required ```  | TODO: Add a parameter description |
| apiKey |  ``` Required ```  | TODO: Add a parameter description |
| xSignature |  ``` Required ```  | TODO: Add a parameter description |
| bookingReference |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string accept = "Accept";
string apiKey = "Api-key";
string xSignature = "X-Signature";
string bookingReference = "booking_reference";

await postBookingOperations.GetBookingDetail(accept, apiKey, xSignature, bookingReference);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="booking_controller"></a>![Class: ](https://apidocs.io/img/class.png "APItudeBookingAPISwagger.Tests.Controllers.BookingController") BookingController

### Get singleton instance

The singleton instance of the ``` BookingController ``` class can be accessed from the API Client.

```csharp
BookingController booking = client.Booking;
```

### <a name="create_booking"></a>![Method: ](https://apidocs.io/img/method.png "APItudeBookingAPISwagger.Tests.Controllers.BookingController.CreateBooking") CreateBooking

> *Tags:*  ``` Skips Authentication ``` 

> Booking


```csharp
Task<PCL.Models.BookingResponse> CreateBooking(
        PCL.Models.BookingRequest body,
        string accept,
        string apiKey,
        string xSignature,
        string contentType,
        string acceptEncoding)
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

```csharp
string bodyValue = "{\n  \"holder\": {\n    \"name\": \"IntegrationTestFirstName\",\n    \"surname\": \"IntegrationTestLastName\"\n  },\n  \"rooms\": [{\n    \"rateKey\": \"20171115|20171120|W|52|1|DBL.ST|ID_B2B_25|RO|EM4TIES|1~1~0||N@1884739731\",\n    \"paxes\": [{\n      \"roomId\": \"1\",\n      \"type\": \"AD\",\n      \"name\": \"Adult Name\"\n    }]\n  }],\n  \"clientReference\": \"IntegrationAgency\"\n}";
var body = Newtonsoft.Json.JsonConvert.DeserializeObject<PCL.Models.BookingRequest>(bodyValue);
string accept = "application/json";
string apiKey = "{{Api-key}}";
string xSignature = "{{X-Signature}}";
string contentType = "application/json";
string acceptEncoding = "gzip";

PCL.Models.BookingResponse result = await booking.CreateBooking(body, accept, apiKey, xSignature, contentType, acceptEncoding);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="check_rate_controller"></a>![Class: ](https://apidocs.io/img/class.png "APItudeBookingAPISwagger.Tests.Controllers.CheckRateController") CheckRateController

### Get singleton instance

The singleton instance of the ``` CheckRateController ``` class can be accessed from the API Client.

```csharp
CheckRateController checkRate = client.CheckRate;
```

### <a name="create_check_rate"></a>![Method: ](https://apidocs.io/img/method.png "APItudeBookingAPISwagger.Tests.Controllers.CheckRateController.CreateCheckRate") CreateCheckRate

> *Tags:*  ``` Skips Authentication ``` 

> CheckRate


```csharp
Task<PCL.Models.CheckRateResponse> CreateCheckRate(
        PCL.Models.CheckRateRequest body,
        string accept,
        string apiKey,
        string xSignature,
        string contentType,
        string acceptEncoding)
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

```csharp
string bodyValue = "{\n  \"rooms\": [{\n    \"rateKey\": \"20171115|20171120|W|52|1|SGL.ST|CG-EXT LONG RO|RO||1~1~0||N@A8921A639A0D46D88735806D109FA6E81544\"\n  }]\n}";
var body = Newtonsoft.Json.JsonConvert.DeserializeObject<PCL.Models.CheckRateRequest>(bodyValue);
string accept = "application/json";
string apiKey = "{{Api-key}}";
string xSignature = "{{X-Signature}}";
string contentType = "application/json";
string acceptEncoding = "gzip";

PCL.Models.CheckRateResponse result = await checkRate.CreateCheckRate(body, accept, apiKey, xSignature, contentType, acceptEncoding);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="availability_controller"></a>![Class: ](https://apidocs.io/img/class.png "APItudeBookingAPISwagger.Tests.Controllers.AvailabilityController") AvailabilityController

### Get singleton instance

The singleton instance of the ``` AvailabilityController ``` class can be accessed from the API Client.

```csharp
AvailabilityController availability = client.Availability;
```

### <a name="create_other_filters"></a>![Method: ](https://apidocs.io/img/method.png "APItudeBookingAPISwagger.Tests.Controllers.AvailabilityController.CreateOtherFilters") CreateOtherFilters

> *Tags:*  ``` Skips Authentication ``` 

> Other filters


```csharp
Task<PCL.Models.OtherFiltersResponse> CreateOtherFilters(
        PCL.Models.OtherFiltersRequest body,
        string accept,
        string apiKey,
        string xSignature,
        string contentType,
        string acceptEncoding)
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

```csharp
string bodyValue = "{\n  \"stay\": {\n    \"checkIn\": \"2017-11-15\",\n    \"checkOut\": \"2017-11-20\",\n    \"shiftDays\": \"2\"\n  },\n  \"occupancies\": [{\n    \"rooms\": 1,\n    \"adults\": 1,\n    \"children\": 0\n  }],\n  \"hotels\": {\n    \"hotel\": [1,\n    271]\n  },\n  \"filter\": {\n    \"minRate\": 100.000,\n    \"maxRate\": 1700.000,\n    \"minCategory\": 3,\n    \"maxCategory\": 5,\n    \"maxRooms\":3,\n    \"maxRatesPerRoom\": 3,\n    \"paymentType\": \"AT_HOTEL\",\n    \"packaging\": true,\n    \"hotelPackage\": \"YES\",\n    \"contract\": \"CG-FIT B2B\"\n  }\n}";
var body = Newtonsoft.Json.JsonConvert.DeserializeObject<PCL.Models.OtherFiltersRequest>(bodyValue);
string accept = "application/json";
string apiKey = "{{Api-key}}";
string xSignature = "{{X-Signature}}";
string contentType = "application/json";
string acceptEncoding = "gzip";

PCL.Models.OtherFiltersResponse result = await availability.CreateOtherFilters(body, accept, apiKey, xSignature, contentType, acceptEncoding);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="misc_controller"></a>![Class: ](https://apidocs.io/img/class.png "APItudeBookingAPISwagger.Tests.Controllers.MiscController") MiscController

### Get singleton instance

The singleton instance of the ``` MiscController ``` class can be accessed from the API Client.

```csharp
MiscController misc = client.Misc;
```

### <a name="get0_status"></a>![Method: ](https://apidocs.io/img/method.png "APItudeBookingAPISwagger.Tests.Controllers.MiscController.Get0Status") Get0Status

> *Tags:*  ``` Skips Authentication ``` 

> 0. Status


```csharp
Task Get0Status(string accept, string apiKey, string xSignature)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| accept |  ``` Required ```  | TODO: Add a parameter description |
| apiKey |  ``` Required ```  | TODO: Add a parameter description |
| xSignature |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string accept = "application/json";
string apiKey = "{{Api-key}}";
string xSignature = "{{X-Signature}}";

await misc.Get0Status(accept, apiKey, xSignature);

```


[Back to List of Controllers](#list_of_controllers)



