# Ilinaya SMSFlow SMS API 
Ilinaya SMSFlow API


- API version: 1.0.0

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com//.git"
    }
  ],
  "require": {
    "/": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/SwaggerClient-php/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\AuthorizeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\TokenRequest(); // \Swagger\Client\Model\TokenRequest | Username and password must be sent via json object

try {
    $result = $apiInstance->authorizePost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthorizeApi->authorizePost: ', $e->getMessage(), PHP_EOL;
}

?>
```

## Documentation for API Endpoints

All URIs are relative to *https://cloud.smsflow.ilinaya.com/api*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AuthorizeApi* | [**authorizePost**](docs/Api/AuthorizeApi.md#authorizepost) | **POST** /authorize | Get BEARER token
*CallerIdsApi* | [**callerIdsGet**](docs/Api/CallerIdsApi.md#calleridsget) | **GET** /callerIds | Retrieve your caller IDs
*DidsApi* | [**didsAvailableGet**](docs/Api/DidsApi.md#didsavailableget) | **GET** /dids/available | Retrieve available for purchase
*DidsApi* | [**didsBuyPost**](docs/Api/DidsApi.md#didsbuypost) | **POST** /dids/buy | Purchase virutal number
*DidsApi* | [**didsGet**](docs/Api/DidsApi.md#didsget) | **GET** /dids | Retrieve your virtual numbers
*DidsApi* | [**didsSetcallbackPost**](docs/Api/DidsApi.md#didssetcallbackpost) | **POST** /dids/setcallback | Set HTTP callback for inbound SMS
*MessagesApi* | [**messagesGet**](docs/Api/MessagesApi.md#messagesget) | **GET** /messages | Retrieve sent and recieved messages
*MessagesApi* | [**messagesSendPost**](docs/Api/MessagesApi.md#messagessendpost) | **POST** /messages/send | Send Messages
*MessagesApi* | [**messagesStatusMessageIdGet**](docs/Api/MessagesApi.md#messagesstatusmessageidget) | **GET** /messages/status/{messageId} | Retrieve message
*PackagesApi* | [**packagesBuyPost**](docs/Api/PackagesApi.md#packagesbuypost) | **POST** /packages/buy | Purchase sms package
*PackagesApi* | [**packagesGet**](docs/Api/PackagesApi.md#packagesget) | **GET** /packages | Retrieve available packages
*PackagesApi* | [**packagesHistoryGet**](docs/Api/PackagesApi.md#packageshistoryget) | **GET** /packages/history | Get sms package number purchase history
*UsersApi* | [**usersBalanceGet**](docs/Api/UsersApi.md#usersbalanceget) | **GET** /users/balance | Retrieve financial information


## Documentation For Models

 - [AvailavbleCallerIdItem](docs/Model/AvailavbleCallerIdItem.md)
 - [AvailavbleDidItem](docs/Model/AvailavbleDidItem.md)
 - [AvailavleDidResponse](docs/Model/AvailavleDidResponse.md)
 - [BalanceResponse](docs/Model/BalanceResponse.md)
 - [CallerIdsResponse](docs/Model/CallerIdsResponse.md)
 - [Did](docs/Model/Did.md)
 - [DidDid](docs/Model/DidDid.md)
 - [DidPurchaseRequest](docs/Model/DidPurchaseRequest.md)
 - [DidPurchaseResponse](docs/Model/DidPurchaseResponse.md)
 - [DidPurchaseResponseDid](docs/Model/DidPurchaseResponseDid.md)
 - [DidResponse](docs/Model/DidResponse.md)
 - [DidResponseInfo](docs/Model/DidResponseInfo.md)
 - [DidSetCallbackRequest](docs/Model/DidSetCallbackRequest.md)
 - [DidSetCallbackResponse](docs/Model/DidSetCallbackResponse.md)
 - [Message](docs/Model/Message.md)
 - [MessageSendRequest](docs/Model/MessageSendRequest.md)
 - [MessageSendResponse](docs/Model/MessageSendResponse.md)
 - [MessageSendResponseMessageItem](docs/Model/MessageSendResponseMessageItem.md)
 - [MessageStatusResponse](docs/Model/MessageStatusResponse.md)
 - [MessagesResponse](docs/Model/MessagesResponse.md)
 - [Package](docs/Model/Package.md)
 - [PackagePurchaseHistoryResponse](docs/Model/PackagePurchaseHistoryResponse.md)
 - [PackagePurchaseRequest](docs/Model/PackagePurchaseRequest.md)
 - [PackagePurchaseResponse](docs/Model/PackagePurchaseResponse.md)
 - [PackagesResponse](docs/Model/PackagesResponse.md)
 - [PurchaseHistoryItem](docs/Model/PurchaseHistoryItem.md)
 - [PurchaseHistoryItemDid](docs/Model/PurchaseHistoryItemDid.md)
 - [PurchaseHistoryItemOrganizationUser](docs/Model/PurchaseHistoryItemOrganizationUser.md)
 - [PurchaseHistoryItemPackage](docs/Model/PurchaseHistoryItemPackage.md)
 - [TokenRequest](docs/Model/TokenRequest.md)
 - [TokenResponse](docs/Model/TokenResponse.md)
 - [User](docs/Model/User.md)


## Documentation For Authorization


## apiKey

- **Type**: API key
- **API key parameter name**: Authorization
- **Location**: HTTP header


## Author

all@ilinaya.com


