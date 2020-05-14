# Swagger\Client\AuthorizeApi

All URIs are relative to *https://cloud.smsflow.ilinaya.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**authorizePost**](AuthorizeApi.md#authorizePost) | **POST** /authorize | Get BEARER token


# **authorizePost**
> \Swagger\Client\Model\TokenResponse authorizePost($body)

Get BEARER token

Obtain token for API call. Token must be sent in every request in Authorization: Bearer <xxx> header, where <xxx> is your token. You may decode token to get token expiration. We use standard JWT

### Example
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

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\TokenRequest**](../Model/TokenRequest.md)| Username and password must be sent via json object |

### Return type

[**\Swagger\Client\Model\TokenResponse**](../Model/TokenResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

