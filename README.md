# jQuery Once [![NPM version](https://img.shields.io/npm/v/jquery-once.svg)](https://npmjs.org/package/jquery-once "View this project on NPM")

[![Build Status](https://img.shields.io/travis/RobLoach/jquery-once/master.svg)](http://travis-ci.org/RobLoach/jquery-once "Check this project's build status on TravisCI")
[![NPM downloads](https://img.shields.io/npm/dm/jquery-once.svg)](https://npmjs.org/package/jquery-once "View this project on NPM")
[![Dependency Status](https://img.shields.io/david/RobLoach/jquery-once.svg)](https://david-dm.org/RobLoach/jquery-once)
[![Coverage Status](https://coveralls.io/repos/RobLoach/jquery-once/badge.svg)](https://coveralls.io/r/RobLoach/jquery-once)

> Act on [jQuery](http://jquery.com) elements only once.

Filters out all elements that had the same filter applied on them before. It
can be used to ensure that a function is only applied once to an element.

## Install

Method | Installation
------ | ------------
[npm](http://npmjs.com/package/jquery-once) | `npm install jquery-once --save`
[Composer](https://packagist.org/packages/robloach/jquery-once) | `composer require jquery-once`
[Bower](http://bower.io/search/?q=jquery-once) | `bower install jquery-once`
[Component](https://github.com/componentjs/component) | `component install RobLoach/jquery-once`
[jsDelivr](http://www.jsdelivr.com/#!jquery.once) | `//cdn.jsdelivr.net/jquery.once/2.0.2/jquery.once.min.js`
[cdnjs](https://cdnjs.com/libraries/jquery-once) | `//cdnjs.cloudflare.com/ajax/libs/jquery-once/2.0.2/jquery.once.js`

## Usage

[See the API documentation for more information on how to use jQuery Once.](https://github.com/RobLoach/jquery-once/blob/master/API.md#readme)

``` javascript
// The following will change the color of each paragraph to red, just once
// for the "changecolor" key.
$('p').once('changecolor').css('color', 'red');

// .once() will return a set of elements that yet to have the once ID
// associated with them. You can return to the original collection set by
// using .end().
$('p')
  .once("changecolorblue")
    .css("color", "blue")
  .end()
  .css("color", "red");

// To execute a function on the once set, you can use jQuery's each().
$('div.calendar').once().each(function() {
  // Since there is no once ID provided here, the key will be "once".
});
```

## Development

1. Ensure you are using [node](http://nodejs.org) >= 4.1.1:
  ```
  node --version
  ```

2. Install dependencies through [npm](http://npmjs.org):
  ```
  npm install
  ```

3. Check coding style standard, and automated testing:
  ```
  npm test
  ```

4. Build `jquery.once.min.js` with:
  ```
  npm run build
  ```

5. Update API documentation:
  ```
  npm run docs
  ```

6. Tag and publish the new versions to [npm](http://npmjs.com) with [Semantic
Versioning](http://semver.org/):
  ```
  git tag 2.1.0
  git push origin 2.1.0
  npm publish
  ```

## Change Log

[Discover the change history by heading on over to the `CHANGELOG.md` file.](CHANGELOG.md)

## License

Dual licensed under:

- [GPL-2.0](http://opensource.org/licenses/gpl-2.0.php)
- the incredibly [permissive](http://en.wikipedia.org/wiki/Permissive_free_software_licence) [MIT license](http://opensource.org/licenses/MIT)

Copyright &copy; [Rob Loach](http://github.com/RobLoach)
