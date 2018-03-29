# Telstra_EventDetection.LongPollApi

All URIs are relative to *https://tapi.telstra.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**longpoll**](LongPollApi.md#longpoll) | **POST** /v1/eventdetection/events/{eventType} | Poll events


# **longpoll**
> GetEventResponse longpoll(event_type, body)

Poll events

Poll events for a given set of MSISDNs

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
api_instance = Telstra_EventDetection.LongPollApi(Telstra_EventDetection.ApiClient(configuration))
event_type = 'event_type_example' # str | Event Type
body = Telstra_EventDetection.PollingObj() # PollingObj | List of MSISDNs to pull the events

try:
    # Poll events
    api_response = api_instance.longpoll(event_type, body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling LongPollApi->longpoll: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **event_type** | **str**| Event Type | 
 **body** | [**PollingObj**](PollingObj.md)| List of MSISDNs to pull the events | 

### Return type

[**GetEventResponse**](GetEventResponse.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

