# Getting started

APItude complete postman collection, with both BookingAPI & ContentAPI. You have the full details of our API in our developer portal:
https://developer.hotelbeds.com/docs?hotel

## How to Build

This client library is a Ruby gem which can be compiled and used in your Ruby and Ruby on Rails project. This library requires a few gems from the RubyGems repository.

1. Open the command line interface or the terminal and navigate to the folder containing the source code.
2. Run ``` gem build ap_itude_booking_api_swagger.gemspec ``` to build the gem.
3. Once built, the gem can be installed on the current work environment using ``` gem install ap_itude_booking_api_swagger-1.0.0.gem ```

![Building Gem](https://apidocs.io/illustration/ruby?step=buildSDK&workspaceFolder=APItude%20BookingAPI%20Swagger-Ruby&workspaceName=APItude%20BookingAPI%20Swagger-Ruby&projectName=ap_itude_booking_api_swagger&gemName=ap_itude_booking_api_swagger&gemVer=1.0.0)

## How to Use

The following section explains how to use the ApItudeBookingApiSwagger Ruby Gem in a new Rails project using RubyMine&trade;. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

### 1. Starting a new project

Close any existing projects in RubyMine&trade; by selecting ``` File -> Close Project ```. Next, click on ``` Create New Project ``` to create a new project from scratch.

![Create a new project in RubyMine](https://apidocs.io/illustration/ruby?step=createNewProject0&workspaceFolder=APItude%20BookingAPI%20Swagger-Ruby&workspaceName=ApItudeBookingApiSwagger&projectName=ap_itude_booking_api_swagger&gemName=ap_itude_booking_api_swagger&gemVer=1.0.0)

Next, provide ``` TestApp ``` as the project name, choose ``` Rails Application ``` as the project type, and click ``` OK ```.

![Create a new Rails Application in RubyMine - step 1](https://apidocs.io/illustration/ruby?step=createNewProject1&workspaceFolder=APItude%20BookingAPI%20Swagger-Ruby&workspaceName=ApItudeBookingApiSwagger&projectName=ap_itude_booking_api_swagger&gemName=ap_itude_booking_api_swagger&gemVer=1.0.0)

In the next dialog make sure that correct *Ruby SDK* is being used (minimum 2.0.0) and click ``` OK ```.

![Create a new Rails Application in RubyMine - step 2](https://apidocs.io/illustration/ruby?step=createNewProject2&workspaceFolder=APItude%20BookingAPI%20Swagger-Ruby&workspaceName=ApItudeBookingApiSwagger&projectName=ap_itude_booking_api_swagger&gemName=ap_itude_booking_api_swagger&gemVer=1.0.0)

This will create a new Rails Application project with an existing set of files and folder.

### 2. Add reference of the gem

In order to use the ApItudeBookingApiSwagger gem in the new project we must add a gem reference. Locate the ```Gemfile``` in the *Project Explorer* window under the ``` TestApp ``` project node. The file contains references to all gems being used in the project. Here, add the reference to the library gem by adding the following line: ``` gem 'ap_itude_booking_api_swagger', '~> 1.0.0' ```

![Add references of the Gemfile](https://apidocs.io/illustration/ruby?step=addReference&workspaceFolder=APItude%20BookingAPI%20Swagger-Ruby&workspaceName=ApItudeBookingApiSwagger&projectName=ap_itude_booking_api_swagger&gemName=ap_itude_booking_api_swagger&gemVer=1.0.0)

### 3. Adding a new Rails Controller

Once the ``` TestApp ``` project is created, a folder named ``` controllers ``` will be visible in the *Project Explorer* under the following path: ``` TestApp > app > controllers ```. Right click on this folder and select ``` New -> Run Rails Generator... ```.

![Run Rails Generator on Controllers Folder](https://apidocs.io/illustration/ruby?step=addCode0&workspaceFolder=APItude%20BookingAPI%20Swagger-Ruby&workspaceName=ApItudeBookingApiSwagger&projectName=ap_itude_booking_api_swagger&gemName=ap_itude_booking_api_swagger&gemVer=1.0.0)

Selecting the said option will popup a small window where the generator names are displayed. Here, select the ``` controller ``` template.

![Create a new Controller](https://apidocs.io/illustration/ruby?step=addCode1&workspaceFolder=APItude%20BookingAPI%20Swagger-Ruby&workspaceName=ApItudeBookingApiSwagger&projectName=ap_itude_booking_api_swagger&gemName=ap_itude_booking_api_swagger&gemVer=1.0.0)

Next, a popup window will ask you for a Controller name and included Actions. For controller name provide ``` Hello ``` and include an action named ``` Index ``` and click ``` OK ```.

![Add a new Controller](https://apidocs.io/illustration/ruby?step=addCode2&workspaceFolder=APItude%20BookingAPI%20Swagger-Ruby&workspaceName=ApItudeBookingApiSwagger&projectName=ap_itude_booking_api_swagger&gemName=ap_itude_booking_api_swagger&gemVer=1.0.0)

A new controller class anmed ``` HelloController ``` will be created in a file named ``` hello_controller.rb ``` containing a method named ``` Index ```. In this method, add code for initialization and a sample for its usage.

![Initialize the library](https://apidocs.io/illustration/ruby?step=addCode3&workspaceFolder=APItude%20BookingAPI%20Swagger-Ruby&workspaceName=ApItudeBookingApiSwagger&projectName=ap_itude_booking_api_swagger&gemName=ap_itude_booking_api_swagger&gemVer=1.0.0)

## How to Test

You can test the generated SDK and the server with automatically generated test
cases as follows:

  1. From terminal/cmd navigate to the root directory of the SDK.
  2. Invoke: `bundle exec rake`

## Initialization

### 

API client can be initialized as following.

```ruby

client = ApItudeBookingApiSwagger::ApItudeBookingApiSwaggerClient.new
```

The added initlization code can be debugged by putting a breakpoint in the ``` Index ``` method and running the project in debug mode by selecting ``` Run -> Debug 'Development: TestApp' ```.

![Debug the TestApp](https://apidocs.io/illustration/ruby?step=addCode4&workspaceFolder=APItude%20BookingAPI%20Swagger-Ruby&workspaceName=ApItudeBookingApiSwagger&projectName=ap_itude_booking_api_swagger&gemName=ap_itude_booking_api_swagger&gemVer=1.0.0&initLine=client%2520%253D%2520ApItudeBookingApiSwaggerClient.new)



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

```ruby
postBookingOperations = client.post_booking_operations
```

### <a name="get_booking_list"></a>![Method: ](https://apidocs.io/img/method.png ".PostBookingOperationsController.get_booking_list") get_booking_list

> *Tags:*  ``` Skips Authentication ``` 

> BookingList


```ruby
def get_booking_list(start,
                         mend,
                         filter_type,
                         status,
                         from,
                         to,
                         accept,
                         api_key,
                         x_signature); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| start |  ``` Required ```  | TODO: Add a parameter description |
| mend |  ``` Required ```  | TODO: Add a parameter description |
| filter_type |  ``` Required ```  | TODO: Add a parameter description |
| status |  ``` Required ```  | TODO: Add a parameter description |
| from |  ``` Required ```  | TODO: Add a parameter description |
| to |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |
| api_key |  ``` Required ```  | TODO: Add a parameter description |
| x_signature |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
start = 2017-08-15
mend = 2017-09-10
filter_type = 'CREATION'
status = 'ALL'
from = 1
to = 25
accept = 'application/json'
api_key = '{{Api-key}}'
x_signature = '{{X-Signature}}'

postBookingOperations.get_booking_list(start, mend, filter_type, status, from, to, accept, api_key, x_signature)

```


### <a name="delete_booking_cancellation"></a>![Method: ](https://apidocs.io/img/method.png ".PostBookingOperationsController.delete_booking_cancellation") delete_booking_cancellation

> *Tags:*  ``` Skips Authentication ``` 

> BookingCancellation


```ruby
def delete_booking_cancellation(cancellation_flag,
                                    language,
                                    accept,
                                    api_key,
                                    x_signature,
                                    booking_reference); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| cancellation_flag |  ``` Required ```  | TODO: Add a parameter description |
| language |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |
| api_key |  ``` Required ```  | TODO: Add a parameter description |
| x_signature |  ``` Required ```  | TODO: Add a parameter description |
| booking_reference |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
cancellation_flag = 'cancellationFlag'
language = 'language'
accept = 'Accept'
api_key = 'Api-key'
x_signature = 'X-Signature'
booking_reference = 'booking_reference'

postBookingOperations.delete_booking_cancellation(cancellation_flag, language, accept, api_key, x_signature, booking_reference)

```


### <a name="update_booking_change"></a>![Method: ](https://apidocs.io/img/method.png ".PostBookingOperationsController.update_booking_change") update_booking_change

> *Tags:*  ``` Skips Authentication ``` 

> BookingChange


```ruby
def update_booking_change(body,
                              accept,
                              api_key,
                              x_signature,
                              content_type,
                              accept_encoding,
                              booking_reference); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |
| api_key |  ``` Required ```  | TODO: Add a parameter description |
| x_signature |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| accept_encoding |  ``` Required ```  | TODO: Add a parameter description |
| booking_reference |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = BookingChangeRequest.new
accept = 'Accept'
api_key = 'Api-key'
x_signature = 'X-Signature'
content_type = 'Content-Type'
accept_encoding = 'Accept-Encoding'
booking_reference = 'booking_reference'

result = postBookingOperations.update_booking_change(body, accept, api_key, x_signature, content_type, accept_encoding, booking_reference)

```


### <a name="get_booking_detail"></a>![Method: ](https://apidocs.io/img/method.png ".PostBookingOperationsController.get_booking_detail") get_booking_detail

> *Tags:*  ``` Skips Authentication ``` 

> BookingDetail


```ruby
def get_booking_detail(accept,
                           api_key,
                           x_signature,
                           booking_reference); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| accept |  ``` Required ```  | TODO: Add a parameter description |
| api_key |  ``` Required ```  | TODO: Add a parameter description |
| x_signature |  ``` Required ```  | TODO: Add a parameter description |
| booking_reference |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
accept = 'Accept'
api_key = 'Api-key'
x_signature = 'X-Signature'
booking_reference = 'booking_reference'

postBookingOperations.get_booking_detail(accept, api_key, x_signature, booking_reference)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="booking_controller"></a>![Class: ](https://apidocs.io/img/class.png ".BookingController") BookingController

### Get singleton instance

The singleton instance of the ``` BookingController ``` class can be accessed from the API Client.

```ruby
booking = client.booking
```

### <a name="create_booking"></a>![Method: ](https://apidocs.io/img/method.png ".BookingController.create_booking") create_booking

> *Tags:*  ``` Skips Authentication ``` 

> Booking


```ruby
def create_booking(body,
                       accept,
                       api_key,
                       x_signature,
                       content_type,
                       accept_encoding); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |
| api_key |  ``` Required ```  | TODO: Add a parameter description |
| x_signature |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| accept_encoding |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body_value = "{\n  \"holder\": {\n    \"name\": \"IntegrationTestFirstName\",\n    \"surname\": \"IntegrationTestLastName\"\n  },\n  \"rooms\": [{\n    \"rateKey\": \"20171115|20171120|W|52|1|DBL.ST|ID_B2B_25|RO|EM4TIES|1~1~0||N@1884739731\",\n    \"paxes\": [{\n      \"roomId\": \"1\",\n      \"type\": \"AD\",\n      \"name\": \"Adult Name\"\n    }]\n  }],\n  \"clientReference\": \"IntegrationAgency\"\n}";
body = JSON.parse(body_value);
accept = 'application/json'
api_key = '{{Api-key}}'
x_signature = '{{X-Signature}}'
content_type = 'application/json'
accept_encoding = 'gzip'

result = booking.create_booking(body, accept, api_key, x_signature, content_type, accept_encoding)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="check_rate_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CheckRateController") CheckRateController

### Get singleton instance

The singleton instance of the ``` CheckRateController ``` class can be accessed from the API Client.

```ruby
checkRate = client.check_rate
```

### <a name="create_check_rate"></a>![Method: ](https://apidocs.io/img/method.png ".CheckRateController.create_check_rate") create_check_rate

> *Tags:*  ``` Skips Authentication ``` 

> CheckRate


```ruby
def create_check_rate(body,
                          accept,
                          api_key,
                          x_signature,
                          content_type,
                          accept_encoding); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |
| api_key |  ``` Required ```  | TODO: Add a parameter description |
| x_signature |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| accept_encoding |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body_value = "{\n  \"rooms\": [{\n    \"rateKey\": \"20171115|20171120|W|52|1|SGL.ST|CG-EXT LONG RO|RO||1~1~0||N@A8921A639A0D46D88735806D109FA6E81544\"\n  }]\n}";
body = JSON.parse(body_value);
accept = 'application/json'
api_key = '{{Api-key}}'
x_signature = '{{X-Signature}}'
content_type = 'application/json'
accept_encoding = 'gzip'

result = checkRate.create_check_rate(body, accept, api_key, x_signature, content_type, accept_encoding)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="availability_controller"></a>![Class: ](https://apidocs.io/img/class.png ".AvailabilityController") AvailabilityController

### Get singleton instance

The singleton instance of the ``` AvailabilityController ``` class can be accessed from the API Client.

```ruby
availability = client.availability
```

### <a name="create_other_filters"></a>![Method: ](https://apidocs.io/img/method.png ".AvailabilityController.create_other_filters") create_other_filters

> *Tags:*  ``` Skips Authentication ``` 

> Other filters


```ruby
def create_other_filters(body,
                             accept,
                             api_key,
                             x_signature,
                             content_type,
                             accept_encoding); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |
| api_key |  ``` Required ```  | TODO: Add a parameter description |
| x_signature |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| accept_encoding |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body_value = "{\n  \"stay\": {\n    \"checkIn\": \"2017-11-15\",\n    \"checkOut\": \"2017-11-20\",\n    \"shiftDays\": \"2\"\n  },\n  \"occupancies\": [{\n    \"rooms\": 1,\n    \"adults\": 1,\n    \"children\": 0\n  }],\n  \"hotels\": {\n    \"hotel\": [1,\n    271]\n  },\n  \"filter\": {\n    \"minRate\": 100.000,\n    \"maxRate\": 1700.000,\n    \"minCategory\": 3,\n    \"maxCategory\": 5,\n    \"maxRooms\":3,\n    \"maxRatesPerRoom\": 3,\n    \"paymentType\": \"AT_HOTEL\",\n    \"packaging\": true,\n    \"hotelPackage\": \"YES\",\n    \"contract\": \"CG-FIT B2B\"\n  }\n}";
body = JSON.parse(body_value);
accept = 'application/json'
api_key = '{{Api-key}}'
x_signature = '{{X-Signature}}'
content_type = 'application/json'
accept_encoding = 'gzip'

result = availability.create_other_filters(body, accept, api_key, x_signature, content_type, accept_encoding)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="misc_controller"></a>![Class: ](https://apidocs.io/img/class.png ".MiscController") MiscController

### Get singleton instance

The singleton instance of the ``` MiscController ``` class can be accessed from the API Client.

```ruby
misc = client.misc
```

### <a name="get_0_status"></a>![Method: ](https://apidocs.io/img/method.png ".MiscController.get_0_status") get_0_status

> *Tags:*  ``` Skips Authentication ``` 

> 0. Status


```ruby
def get_0_status(accept,
                     api_key,
                     x_signature); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| accept |  ``` Required ```  | TODO: Add a parameter description |
| api_key |  ``` Required ```  | TODO: Add a parameter description |
| x_signature |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
accept = 'application/json'
api_key = '{{Api-key}}'
x_signature = '{{X-Signature}}'

misc.get_0_status(accept, api_key, x_signature)

```


[Back to List of Controllers](#list_of_controllers)



