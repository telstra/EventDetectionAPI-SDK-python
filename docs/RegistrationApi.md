# Telstra_EventDetection.RegistrationApi

All URIs are relative to *https://tapi.telstra.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**register**](RegistrationApi.md#register) | **POST** /v1/eventdetection/events | Register
[**unregister**](RegistrationApi.md#unregister) | **DELETE** /v1/eventdetection/events/{eventType} | Unregister


# **register**
> ResisterPhoneNumberList register(body)

Register

Register for an event

### Example
```python
from __future__ import print_function
import time
import Telstra_EventDetection
from Telstra_EventDetection.rest import ApiException
from pprint import pprint

# Configure OAuth2 access token for authorization: auth
configuration = Telstra_EventDetection.Configuration()
configuration.access_token = 'YOUR_ACCESS_TOKEN'

# create an instance of the API class
api_instance = Telstra_EventDetection.RegistrationApi(Telstra_EventDetection.ApiClient(configuration))
body = Telstra_EventDetection.SubscriptionObj() # SubscriptionObj | Subscribe with a list of phone numbers, push notification URL (optional) and the event type.

try:
    # Register
    api_response = api_instance.register(body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling RegistrationApi->register: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**SubscriptionObj**](SubscriptionObj.md)| Subscribe with a list of phone numbers, push notification URL (optional) and the event type. | 

### Return type

[**ResisterPhoneNumberList**](ResisterPhoneNumberList.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **unregister**
> ResisterPhoneNumberList unregister(event_type, body)

Unregister

Unregister from an event

### Example
```python
from __future__ import print_function
import time
import Telstra_EventDetection
from Telstra_EventDetection.rest import ApiException
from pprint import pprint

# Configure OAuth2 access token for authorization: auth
configuration = Telstra_EventDetection.Configuration()
configuration.access_token = 'YOUR_ACCESS_TOKEN'

# create an instance of the API class
api_instance = Telstra_EventDetection.RegistrationApi(Telstra_EventDetection.ApiClient(configuration))
event_type = 'event_type_example' # str | Event Type
body = Telstra_EventDetection.UnregisterRequestObj() # UnregisterRequestObj | List of subscribed phone numbers and notification URL (optional)

try:
    # Unregister
    api_response = api_instance.unregister(event_type, body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling RegistrationApi->unregister: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **event_type** | **str**| Event Type | 
 **body** | [**UnregisterRequestObj**](UnregisterRequestObj.md)| List of subscribed phone numbers and notification URL (optional) | 

### Return type

[**ResisterPhoneNumberList**](ResisterPhoneNumberList.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

