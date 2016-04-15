## Valitron: Easy Validation That Doesn't Suck

This is a Fork of https://github.com/vlucas/valitron

## Installation

Valitron uses [Composer](http://getcomposer.org) to install and update:

```
curl -s http://getcomposer.org/installer | php
php composer.phar require nirgendswo/valitron
```

## Reject

The validation always failed if there is any Data that is not set by the Rules.

## Defaults

Default values can be set for each Field, if the Field is not required.

```php
$validator = new Valitron\Validator(['name' => 'Chester Tester']);
$validator->setDefault('birthday', '10-01-2015');

```

You can also set Defaults as array,

```php
$defaults = ['birthday' => '10-01-2015'];

$validator = new Valitron\Validator(['name' => 'Chester Tester']);
$validator->setDefaults($defaults);

```

## arrayIn

Performs in_array check on given array values for an array

```php

$data = ['roles' => ['USER']];

$validator = new Valitron\Validator($data);
$validator->setRule('arrayIn', 'roles', ['USER', 'ADMIN']);
```

## Running Tests

The test suite depends on the Composer autoloader to load and run the
Valitron files. Please ensure you have downloaded and installed Composer
before running the tests:

1. Download Composer `curl -s http://getcomposer.org/installer | php`
2. Run 'install' `php composer.phar install`
3. Run the tests `phpunit`

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Make your changes
4. Run the tests, adding new ones for your own code if necessary (`phpunit`)
5. Commit your changes (`git commit -am 'Added some feature'`)
6. Push to the branch (`git push origin my-new-feature`)
7. Create new Pull Request
8. Pat yourself on the back for being so awesome

