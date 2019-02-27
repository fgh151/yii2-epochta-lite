Epochta lite
============
Lite version of Epochta sms sender.
Unlike [yii2-epochta](https://github.com/fgh151/yii2-epochta) this component can only send sms to one recipient.

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist fgh151/yii2-epochta-lite "*"
```

or add

```
"fgh151/yii2-epochta-lite": "*"
```

to the require section of your `composer.json` file.


Settings
-----

Add sms component to components section in config file:

```php
'components' => [
        'sms' => [
            'class' => \cfgh151\modules\epochta\Sms::class
        ]
    ],
```

Add settings to application params:

```php
return [
    'epochta-key' => 'your-epochta-key',
    'epochta-secret' => 'your-epochta-secret',
    'epochta-sender' => Sender Name,
];
```


Usage:
----
Once the extension is installed, simply use it in your code by  :


```php
Yii::$app->sms->send('Message text', '+9 (999) 999 99 99');
```