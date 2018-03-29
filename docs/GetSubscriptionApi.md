# Telstra_EventDetection.GetSubscriptionApi

All URIs are relative to *https://tapi.telstra.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_subscription**](GetSubscriptionApi.md#get_subscription) | **POST** /v1/eventdetection/events/subscriptions | Get Event Subscriptions


# **get_subscription**
> GetSubscriptionResponse get_subscription(body)

Get Event Subscriptions

Get the list of events subscribed for

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
api_instance = Telstra_EventDetection.GetSubscriptionApi(Telstra_EventDetection.ApiClient(configuration))
body = Telstra_EventDetection.PhoneNumberList() # PhoneNumberList | List of subscribed phone numbers

try:
    # Get Event Subscriptions
    api_response = api_instance.get_subscription(body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling GetSubscriptionApi->get_subscription: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**PhoneNumberList**](PhoneNumberList.md)| List of subscribed phone numbers | 

### Return type

[**GetSubscriptionResponse**](GetSubscriptionResponse.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

