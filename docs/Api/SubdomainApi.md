# OpenAPI\Client\SubdomainApi

All URIs are relative to https://dynamicdns.pro/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**update()**](SubdomainApi.md#update) | **POST** /{subdomain}/record |  |
| [**updateip()**](SubdomainApi.md#updateip) | **POST** /{subdomain} | update the ip address with the connecting ip address |


## `update()`

```php
update($subdomain, $update_request): \OpenAPI\Client\Model\Update200Response
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer () authorization: http
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SubdomainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$subdomain = 'subdomain_example'; // string
$update_request = new \OpenAPI\Client\Model\UpdateRequest(); // \OpenAPI\Client\Model\UpdateRequest

try {
    $result = $apiInstance->update($subdomain, $update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubdomainApi->update: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **subdomain** | **string**|  | |
| **update_request** | [**\OpenAPI\Client\Model\UpdateRequest**](../Model/UpdateRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\Update200Response**](../Model/Update200Response.md)

### Authorization

[http](../../README.md#http)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateip()`

```php
updateip($subdomain, $body): \OpenAPI\Client\Model\Updateip200Response
```

update the ip address with the connecting ip address

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer () authorization: http
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SubdomainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$subdomain = 'subdomain_example'; // string
$body = array('key' => new \stdClass); // object

try {
    $result = $apiInstance->updateip($subdomain, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SubdomainApi->updateip: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **subdomain** | **string**|  | |
| **body** | **object**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\Updateip200Response**](../Model/Updateip200Response.md)

### Authorization

[http](../../README.md#http)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
