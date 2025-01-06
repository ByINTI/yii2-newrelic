Newrelic instrumentation for Yii 2
==================================

This extension describes routes, action params and instruments views with newrelic end user monitoring scripts.
Supports console and web applications.

For license information check the [LICENSE](LICENSE)-file.

Requirements
------------

Works with newrelic agent with version >=3.0

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist byinti/yii2-newrelic
```

or 

```
composer require --prefer-dist byinti/yii2-newrelic
```

or add

```json
"byinti/yii2-newrelic": "^1.0"
```

to the require section of your composer.json.


Configuration
-------------

To use this extension, you have to configure your components & bootstrap section your application configuration:

```php
return [
    'bootstrap' => ['newrelic'],
    'components' => [
        // ...
        'newrelic' => [
            'enableEndUser' => true, // MIND THIS! It is JS instrumentation for end user. Default is true.
            'class' => 'byinti\yii\newrelic\Newrelic',
            'name' => 'My App Frontend', // optional, uses Yii::$app->name by default
            'handler' => 'class/name', // optional, your custom handler
            'licence' => '...', // optional
            'enabled' => false // optional, default = true
        ]
    ],
];
```

Packagist Repository

https://packagist.org/packages/byinti/yii2-newrelic