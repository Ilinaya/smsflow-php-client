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
      "url": "https://github.com/Ilinaya/smsflow-php-client.git"
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

## Documentation For Authorization

Visit  [Documentation page](https://smsflow.ilinaya.com/docs) to get API reference

Register at  [SMSFlow portal](https://cloud.smsflow.ilinaya.com/) to get API key


## apiKey

- **Type**: API key
- **API key parameter name**: Authorization: Bearer <API_KEY>
- **Location**: HTTP header


## Author

all@ilinaya.com


