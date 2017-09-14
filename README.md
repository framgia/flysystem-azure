[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE)

# Azure custom filesystem for Laravel 5

This is a Flysystem adapter for the Windows Azure.

Require Laravel 5

# Install

Install package
```bash
composer require framgia/flysystem-azure
```

Open **config/app.php** and add this to providers section

```
Framgia\Flysystem\Azure\AzureServiceProvider::class,
```

Open **config/filesystems.php** and add this stuff to disks section
```
'azure' => [
    'driver' => 'azure',
    'name' => env('AZURE_STORAGE_NAME'),
    'key' => env('AZURE_STORAGE_KEY'),
    'container' => env('AZURE_STORAGE_CONTAINER', ''),
    'service_url' => env('AZURE_STORAGE_SERVICE_URL'),
]
```

Edit **.env** and add variables
```
AZURE_STORAGE_NAME=
AZURE_STORAGE_KEY=
AZURE_STORAGE_CONTAINER=
AZURE_STORAGE_SERVICE_URL=https://{namespace}.blob.core.windows.net
```
