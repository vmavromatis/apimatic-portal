# Getting started

APItude complete postman collection, with both BookingAPI & ContentAPI. You have the full details of our API in our developer portal:
https://developer.hotelbeds.com/docs?hotel

## How to Build


You must have Python 2 >=2.7.9 or Python 3 >=3.4 installed on your system to install and run this SDK. This SDK package depends on other Python packages like nose, jsonpickle etc. 
These dependencies are defined in the ```requirements.txt``` file that comes with the SDK.
To resolve these dependencies, you can use the PIP Dependency manager. Install it by following steps at [https://pip.pypa.io/en/stable/installing/](https://pip.pypa.io/en/stable/installing/).

Python and PIP executables should be defined in your PATH. Open command prompt and type ```pip --version```.
This should display the version of the PIP Dependency Manager installed if your installation was successful and the paths are properly defined.

* Using command line, navigate to the directory containing the generated files (including ```requirements.txt```) for the SDK.
* Run the command ```pip install -r requirements.txt```. This should install all the required dependencies.

![Building SDK - Step 1](https://apidocs.io/illustration/python?step=installDependencies&workspaceFolder=APItude%20BookingAPI%20Swagger-Python)


## How to Use

The following section explains how to use the Apitudebookingapiswagger SDK package in a new project.

### 1. Open Project in an IDE

Open up a Python IDE like PyCharm. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

![Open project in PyCharm - Step 1](https://apidocs.io/illustration/python?step=pyCharm)

Click on ```Open``` in PyCharm to browse to your generated SDK directory and then click ```OK```.

![Open project in PyCharm - Step 2](https://apidocs.io/illustration/python?step=openProject0&workspaceFolder=APItude%20BookingAPI%20Swagger-Python)     

The project files will be displayed in the side bar as follows:

![Open project in PyCharm - Step 3](https://apidocs.io/illustration/python?step=openProject1&workspaceFolder=APItude%20BookingAPI%20Swagger-Python&projectName=apitudebookingapiswagger)     

### 2. Add a new Test Project

Create a new directory by right clicking on the solution name as shown below:

![Add a new project in PyCharm - Step 1](https://apidocs.io/illustration/python?step=createDirectory&workspaceFolder=APItude%20BookingAPI%20Swagger-Python&projectName=apitudebookingapiswagger)

Name the directory as "test"

![Add a new project in PyCharm - Step 2](https://apidocs.io/illustration/python?step=nameDirectory)
   
Add a python file to this project with the name "testsdk"

![Add a new project in PyCharm - Step 3](https://apidocs.io/illustration/python?step=createFile&workspaceFolder=APItude%20BookingAPI%20Swagger-Python&projectName=apitudebookingapiswagger)

Name it "testsdk"

![Add a new project in PyCharm - Step 4](https://apidocs.io/illustration/python?step=nameFile)

In your python file you will be required to import the generated python library using the following code lines

```Python
from apitudebookingapiswagger.apitudebookingapiswagger_client import ApitudebookingapiswaggerClient
```

![Add a new project in PyCharm - Step 4](https://apidocs.io/illustration/python?step=projectFiles&workspaceFolder=APItude%20BookingAPI%20Swagger-Python&libraryName=apitudebookingapiswagger.apitudebookingapiswagger_client&projectName=apitudebookingapiswagger)

After this you can write code to instantiate an API client object, get a controller object and  make API calls. Sample code is given in the subsequent sections.

### 3. Run the Test Project

To run the file within your test project, right click on your Python file inside your Test project and click on ```Run```

![Run Test Project - Step 1](https://apidocs.io/illustration/python?step=runProject&workspaceFolder=APItude%20BookingAPI%20Swagger-Python&libraryName=apitudebookingapiswagger.apitudebookingapiswagger_client&projectName=apitudebookingapiswagger)


## How to Test

You can test the generated SDK and the server with automatically generated test
cases. unittest is used as the testing framework and nose is used as the test
runner. You can run the tests as follows:

  1. From terminal/cmd navigate to the root directory of the SDK.
  2. Invoke 'pip install -r test-requirements.txt'
  3. Invoke 'nosetests'

## Initialization

### 

API client can be initialized as following.

```python

client = ApitudebookingapiswaggerClient()
```



# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [PostBookingOperationsController](#post_booking_operations_controller)
* [BookingController](#booking_controller)
* [CheckRateController](#check_rate_controller)
* [AvailabilityController](#availability_controller)
* [MiscController](#misc_controller)

## <a name="post_booking_operations_controller"></a>![Class: ](https://apidocs.io/img/class.png ".PostBookingOperationsController") PostBookingOperationsController

### Get controller instance

An instance of the ``` PostBookingOperationsController ``` class can be accessed from the API Client.

```python
 post_booking_operations_client = client.post_booking_operations
```

### <a name="get_booking_list"></a>![Method: ](https://apidocs.io/img/method.png ".PostBookingOperationsController.get_booking_list") get_booking_list

> *Tags:*  ``` Skips Authentication ``` 

> BookingList

```python
def get_booking_list(self,
                         start,
                         end,
                         filter_type,
                         status,
                         mfrom,
                         to,
                         accept,
                         api_key,
                         x_signature)
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

```python
start = 2017-08-15
end = 2017-09-10
filter_type = 'CREATION'
status = 'ALL'
mfrom = 1
to = 25
accept = 'application/json'
api_key = '{{Api-key}}'
x_signature = '{{X-Signature}}'

post_booking_operations_client.get_booking_list(start, end, filter_type, status, mfrom, to, accept, api_key, x_signature)

```


### <a name="delete_booking_cancellation"></a>![Method: ](https://apidocs.io/img/method.png ".PostBookingOperationsController.delete_booking_cancellation") delete_booking_cancellation

> *Tags:*  ``` Skips Authentication ``` 

> BookingCancellation

```python
def delete_booking_cancellation(self,
                                    cancellation_flag,
                                    language,
                                    accept,
                                    api_key,
                                    x_signature,
                                    booking_reference)
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

```python
cancellation_flag = 'cancellationFlag'
language = 'language'
accept = 'Accept'
api_key = 'Api-key'
x_signature = 'X-Signature'
booking_reference = 'booking_reference'

post_booking_operations_client.delete_booking_cancellation(cancellation_flag, language, accept, api_key, x_signature, booking_reference)

```


### <a name="update_booking_change"></a>![Method: ](https://apidocs.io/img/method.png ".PostBookingOperationsController.update_booking_change") update_booking_change

> *Tags:*  ``` Skips Authentication ``` 

> BookingChange

```python
def update_booking_change(self,
                              body,
                              accept,
                              api_key,
                              x_signature,
                              content_type,
                              accept_encoding,
                              booking_reference)
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

```python
body = BookingChangeRequest()
accept = 'Accept'
api_key = 'Api-key'
x_signature = 'X-Signature'
content_type = 'Content-Type'
accept_encoding = 'Accept-Encoding'
booking_reference = 'booking_reference'

result = post_booking_operations_client.update_booking_change(body, accept, api_key, x_signature, content_type, accept_encoding, booking_reference)

```


### <a name="get_booking_detail"></a>![Method: ](https://apidocs.io/img/method.png ".PostBookingOperationsController.get_booking_detail") get_booking_detail

> *Tags:*  ``` Skips Authentication ``` 

> BookingDetail

```python
def get_booking_detail(self,
                           accept,
                           api_key,
                           x_signature,
                           booking_reference)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| accept |  ``` Required ```  | TODO: Add a parameter description |
| apiKey |  ``` Required ```  | TODO: Add a parameter description |
| xSignature |  ``` Required ```  | TODO: Add a parameter description |
| bookingReference |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
accept = 'Accept'
api_key = 'Api-key'
x_signature = 'X-Signature'
booking_reference = 'booking_reference'

post_booking_operations_client.get_booking_detail(accept, api_key, x_signature, booking_reference)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="booking_controller"></a>![Class: ](https://apidocs.io/img/class.png ".BookingController") BookingController

### Get controller instance

An instance of the ``` BookingController ``` class can be accessed from the API Client.

```python
 booking_client = client.booking
```

### <a name="create_booking"></a>![Method: ](https://apidocs.io/img/method.png ".BookingController.create_booking") create_booking

> *Tags:*  ``` Skips Authentication ``` 

> Booking

```python
def create_booking(self,
                       body,
                       accept,
                       api_key,
                       x_signature,
                       content_type,
                       accept_encoding)
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

```python
body_value = "{\n  \"holder\": {\n    \"name\": \"IntegrationTestFirstName\",\n    \"surname\": \"IntegrationTestLastName\"\n  },\n  \"rooms\": [{\n    \"rateKey\": \"20171115|20171120|W|52|1|DBL.ST|ID_B2B_25|RO|EM4TIES|1~1~0||N@1884739731\",\n    \"paxes\": [{\n      \"roomId\": \"1\",\n      \"type\": \"AD\",\n      \"name\": \"Adult Name\"\n    }]\n  }],\n  \"clientReference\": \"IntegrationAgency\"\n}"
body = json.loads(body_value)
accept = 'application/json'
api_key = '{{Api-key}}'
x_signature = '{{X-Signature}}'
content_type = 'application/json'
accept_encoding = 'gzip'

result = booking_client.create_booking(body, accept, api_key, x_signature, content_type, accept_encoding)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="check_rate_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CheckRateController") CheckRateController

### Get controller instance

An instance of the ``` CheckRateController ``` class can be accessed from the API Client.

```python
 check_rate_client = client.check_rate
```

### <a name="create_check_rate"></a>![Method: ](https://apidocs.io/img/method.png ".CheckRateController.create_check_rate") create_check_rate

> *Tags:*  ``` Skips Authentication ``` 

> CheckRate

```python
def create_check_rate(self,
                          body,
                          accept,
                          api_key,
                          x_signature,
                          content_type,
                          accept_encoding)
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

```python
body_value = "{\n  \"rooms\": [{\n    \"rateKey\": \"20171115|20171120|W|52|1|SGL.ST|CG-EXT LONG RO|RO||1~1~0||N@A8921A639A0D46D88735806D109FA6E81544\"\n  }]\n}"
body = json.loads(body_value)
accept = 'application/json'
api_key = '{{Api-key}}'
x_signature = '{{X-Signature}}'
content_type = 'application/json'
accept_encoding = 'gzip'

result = check_rate_client.create_check_rate(body, accept, api_key, x_signature, content_type, accept_encoding)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="availability_controller"></a>![Class: ](https://apidocs.io/img/class.png ".AvailabilityController") AvailabilityController

### Get controller instance

An instance of the ``` AvailabilityController ``` class can be accessed from the API Client.

```python
 availability_client = client.availability
```

### <a name="create_other_filters"></a>![Method: ](https://apidocs.io/img/method.png ".AvailabilityController.create_other_filters") create_other_filters

> *Tags:*  ``` Skips Authentication ``` 

> Other filters

```python
def create_other_filters(self,
                             body,
                             accept,
                             api_key,
                             x_signature,
                             content_type,
                             accept_encoding)
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

```python
body_value = "{\n  \"stay\": {\n    \"checkIn\": \"2017-11-15\",\n    \"checkOut\": \"2017-11-20\",\n    \"shiftDays\": \"2\"\n  },\n  \"occupancies\": [{\n    \"rooms\": 1,\n    \"adults\": 1,\n    \"children\": 0\n  }],\n  \"hotels\": {\n    \"hotel\": [1,\n    271]\n  },\n  \"filter\": {\n    \"minRate\": 100.000,\n    \"maxRate\": 1700.000,\n    \"minCategory\": 3,\n    \"maxCategory\": 5,\n    \"maxRooms\":3,\n    \"maxRatesPerRoom\": 3,\n    \"paymentType\": \"AT_HOTEL\",\n    \"packaging\": true,\n    \"hotelPackage\": \"YES\",\n    \"contract\": \"CG-FIT B2B\"\n  }\n}"
body = json.loads(body_value)
accept = 'application/json'
api_key = '{{Api-key}}'
x_signature = '{{X-Signature}}'
content_type = 'application/json'
accept_encoding = 'gzip'

result = availability_client.create_other_filters(body, accept, api_key, x_signature, content_type, accept_encoding)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="misc_controller"></a>![Class: ](https://apidocs.io/img/class.png ".MiscController") MiscController

### Get controller instance

An instance of the ``` MiscController ``` class can be accessed from the API Client.

```python
 misc_client = client.misc
```

### <a name="get_0_status"></a>![Method: ](https://apidocs.io/img/method.png ".MiscController.get_0_status") get_0_status

> *Tags:*  ``` Skips Authentication ``` 

> 0. Status

```python
def get_0_status(self,
                     accept,
                     api_key,
                     x_signature)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| accept |  ``` Required ```  | TODO: Add a parameter description |
| apiKey |  ``` Required ```  | TODO: Add a parameter description |
| xSignature |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
accept = 'application/json'
api_key = '{{Api-key}}'
x_signature = '{{X-Signature}}'

misc_client.get_0_status(accept, api_key, x_signature)

```


[Back to List of Controllers](#list_of_controllers)



