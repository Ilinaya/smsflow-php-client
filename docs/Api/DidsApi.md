# Swagger\Client\DidsApi

All URIs are relative to *https://cloud.smsflow.ilinaya.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**didsAvailableGet**](DidsApi.md#didsAvailableGet) | **GET** /dids/available | Retrieve available for purchase
[**didsBuyPost**](DidsApi.md#didsBuyPost) | **POST** /dids/buy | Purchase virutal number
[**didsGet**](DidsApi.md#didsGet) | **GET** /dids | Retrieve your virtual numbers
[**didsSetcallbackPost**](DidsApi.md#didsSetcallbackPost) | **POST** /dids/setcallback | Set HTTP callback for inbound SMS


# **didsAvailableGet**
> \Swagger\Client\Model\AvailavleDidResponse didsAvailableGet($page)

Retrieve available for purchase

This method allows you to get paginated output of availavle virtual numbers

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: apiKey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\DidsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 8.14; // float | Specify Page number for results pagination

try {
    $result = $apiInstance->didsAvailableGet($page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DidsApi->didsAvailableGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **float**| Specify Page number for results pagination | [optional]

### Return type

[**\Swagger\Client\Model\AvailavleDidResponse**](../Model/AvailavleDidResponse.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **didsBuyPost**
> \Swagger\Client\Model\DidPurchaseResponse didsBuyPost($body)

Purchase virutal number

This method allows you to purchase virutal number

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: apiKey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\DidsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\DidPurchaseRequest(); // \Swagger\Client\Model\DidPurchaseRequest | Provide didId

try {
    $result = $apiInstance->didsBuyPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DidsApi->didsBuyPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\DidPurchaseRequest**](../Model/DidPurchaseRequest.md)| Provide didId |

### Return type

[**\Swagger\Client\Model\DidPurchaseResponse**](../Model/DidPurchaseResponse.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **didsGet**
> \Swagger\Client\Model\DidResponse didsGet($page)

Retrieve your virtual numbers

This method allows you to get paginated output of your virtual numbers

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: apiKey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\DidsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 8.14; // float | Specify Page number for results pagination

try {
    $result = $apiInstance->didsGet($page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DidsApi->didsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **float**| Specify Page number for results pagination | [optional]

### Return type

[**\Swagger\Client\Model\DidResponse**](../Model/DidResponse.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **didsSetcallbackPost**
> \Swagger\Client\Model\DidSetCallbackResponse didsSetcallbackPost($body)

Set HTTP callback for inbound SMS

We wil forward all inbound messages to your HTTP(s) callback url

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: apiKey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\DidsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\DidSetCallbackRequest(); // \Swagger\Client\Model\DidSetCallbackRequest | Provide didId

try {
    $result = $apiInstance->didsSetcallbackPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DidsApi->didsSetcallbackPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\DidSetCallbackRequest**](../Model/DidSetCallbackRequest.md)| Provide didId |

### Return type

[**\Swagger\Client\Model\DidSetCallbackResponse**](../Model/DidSetCallbackResponse.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

