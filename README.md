# [RaggiTech] Laravel-Locatable.

#  [![Latest Stable Version](https://poser.pugx.org/raggitech/laravel-locatable/v/stable)](https://packagist.org/packages/raggitech/laravel-locatable) [![Total Downloads](https://poser.pugx.org/raggitech/laravel-locatable/downloads)](https://packagist.org/packages/raggitech/laravel-locatable) [![License](https://poser.pugx.org/raggitech/laravel-locatable/license)](https://packagist.org/packages/raggitech/laravel-locatable)

#### Locatable provides a quick and easy methods.


## Install

Install the latest version using [Composer](https://getcomposer.org/):

```bash
$ composer require raggitech/laravel-locatable
```



## Supported Languages

- Arabic
- English




## Usage

- [TimeZone](#TZ)
- [Continents](#Continents)
- [Countries](#Countries)
- [States](#States)



<a name="TZ"></a>

#### TimeZone
###### function getTimeZones(?string $lang = null)

```php
$timezones = getTimeZones();

/**
*	...
*	+"Europe/Athens": "(UTC+02:00) Athens"
*	+"Europe/Bucharest": "(UTC+02:00) Bucharest"
*	+"Africa/Cairo": "(UTC+02:00) Cairo"
*	+"Africa/Harare": "(UTC+02:00) Harare"
*	+"Europe/Helsinki": "(UTC+02:00) Kyiv"
*	+"Europe/Istanbul": "(UTC+02:00) Istanbul"
*	+"Asia/Jerusalem": "(UTC+02:00) Jerusalem"
*	...
*/
```





<a name="Continents"></a>

#### Continents
###### function getContinents(?string $lang = null)
###### function getContinent(string $code, ?string $lang = null)

```php
$continents = getContinents();
/**
*	+"AF": "Africa"
*	+"AN": "Antarctica"
*	+"AS": "Asia"
*	...
*/

echo getContinent('AF', 'ar'); // أفريقيا
```





<a name="Countries"></a>

#### Countries
###### function getCountriesNames(?string $lang = null)
###### function function getCountries(?string $lang = null)
###### function getCountry(string $code, ?string $lang = null)

```php
$countriesNames = getCountriesNames();
/**
*	+"AF": "Afghanistan"
*	+"AX": "Aland Islands"
*	+"AL": "Albania"
*	+"DZ": "Algeria"
*	+"AS": "American Samoa"
*	...
*/

$countries = getCountries();
/**
*	...
*	    +"EG": array:9 [▼
*	    	"iso" => "EGY"
*	    	"name" => "Egypt"
*	    	"native" => "مصر‎"
*	    	"currency" => "EGP"
*	    	"phone" => "20"
*	    	"timezone" => "Africa/Cairo"
*	    	"languages" => array:1 [▼
*	    		0 => "AR"
*	    	]
*	    	"continent" => "AF"
*	    	"capital" => "Cairo"
*	    ]
*	...
*/

$country =  getCountry('EG', 'ar'); // Same result with "name" => "مصر"
```




<a name="States"></a>

#### States
###### function getStates(?string $country = null)
###### function getState(string $code, ?string $country = null)
```php
$states = getStates('EG');
/**
*	+"ALX": "Alexandria Governorate"
*	+"ASN": "Aswan Governorate"
*	+"AST": "Asyut Governorate"
*	.....
*/

echo getStates('ALX', 'EG'); // Alexandria Governorate
```




## License

[MIT license](LICENSE.md)