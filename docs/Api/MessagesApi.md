# Swagger\Client\MessagesApi

All URIs are relative to *https://cloud.smsflow.ilinaya.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**messagesGet**](MessagesApi.md#messagesGet) | **GET** /messages | Retrieve sent and recieved messages
[**messagesSendPost**](MessagesApi.md#messagesSendPost) | **POST** /messages/send | Send Messages
[**messagesStatusMessageIdGet**](MessagesApi.md#messagesStatusMessageIdGet) | **GET** /messages/status/{messageId} | Retrieve message


# **messagesGet**
> \Swagger\Client\Model\MessagesResponse messagesGet($page)

Retrieve sent and recieved messages

This method allows you to get paginated output of your messages

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: apiKey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\MessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 8.14; // float | Specify Page number for results pagination

try {
    $result = $apiInstance->messagesGet($page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->messagesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **float**| Specify Page number for results pagination | [optional]

### Return type

[**\Swagger\Client\Model\MessagesResponse**](../Model/MessagesResponse.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **messagesSendPost**
> \Swagger\Client\Model\MessageSendResponse messagesSendPost($body)

Send Messages

Method allows you to send text message to one or many destination numbers

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: apiKey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\MessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\MessageSendRequest(); // \Swagger\Client\Model\MessageSendRequest | order placed for purchasing the pet

try {
    $result = $apiInstance->messagesSendPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->messagesSendPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\MessageSendRequest**](../Model/MessageSendRequest.md)| order placed for purchasing the pet |

### Return type

[**\Swagger\Client\Model\MessageSendResponse**](../Model/MessageSendResponse.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **messagesStatusMessageIdGet**
> \Swagger\Client\Model\MessageStatusResponse messagesStatusMessageIdGet($message_id)

Retrieve message

This method allows you to get information about specific message

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: apiKey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new Swagger\Client\Api\MessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$message_id = 56; // int | Numeric ID of the user to get

try {
    $result = $apiInstance->messagesStatusMessageIdGet($message_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->messagesStatusMessageIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **message_id** | **int**| Numeric ID of the user to get |

### Return type

[**\Swagger\Client\Model\MessageStatusResponse**](../Model/MessageStatusResponse.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

