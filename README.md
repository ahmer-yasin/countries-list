# country-data-list

[![Build Status](https://travis-ci.com/ahmer-yasin/countries-list.svg?branch=master)](https://travis-ci.com/ahmer-yasin/countries-list) [![Coverage Status](https://coveralls.io/repos/github/ahmer-yasin/countries-list/badge.svg?branch=master)](https://coveralls.io/github/ahmer-yasin/countries-list?branch=master)

Maps ISO 3166-1-alpha-2 codes to English country names and vice versa.

Uses data from https://www.iso.org/iso-3166-country-codes.html

### Looking for Version 1
You can find version 1.* of country-list [here](https://github.com/ahmer-yasin/countries-list/tree/1.x).

## Example

``` js
const { getCode, getName } = require('country-list');

console.log(getName('IS')); // Iceland
console.log(getCode('Iceland')); // IS
console.log(getCode('Nowhere-to-be-found-land')); // undefined
```

And how to change the name of a country 
``` js
const { overwrite, getName } = require('country-list');
overwrite([{
  code: 'TW',
  name: 'Taiwan'
}])

console.log(getName('TW')); // Taiwan
```

## Methods

Usage:

``` js
const countryList = require('country-list');
```
All input is case-insensitive.

### overwrite(countries)

Expects an array of country objects containing `code` and `name` properties.
``` js
[{
  code: 'TW',
  name: 'Taiwan'
}]
```

### getName(code)

Expects a two-digit country code.  
Returns the name for that country.  
If not found, it returns `undefined`.  

### getCode(name)

Expects the English country name.  
Returns the code for that country.  
If not found, it returns `undefined`.  

### getNames()

Returns an array of all country names.

### getCodes()

Returns an array of all country codes.

### getNameList()

Returns a key-value object of all countries using the name as key.

### getCodeList()

Returns a key-value object of all countries using the code as key.

### getData()

Returns an array of all country information, in the same format as it gets imported.

## Install

``` cli
npm install country-data-list
```

## Related Projects
 - [datasets/country-list](https://github.com/datasets/country-list)
 - [srcagency/iso-3166-1-codes](https://github.com/srcagency/iso-3166-1-codes)
 - [olahol/iso-3166-2.js](https://github.com/olahol/iso-3166-2.js)

## License

MIT

## Source
 - [ISO (International Organization for Standardization)](https://www.iso.org/iso-3166-country-codes.html)
>ISO makes the list of alpha-2 country codes available for internal use and non-commercial purposes free of charge.
