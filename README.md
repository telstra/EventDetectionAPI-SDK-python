# Telstra_EventDetection

- API version: 1.0.0
- Package version: 1.0.0

## Requirements.

Python 2.7 and 3.4+

## Installation & Usage
### pip install


```sh
pip install git+https://github.com/Telstra/EventDetectionAPI-SDK-python.git
```
(you may need to run `pip` with root permission: `sudo pip install git+https://github.com/Telstra/EventDetectionAPI-SDK-python.git`)

```python
import Telstra_EventDetection 
```

### Setuptools

Install via [Setuptools](http://pypi.python.org/pypi/setuptools).

```sh
python setup.py install --user
```

```python
import Telstra_EventDetection
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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

## Documentation for API Endpoints

All URIs are relative to *https://tapi.telstra.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AuthenticationApi* | [**auth_token**](docs/AuthenticationApi.md#auth_token) | **POST** /v2/oauth/token | Generate authentication token
*GetSubscriptionApi* | [**get_subscription**](docs/GetSubscriptionApi.md#get_subscription) | **POST** /v1/eventdetection/events/subscriptions | Get Event Subscriptions
*LongPollApi* | [**longpoll**](docs/LongPollApi.md#longpoll) | **POST** /v1/eventdetection/events/{eventType} | Poll events
*PushNotificationsApi* | [**push_notifications**](docs/PushNotificationsApi.md#push_notifications) | **POST** /v1/eventdetection/events/notifications | Push event notifications
*RegistrationApi* | [**register**](docs/RegistrationApi.md#register) | **POST** /v1/eventdetection/events | Register
*RegistrationApi* | [**unregister**](docs/RegistrationApi.md#unregister) | **DELETE** /v1/eventdetection/events/{eventType} | Unregister


## Documentation For Models

 - [Eventsattr](docs/Eventsattr.md)
 - [GetEventResponse](docs/GetEventResponse.md)
 - [GetSubscriptionResponse](docs/GetSubscriptionResponse.md)
 - [NotificationPayload](docs/NotificationPayload.md)
 - [OAuthResponse](docs/OAuthResponse.md)
 - [PhoneNumberList](docs/PhoneNumberList.md)
 - [PollingObj](docs/PollingObj.md)
 - [PushNotificationObj](docs/PushNotificationObj.md)
 - [ResisterPhoneNumberList](docs/ResisterPhoneNumberList.md)
 - [ServiceEventsAttr](docs/ServiceEventsAttr.md)
 - [SubscriptionObj](docs/SubscriptionObj.md)
 - [Subscriptionattr](docs/Subscriptionattr.md)
 - [Test](docs/Test.md)
 - [UnregisterRequestObj](docs/UnregisterRequestObj.md)


## Documentation For Authorisation


## auth

- **Type**: OAuth
- **Flow**: application
- **Authorisation URL**: 
- **Scopes**: 
 - **v1_eventdetection_simswap**: v1_eventdetection_simswap


## Author



