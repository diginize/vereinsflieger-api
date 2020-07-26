# DiginizeVereinsfliegerApi\MembersApi

All URIs are relative to *https://www.vereinsflieger.de/interface/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getMembers**](MembersApi.md#getMembers) | **POST** /user/list | 



## getMembers

> VereinsfliegerResponseDto getMembers()



Get a list of all members

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: access_token
$config = DiginizeVereinsfliegerApi\Configuration::getDefaultConfiguration()->setApiKey('accesstoken', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DiginizeVereinsfliegerApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('accesstoken', 'Bearer');


$apiInstance = new DiginizeVereinsfliegerApi\Api\MembersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getMembers();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MembersApi->getMembers: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**VereinsfliegerResponseDto**](../Model/VereinsfliegerResponseDto.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)

