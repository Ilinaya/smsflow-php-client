# Swagger\Client\PackagesApi

All URIs are relative to *https://cloud.smsflow.ilinaya.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**packagesBuyPost**](PackagesApi.md#packagesBuyPost) | **POST** /packages/buy | Purchase sms package
[**packagesGet**](PackagesApi.md#packagesGet) | **GET** /packages | Retrieve available packages
[**packagesHistoryGet**](PackagesApi.md#packagesHistoryGet) | **GET** /packages/history | Get sms package number purchase history


# **packagesBuyPost**
> \Swagger\Client\Model\PackagePurchaseResponse packagesBuyPost($body)

Purchase sms package

This method allows you to purchase SMS package

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: apiKey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\PackagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\PackagePurchaseRequest(); // \Swagger\Client\Model\PackagePurchaseRequest | order placed for purchasing the pet

try {
    $result = $apiInstance->packagesBuyPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PackagesApi->packagesBuyPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\PackagePurchaseRequest**](../Model/PackagePurchaseRequest.md)| order placed for purchasing the pet |

### Return type

[**\Swagger\Client\Model\PackagePurchaseResponse**](../Model/PackagePurchaseResponse.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **packagesGet**
> \Swagger\Client\Model\PackagesResponse packagesGet($page)

Retrieve available packages

Get available packages for your account

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: apiKey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\PackagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 8.14; // float | Specify Page number for results pagination

try {
    $result = $apiInstance->packagesGet($page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PackagesApi->packagesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **float**| Specify Page number for results pagination | [optional]

### Return type

[**\Swagger\Client\Model\PackagesResponse**](../Model/PackagesResponse.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **packagesHistoryGet**
> \Swagger\Client\Model\PackagePurchaseHistoryResponse packagesHistoryGet($page)

Get sms package number purchase history

Get sms package number purchase history

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: apiKey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\PackagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 8.14; // float | Specify Page number for results pagination

try {
    $result = $apiInstance->packagesHistoryGet($page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PackagesApi->packagesHistoryGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **float**| Specify Page number for results pagination | [optional]

### Return type

[**\Swagger\Client\Model\PackagePurchaseHistoryResponse**](../Model/PackagePurchaseHistoryResponse.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

