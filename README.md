# Laravel Multichain API

Laravel 5.x API wrapper package for the Multichain blockchain. Please read the Credits. 

## Features
- Simple Multichain JsonRPC interface.
- Full Multichain API implementation.

Note: Support for Multichain Version 2.0.  

## Example usage
```
$mchain = MultiChain::getInfo();
```

## Installation
Require the package 
``` bash
$ composer require eskie/laravel-multichain-api
```

Laravel has auto import providers and aliases settings so you don't need to add it manually.
But if there is an error please double check your `app.php`.

Manual Import of providers and aliases:
Add service provider class to `providers` section of `app.php` located in `config` directory 
``` 
'providers' => [
        .
        .
        .
		        Eskie\Multichain\MultiChainServiceProvider::class,
]
```
Add facade to `aliases` section of `app.php` located in `config` directory. 
``` 
'aliases' => [
        .
        .
        .
		        'MultiChain' => Eskie\Multichain\Facades\MultiChain::class,
]
```


Publish configuration file
``` bash
$ php artisan vendor:publish --tag=config
```
This will publish the `multichain.php` configuration file to `config` directory.

## Configuration
Edit `multichain.php` loated in the `config` directory providing the required credentials as per the `multichain.conf` file on the node you wish to access.

## Usage
Refer to the following documentation:

1. Multichain JSON-RPC API commands (http://www.multichain.com/developers/json-rpc-api/)

## Credits
I take no credit for this work - the real credits go to the folks Kunstmaan Labs who wrote the original php library (https://github.com/Kunstmaan/libphp-multichain) and Lehn (https://github.com/lenh/laravel-multichain-api).