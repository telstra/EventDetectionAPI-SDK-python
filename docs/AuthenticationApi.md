# Telstra_EventDetection.AuthenticationApi

All URIs are relative to *https://tapi.telstra.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**auth_token**](AuthenticationApi.md#auth_token) | **POST** /v2/oauth/token | Generate authentication token


# **auth_token**
> OAuthResponse auth_token(client_id, client_secret, grant_type)

Generate authentication token

Generate authentication token

### Example
```python
from __future__ import print_function
import time
import Telstra_EventDetection
from Telstra_EventDetection.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = Telstra_EventDetection.AuthenticationApi()
client_id = 'client_id_example' # str | 
client_secret = 'client_secret_example' # str | 
grant_type = 'client_credentials' # str |  (default to client_credentials)

try:
    # Generate authentication token
    api_response = api_instance.auth_token(client_id, client_secret, grant_type)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling AuthenticationApi->auth_token: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client_id** | **str**|  | 
 **client_secret** | **str**|  | 
 **grant_type** | **str**|  | [default to client_credentials]

### Return type

[**OAuthResponse**](OAuthResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

