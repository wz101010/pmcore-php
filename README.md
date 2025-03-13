# PMCore-Client

No description provided (generated by Openapi Generator https://github.com/openapitools/openapi-generator)


## Installation & Usage

### Requirements

PHP 7.4 and later.
Should also work with PHP 8.0.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https:////.git"
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
<?php
require_once('/path/to/PMCore-Client/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure Bearer authorization: Bearer
$config = PMCore\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new PMCore\Client\Api\FileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$app_key = 'app_key_example'; // string
$path = 'path_example'; // string | 

try {
    $result = $apiInstance->fileCreateFolder($app_key, $path);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FileApi->fileCreateFolder: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *https://api-staging.paomo.fun*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*FileApi* | [**fileCreateFolder**](docs/Api/FileApi.md#filecreatefolder) | **POST** /File/{appKey}/CreateFolder | 创建文件夹
*FileApi* | [**fileDelete**](docs/Api/FileApi.md#filedelete) | **DELETE** /File/{appKey} | 删除文件
*FileApi* | [**fileRename**](docs/Api/FileApi.md#filerename) | **POST** /File/{appKey}/Rename | 重命名文件
*FileApi* | [**fileUpload**](docs/Api/FileApi.md#fileupload) | **POST** /File/{appKey}/Upload | 上传文件
*FileApi* | [**files**](docs/Api/FileApi.md#files) | **GET** /File/{appKey} | 文件列表

## Models

- [JObjectApiResult](docs/Model/JObjectApiResult.md)

## Authorization

Authentication schemes defined for the API:
### Bearer

- **Type**: Bearer authentication

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `v1`
    - Package version: `1.0.7`
    - Generator version: `7.12.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
