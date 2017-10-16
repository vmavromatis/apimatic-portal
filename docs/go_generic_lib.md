# Getting started

APItude complete postman collection, with both BookingAPI & ContentAPI. You have the full details of our API in our developer portal:
https://developer.hotelbeds.com/docs?hotel

## How to Build


* In order to successfully build and run your SDK files, you are required to have the following setup in your system:
    * **Go**  (Visit [https://golang.org/doc/install](https://golang.org/doc/install) for more details on how to install Go)
    * **Java VM** Version 8 or later
    * **Eclipse 4.6 (Neon)** or later ([http://www.eclipse.org/neon/](http://www.eclipse.org/neon/))
    * **GoClipse** setup within above installed Eclipse (Follow the instructions at [this link](https://github.com/GoClipse/goclipse/blob/latest/documentation/Installation.md#instructions) to setup GoClipse)
* Ensure that ```GOPATH``` environment variable is set in the system variables. If not, set it to your workspace directory where you will be adding your Go projects.
* The generated code uses unirest-go http library. Therefore, you will need internet access to resolve this dependency. If Go is properly installed and configured, run the following command to pull the dependency:

```Go
go get github.com/apimatic/unirest-go
```

This will install unirest-go in the ```GOPATH``` you specified in the system variables.

Now follow the steps mentioned below to build your SDK:

1. Open eclipse in the Go language perspective and click on the ```Import``` option in ```File``` menu.

![Importing SDK into Eclipse - Step 1](https://apidocs.io/illustration/go?step=import0)

2. Select ```General -> Existing Projects into Workspace``` option from the tree list.

![Importing SDK into Eclipse - Step 2](https://apidocs.io/illustration/go?step=import1)

3. In ```Select root directory```, provide path to the unzipped archive for the generated code. Once the path is set and the Project becomes visible under ```Projects``` click ```Finish```

![Importing SDK into Eclipse - Step 3](https://apidocs.io/illustration/go?step=import2&workspaceFolder=APItude%20BookingAPI%20Swagger-GoLang&projectName=apitudebookingapiswagger_lib)

4. The Go library will be imported and its files will be visible in the Project Explorer

![Importing SDK into Eclipse - Step 4](https://apidocs.io/illustration/go?step=import3&projectName=apitudebookingapiswagger_lib)

## How to Use

The following section explains how to use the ApitudebookingapiswaggerLib library in a new project.

### 1. Add a new Test Project

Create a new project in Eclipse by ```File``` -> ```New``` -> ```Go Project```

![Add a new project in Eclipse](https://apidocs.io/illustration/go?step=createNewProject0)

Name the Project as ```Test``` and click ```Finish```

![Create a new Maven Project - Step 1](https://apidocs.io/illustration/go?step=createNewProject1)

Create a new directory in the ```src``` directory of this project

![Create a new Maven Project - Step 2](https://apidocs.io/illustration/go?step=createNewProject2&projectName=apitudebookingapiswagger_lib)

Name it ```test.com```

![Create a new Maven Project - Step 3](https://apidocs.io/illustration/go?step=createNewProject3&projectName=apitudebookingapiswagger_lib)

Now create a new file inside ```src/test.com```

![Create a new Maven Project - Step 4](https://apidocs.io/illustration/go?step=createNewProject4&projectName=apitudebookingapiswagger_lib)

Name it ```testsdk.go```

![Create a new Maven Project - Step 5](https://apidocs.io/illustration/go?step=createNewProject5&projectName=apitudebookingapiswagger_lib)

In this Go file, you can start adding code to initialize the client library. Sample code to initialize the client library and using its methods is given in the subsequent sections.

### 2. Configure the Test Project

You need to import your generated library in this project in order to make use of its functions. In order to import the library, you can add its path in the ```GOPATH``` for this project. Follow the below steps:

Right click on the project name and click on ```Properties```

![Adding dependency to the client library - Step 1](https://apidocs.io/illustration/go?step=testProject0&projectName=apitudebookingapiswagger_lib)

Choose ```Go Compiler``` from the side menu. Check ```Use project specific settings``` and uncheck ```Use same value as the GOPATH environment variable.```. By default, the GOPATH value from the environment variables will be visible in ```Eclipse GOPATH```. Do not remove this as this points to the unirest dependency.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/go?step=testProject1)

Append the library path to this GOPATH

![Adding dependency to the client library - Step 3](https://apidocs.io/illustration/go?step=testProject2&workspaceFolder=APItude%20BookingAPI%20Swagger-GoLang)

Once the path is appended, click on ```OK```

### 3. Build the Test Project

Right click on the project name and click on ```Build Project```

![Build Project](https://apidocs.io/illustration/go?step=buildProject&projectName=apitudebookingapiswagger_lib)

### 4. Run the Test Project

If the build is successful, right click on your Go file and click on ```Run As``` -> ```Go Application```

![Run Project](https://apidocs.io/illustration/go?step=runProject&projectName=apitudebookingapiswagger_lib)

# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [postbookingoperations_pkg](#postbookingoperations_pkg)
* [booking_pkg](#booking_pkg)
* [checkrate_pkg](#checkrate_pkg)
* [availability_pkg](#availability_pkg)
* [misc_pkg](#misc_pkg)

## <a name="postbookingoperations_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".postbookingoperations_pkg") postbookingoperations_pkg

### Get instance

Factory for the ``` POSTBOOKINGOPERATIONS ``` interface can be accessed from the package postbookingoperations_pkg.

```go
postBookingOperations := postbookingoperations_pkg.NewPOSTBOOKINGOPERATIONS()
```

### <a name="get_booking_list"></a>![Method: ](https://apidocs.io/img/method.png ".postbookingoperations_pkg.GetBookingList") GetBookingList

> *Tags:*  ``` Skips Authentication ``` 

> BookingList


```go
func (me *POSTBOOKINGOPERATIONS_IMPL) GetBookingList(
            start *time.Time,
            end *time.Time,
            filterType string,
            status string,
            from int64,
            to int64,
            accept string,
            apiKey string,
            xSignature string)(,error)
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

```go
start := "2017-08-15"
end := "2017-09-10"
filterType := "CREATION"
status := "ALL"
from,_ := strconv.ParseInt("1", 10, 8)
to,_ := strconv.ParseInt("25", 10, 8)
accept := "application/json"
apiKey := "{{Api-key}}"
xSignature := "{{X-Signature}}"

var result 
result,_ = postBookingOperations.GetBookingList(start, end, filterType, status, from, to, accept, apiKey, xSignature)

```


### <a name="delete_booking_cancellation"></a>![Method: ](https://apidocs.io/img/method.png ".postbookingoperations_pkg.DeleteBookingCancellation") DeleteBookingCancellation

> *Tags:*  ``` Skips Authentication ``` 

> BookingCancellation


```go
func (me *POSTBOOKINGOPERATIONS_IMPL) DeleteBookingCancellation(
            cancellationFlag string,
            language string,
            accept string,
            apiKey string,
            xSignature string,
            bookingReference string)(,error)
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

```go
cancellationFlag := "cancellationFlag"
language := "language"
accept := "Accept"
apiKey := "Api-key"
xSignature := "X-Signature"
bookingReference := "booking_reference"

var result 
result,_ = postBookingOperations.DeleteBookingCancellation(cancellationFlag, language, accept, apiKey, xSignature, bookingReference)

```


### <a name="update_booking_change"></a>![Method: ](https://apidocs.io/img/method.png ".postbookingoperations_pkg.UpdateBookingChange") UpdateBookingChange

> *Tags:*  ``` Skips Authentication ``` 

> BookingChange


```go
func (me *POSTBOOKINGOPERATIONS_IMPL) UpdateBookingChange(
            body *models_pkg.BookingChangeRequest,
            accept string,
            apiKey string,
            xSignature string,
            contentType string,
            acceptEncoding string,
            bookingReference string)(*models_pkg.BookingChangeResponse,error)
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

```go
var body *models_pkg.BookingChangeRequest
accept := "Accept"
apiKey := "Api-key"
xSignature := "X-Signature"
contentType := "Content-Type"
acceptEncoding := "Accept-Encoding"
bookingReference := "booking_reference"

var result *models_pkg.BookingChangeResponse
result,_ = postBookingOperations.UpdateBookingChange(body, accept, apiKey, xSignature, contentType, acceptEncoding, bookingReference)

```


### <a name="get_booking_detail"></a>![Method: ](https://apidocs.io/img/method.png ".postbookingoperations_pkg.GetBookingDetail") GetBookingDetail

> *Tags:*  ``` Skips Authentication ``` 

> BookingDetail


```go
func (me *POSTBOOKINGOPERATIONS_IMPL) GetBookingDetail(
            accept string,
            apiKey string,
            xSignature string,
            bookingReference string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| accept |  ``` Required ```  | TODO: Add a parameter description |
| apiKey |  ``` Required ```  | TODO: Add a parameter description |
| xSignature |  ``` Required ```  | TODO: Add a parameter description |
| bookingReference |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
accept := "Accept"
apiKey := "Api-key"
xSignature := "X-Signature"
bookingReference := "booking_reference"

var result 
result,_ = postBookingOperations.GetBookingDetail(accept, apiKey, xSignature, bookingReference)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="booking_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".booking_pkg") booking_pkg

### Get instance

Factory for the ``` BOOKING ``` interface can be accessed from the package booking_pkg.

```go
booking := booking_pkg.NewBOOKING()
```

### <a name="create_booking"></a>![Method: ](https://apidocs.io/img/method.png ".booking_pkg.CreateBooking") CreateBooking

> *Tags:*  ``` Skips Authentication ``` 

> Booking


```go
func (me *BOOKING_IMPL) CreateBooking(
            body *models_pkg.BookingRequest,
            accept string,
            apiKey string,
            xSignature string,
            contentType string,
            acceptEncoding string)(*models_pkg.BookingResponse,error)
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

```go
bodyValue := []byte("{\n  \"holder\": {\n    \"name\": \"IntegrationTestFirstName\",\n    \"surname\": \"IntegrationTestLastName\"\n  },\n  \"rooms\": [{\n    \"rateKey\": \"20171115|20171120|W|52|1|DBL.ST|ID_B2B_25|RO|EM4TIES|1~1~0||N@1884739731\",\n    \"paxes\": [{\n      \"roomId\": \"1\",\n      \"type\": \"AD\",\n      \"name\": \"Adult Name\"\n    }]\n  }],\n  \"clientReference\": \"IntegrationAgency\"\n}")
var body *models_pkg.BookingRequest
json.Unmarshal(bodyValue,&body)
accept := "application/json"
apiKey := "{{Api-key}}"
xSignature := "{{X-Signature}}"
contentType := "application/json"
acceptEncoding := "gzip"

var result *models_pkg.BookingResponse
result,_ = booking.CreateBooking(body, accept, apiKey, xSignature, contentType, acceptEncoding)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="checkrate_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".checkrate_pkg") checkrate_pkg

### Get instance

Factory for the ``` CHECKRATE ``` interface can be accessed from the package checkrate_pkg.

```go
checkRate := checkrate_pkg.NewCHECKRATE()
```

### <a name="create_check_rate"></a>![Method: ](https://apidocs.io/img/method.png ".checkrate_pkg.CreateCheckRate") CreateCheckRate

> *Tags:*  ``` Skips Authentication ``` 

> CheckRate


```go
func (me *CHECKRATE_IMPL) CreateCheckRate(
            body *models_pkg.CheckRateRequest,
            accept string,
            apiKey string,
            xSignature string,
            contentType string,
            acceptEncoding string)(*models_pkg.CheckRateResponse,error)
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

```go
bodyValue := []byte("{\n  \"rooms\": [{\n    \"rateKey\": \"20171115|20171120|W|52|1|SGL.ST|CG-EXT LONG RO|RO||1~1~0||N@A8921A639A0D46D88735806D109FA6E81544\"\n  }]\n}")
var body *models_pkg.CheckRateRequest
json.Unmarshal(bodyValue,&body)
accept := "application/json"
apiKey := "{{Api-key}}"
xSignature := "{{X-Signature}}"
contentType := "application/json"
acceptEncoding := "gzip"

var result *models_pkg.CheckRateResponse
result,_ = checkRate.CreateCheckRate(body, accept, apiKey, xSignature, contentType, acceptEncoding)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="availability_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".availability_pkg") availability_pkg

### Get instance

Factory for the ``` AVAILABILITY ``` interface can be accessed from the package availability_pkg.

```go
availability := availability_pkg.NewAVAILABILITY()
```

### <a name="create_other_filters"></a>![Method: ](https://apidocs.io/img/method.png ".availability_pkg.CreateOtherFilters") CreateOtherFilters

> *Tags:*  ``` Skips Authentication ``` 

> Other filters


```go
func (me *AVAILABILITY_IMPL) CreateOtherFilters(
            body *models_pkg.OtherFiltersRequest,
            accept string,
            apiKey string,
            xSignature string,
            contentType string,
            acceptEncoding string)(*models_pkg.OtherFiltersResponse,error)
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

```go
bodyValue := []byte("{\n  \"stay\": {\n    \"checkIn\": \"2017-11-15\",\n    \"checkOut\": \"2017-11-20\",\n    \"shiftDays\": \"2\"\n  },\n  \"occupancies\": [{\n    \"rooms\": 1,\n    \"adults\": 1,\n    \"children\": 0\n  }],\n  \"hotels\": {\n    \"hotel\": [1,\n    271]\n  },\n  \"filter\": {\n    \"minRate\": 100.000,\n    \"maxRate\": 1700.000,\n    \"minCategory\": 3,\n    \"maxCategory\": 5,\n    \"maxRooms\":3,\n    \"maxRatesPerRoom\": 3,\n    \"paymentType\": \"AT_HOTEL\",\n    \"packaging\": true,\n    \"hotelPackage\": \"YES\",\n    \"contract\": \"CG-FIT B2B\"\n  }\n}")
var body *models_pkg.OtherFiltersRequest
json.Unmarshal(bodyValue,&body)
accept := "application/json"
apiKey := "{{Api-key}}"
xSignature := "{{X-Signature}}"
contentType := "application/json"
acceptEncoding := "gzip"

var result *models_pkg.OtherFiltersResponse
result,_ = availability.CreateOtherFilters(body, accept, apiKey, xSignature, contentType, acceptEncoding)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="misc_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".misc_pkg") misc_pkg

### Get instance

Factory for the ``` MISC ``` interface can be accessed from the package misc_pkg.

```go
misc := misc_pkg.NewMISC()
```

### <a name="get0_status"></a>![Method: ](https://apidocs.io/img/method.png ".misc_pkg.Get0Status") Get0Status

> *Tags:*  ``` Skips Authentication ``` 

> 0. Status


```go
func (me *MISC_IMPL) Get0Status(
            accept string,
            apiKey string,
            xSignature string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| accept |  ``` Required ```  | TODO: Add a parameter description |
| apiKey |  ``` Required ```  | TODO: Add a parameter description |
| xSignature |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
accept := "application/json"
apiKey := "{{Api-key}}"
xSignature := "{{X-Signature}}"

var result 
result,_ = misc.Get0Status(accept, apiKey, xSignature)

```


[Back to List of Controllers](#list_of_controllers)



