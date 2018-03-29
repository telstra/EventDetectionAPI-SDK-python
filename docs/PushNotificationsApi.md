# Telstra_EventDetection.PushNotificationsApi

All URIs are relative to *https://tapi.telstra.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**push_notifications**](PushNotificationsApi.md#push_notifications) | **POST** /v1/eventdetection/events/notifications | Push event notifications


# **push_notifications**
> PushNotificationObj push_notifications(content_type, body)

Push event notifications

Push event notifications to the notification URL configured during the MSISDN registration process

### Example
```python
from __future__ import print_function
import time
import Telstra_EventDetection
from Telstra_EventDetection.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = Telstra_EventDetection.PushNotificationsApi()
content_type = 'content_type_example' # str | application/json
body = Telstra_EventDetection.NotificationPayload() # NotificationPayload | Application Id, MSISDN, Event Id and Event Date

try:
    # Push event notifications
    api_response = api_instance.push_notifications(content_type, body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PushNotificationsApi->push_notifications: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **content_type** | **str**| application/json | 
 **body** | [**NotificationPayload**](NotificationPayload.md)| Application Id, MSISDN, Event Id and Event Date | 

### Return type

[**PushNotificationObj**](PushNotificationObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

