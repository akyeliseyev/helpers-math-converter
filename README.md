English | [Русский](https://github.com/cs-eliseev/helpers-math-converter/blob/master/README.ru_RU.md)

MATH CONVERTER CSE HELPERS
=======

[![Travis (.org)](https://img.shields.io/travis/cs-eliseev/helpers-math-converter.svg?style=flat-square)](https://travis-ci.org/cs-eliseev/helpers-math-converter)
[![Codecov](https://img.shields.io/codecov/c/github/cs-eliseev/helpers-math-converter.svg?style=flat-square)](https://codecov.io/gh/cs-eliseev/helpers-math-converter)
[![Scrutinizer code quality](https://img.shields.io/scrutinizer/g/cs-eliseev/helpers-math-converter.svg?style=flat-square)](https://scrutinizer-ci.com/g/cs-eliseev/helpers-math-converter/?branch=master)

[![Packagist](https://img.shields.io/packagist/v/cse/helpers-math-converter.svg?style=flat-square)](https://packagist.org/packages/cse/helpers-math-converter)
[![Minimum PHP Version](https://img.shields.io/badge/php-%3E%3D%207.1-8892BF.svg?style=flat-square)](https://packagist.org/packages/cse/helpers-math-converter)
[![Packagist](https://img.shields.io/packagist/l/cse/helpers-math-converter.svg?style=flat-square)](https://github.com/cs-eliseev/helpers-math-converter/blob/master/LICENSE.md)
[![GitHub repo size](https://img.shields.io/github/repo-size/cs-eliseev/helpers-math-converter.svg?style=flat-square)](https://github.com/cs-eliseev/helpers-math-converter/archive/master.zip)

A mathematics helpers, providing functionality for numbers converter.

Project repository: https://github.com/cs-eliseev/helpers-math-converter

**DEMO**
```php
$mb = MathConverter::toMb('300K');
$sub = bcsub(
    MathConverter::roundDecimal($mb, 4),    // 0.293
    MathConverter::cutDecimal($mb, 4),      // 0.2929
    4
);
// 0.0001
MathConverter::binToHex($sub);
// 302e30303031
```
***

## Introduction

[CSE HELPERS](https://github.com/cs-eliseev/helpers/blob/master/README.md) is a collection of several libraries with simple functions written in PHP for people.

Despite using PHP as the main programming language for the Internet, its functions are not enough. MATH CONVERTER CSE HELPERS providing functionality for numbers converter.

[CSE HELPERS](https://github.com/cs-eliseev/helpers/blob/master/README.md) was created for the rapid development of web applications.

**CSE Helpers project:**
* [Array CSE helpers](https://github.com/cs-eliseev/helpers-arrays)
* [Cookie CSE helpers](https://github.com/cs-eliseev/helpers-cookie)
* [Date CSE helpers](https://github.com/cs-eliseev/helpers-date)
* [Email CSE helpers](https://github.com/cs-eliseev/helpers-email)
* [IP CSE helpers](https://github.com/cs-eliseev/helpers-ip)
* [Json CSE helpers](https://github.com/cs-eliseev/helpers-json)
* [Math Converter CSE helpers](https://github.com/cs-eliseev/helpers-math-converter)
* [Phone CSE helpers](https://github.com/cs-eliseev/helpers-phone)
* [Request CSE helpers](https://github.com/cs-eliseev/helpers-request)
* [Session CSE helpers](https://github.com/cs-eliseev/helpers-session)
* [Word CSE helpers](https://github.com/cs-eliseev/helpers-word)

Below you will find some information on how to init library and perform common commands.

## Install

You can find the most recent version of this project [here](https://github.com/cs-eliseev/helpers-math-converter).

### Composer

Execute the following command to get the latest version of the package:
```bash
composer require cse/helpers-math-converter
```

Or file composer.json should include the following contents:
```json
{
    "require": {
        "cse/helpers-math-converter": "*"
    }
}
```

### Git

Clone this repository locally:
```bash
git clone https://github.com/cs-eliseev/helpers-math-converter.git
```

### Download

[Download the latest release here](https://github.com/cs-eliseev/helpers-math-converter/archive/master.zip).

## Usage

The class consists of static methods that are conveniently used in any project. See example [examples-math-converter.php](https://github.com/cs-eliseev/helpers-math-converter/blob/master/examples/examples-math-converter.php).

**Convert HEX TO BINARY**

Example:
```php
MathConverter::hexToBin('48454c4c4f');
// HELLO
```

**Convert BINARY TO HEX**

Example:
```php
MathConverter::binToHex('HELLO');
// 48454c4c4f
```

**Convert MEGABYTES TO BYTES**

Example:
```php
MathConverter::mbToBytes(1);
// 1048576
```

**Convert BYTES TO MEGABYTES**

Example:
```php
MathConverter::bytesToMb(1048576);
// 1
```

Change decimal:
```php
MathConverter::bytesToMb(1000000, 4);
// 0.9537
```

**Convert GIGABYTES TO BYTES**

Example:
```php
MathConverter::gbToBytes(1);
// 1073741824
```

**Convert BYTES TO GIGABYTES**

Example:
```php
MathConverter::bytesToGb(1073741824);
// 1
```

Change decimal:
```php
MathConverter::bytesToGb(1000000000, 4);
// 0.9313
```

**Convert GIGABYTES TO MEGABYTES**

Example:
```php
MathConverter::gbToMb(1);
// 1024
```

**Convert MEGABYTES TO GIGABYTES**

Example:
```php
MathConverter::mbToGb(1024);
// 1
```

Change decimal:
```php
MathConverter::mbToGb(1000, 4);
// 0.9766
```

**Convert TO MEGABYTES**

Example:
```php
MathConverter::toMb('1M');
// 1
```

Petabyte to megabyte:
```php
MathConverter::toMb('0.001P');
// 1073741.824
```

Terabyte to megabyte:
```php
MathConverter::toMb('0.1T');
// 104857.6.824
```

Gigabyte to megabyte:
```php
MathConverter::toMb('1G');
// 1024
```

Kilobyte to megabyte:
```php
MathConverter::toMb('1000K');
// 0.9765625
```

Byte to megabyte:
```php
MathConverter::toMb('1000000B');
// 0.95367431640625
```

**CUT DECIMAL**

Example:
```php
MathConverter::cutDecimal(11.726);
// 11.72
```

Change decimal:
```php
MathConverter::cutDecimal('-67.099', 1);
// -67
```

**ROUND DECIMAL**

Example:
```php
MathConverter::roundDecimal(11.726);
// 11.73
```

Change decimal:
```php
MathConverter::roundDecimal('-67.099', 0);
// -67
```


## Testing & Code Coverage

PHPUnit is used for unit testing. Unit tests ensure that class and methods does exactly what it is meant to do.

General PHPUnit documentation can be found at https://phpunit.de/documentation.html.

To run the PHPUnit unit tests, execute:
```bash
phpunit PATH/TO/PROJECT/tests/
```

If you want code coverage reports, use the following:
```bash
phpunit --coverage-html ./report PATH/TO/PROJECT/tests/
```

Used PHPUnit default config:
```bash
phpunit --configuration PATH/TO/PROJECT/phpunit.xml
```


## Donating

You can support this project [here](https://www.paypal.me/cseliseev/10usd). 
You can also help out by contributing to the project, or reporting bugs. 
Even voicing your suggestions for features is great. Anything to help is much appreciated.


## License

The MATH CONVERTER CSE HELPERS is open-source PHP library licensed under the MIT license. Please see [License File](https://github.com/cs-eliseev/helpers-math-converter/blob/master/LICENSE.md) for more information.

***

> GitHub [@cs-eliseev](https://github.com/cs-eliseev)