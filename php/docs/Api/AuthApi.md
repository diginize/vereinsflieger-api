# DiginizeVereinsfliegerApi\AuthApi

All URIs are relative to *https://www.vereinsflieger.de/interface/rest*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getAccesstoken**](AuthApi.md#getAccesstoken) | **GET** /auth/accesstoken | 
[**getUser**](AuthApi.md#getUser) | **POST** /auth/getuser | 
[**signin**](AuthApi.md#signin) | **POST** /auth/signin | 
[**signout**](AuthApi.md#signout) | **DELETE** /auth/signout | 



## getAccesstoken

> VereinsfliegerResponseDto getAccesstoken()



Returns an accesstoken

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new DiginizeVereinsfliegerApi\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->getAccesstoken();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->getAccesstoken: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**VereinsfliegerResponseDto**](../Model/VereinsfliegerResponseDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## getUser

> VereinsfliegerResponseDto getUser()



Get details of the current user

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: access_token
$config = DiginizeVereinsfliegerApi\Configuration::getDefaultConfiguration()->setApiKey('accesstoken', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DiginizeVereinsfliegerApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('accesstoken', 'Bearer');


$apiInstance = new DiginizeVereinsfliegerApi\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getUser();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->getUser: ', $e->getMessage(), PHP_EOL;
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


## signin

> \DiginizeVereinsfliegerApi\Model\VereinsfliegerResponseDto signin($appkey, $username, $password, $cid, $auth_secret)



Login with access token

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: access_token
$config = DiginizeVereinsfliegerApi\Configuration::getDefaultConfiguration()->setApiKey('accesstoken', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DiginizeVereinsfliegerApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('accesstoken', 'Bearer');


$apiInstance = new DiginizeVereinsfliegerApi\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$appkey = 'appkey_example'; // string | Aplication secret. To obtain one, contact the support of Vereinsflieger.de
$username = 'username_example'; // string | 
$password = 'password_example'; // string | The md5 hashed password of the user
$cid = 56; // int | The club id. Only required if the user is member of multiple clubs
$auth_secret = 'auth_secret_example'; // string | The current OTP if 2FA is enabled for the user's account

try {
    $result = $apiInstance->signin($appkey, $username, $password, $cid, $auth_secret);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->signin: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **appkey** | **string**| Aplication secret. To obtain one, contact the support of Vereinsflieger.de |
 **username** | **string**|  |
 **password** | **string**| The md5 hashed password of the user |
 **cid** | **int**| The club id. Only required if the user is member of multiple clubs | [optional]
 **auth_secret** | **string**| The current OTP if 2FA is enabled for the user&#39;s account | [optional]

### Return type

[**\DiginizeVereinsfliegerApi\Model\VereinsfliegerResponseDto**](../Model/VereinsfliegerResponseDto.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

- **Content-Type**: application/x-www-form-urlencoded
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## signout

> \DiginizeVereinsfliegerApi\Model\VereinsfliegerResponseDto signout()



Logout with accesstoken

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: access_token
$config = DiginizeVereinsfliegerApi\Configuration::getDefaultConfiguration()->setApiKey('accesstoken', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DiginizeVereinsfliegerApi\Configuration::getDefaultConfiguration()->setApiKeyPrefix('accesstoken', 'Bearer');


$apiInstance = new DiginizeVereinsfliegerApi\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->signout();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->signout: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\DiginizeVereinsfliegerApi\Model\VereinsfliegerResponseDto**](../Model/VereinsfliegerResponseDto.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)

