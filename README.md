# SocialiteProviders Snapchat Marketing API

[![License](http://poser.pugx.org/doctrine/inflector/license)](https://packagist.org/packages/doctrine/inflector) 
[![PHP Version Require](http://poser.pugx.org/doctrine/inflector/require/php)](https://packagist.org/packages/doctrine/inflector)

```bash
composer require yz/laravel-socialite-snapchat-marketing-api
```

## Installation & Basic Usage

Please see the [Base Installation Guide](https://socialiteproviders.com/usage/), then follow the provider specific instructions below.

### Add configuration to `config/services.php`

```php
'adobe' => [    
  'client_id' => env('ADOBE_CLIENT_ID'),  
  'client_secret' => env('ADOBE_CLIENT_SECRET'),  
  'redirect' => env('ADOBE_REDIRECT_URI') 
],
```

### Add provider event listener

Configure the package's listener to listen for `SocialiteWasCalled` events.

Add the event to your `listen[]` array in `app/Providers/EventServiceProvider`. See the [Base Installation Guide](https://socialiteproviders.com/usage/) for detailed instructions.

```php
protected $listen = [
    \SocialiteProviders\Manager\SocialiteWasCalled::class => [
        // ... other providers
        'SocialiteProviders\Adobe\AdobeApiExtendSocialite@handle@handle'
    ],
];
```

### Usage

You should now be able to use the provider like you would regularly use Socialite (assuming you have the facade installed):

```php
return Socialite::driver('adobe')->redirect();
```

### Returned User fields

WIP

### Use cases

WIP
