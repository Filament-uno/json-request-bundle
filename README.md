SymfonyBundles JsonRequest Bundle
=================================

This is a copy of the Original SymfonyBundles JsonRequest bundle, with commit fa0e3d252c244aea89ef44866c404b29cfd6dc4c as base.
I will try to keep this up to date, but I won't be actively adding new features to this bundle.


[![Build Status][testing-image]][testing-link]
[![Scrutinizer Code Quality][scrutinizer-code-quality-image]][scrutinizer-code-quality-link]
[![Code Coverage][code-coverage-image]][code-coverage-link]
[![Total Downloads][downloads-image]][package-link]
[![Latest Stable Version][stable-image]][package-link]
[![License][license-image]][license-link]

What is JsonRequest Bundle?
---------------------------
This bundle will help you to work with json requests as standard requests without using «crutches».
If previously for fetching of data from the request you did like this:
`$data = json_decode($request->getContent())`,
it is now in this already there is no need to.

For example when sending json-request from AngularJS, Vue.js or etc.
Early:
``` php
public function indexAction(Request $request)
{
    $data = json_decode($request->getContent(), true);

    // uses request data
    $name = isset($data['name']) ? $data['name'] : null;
}
```

Now you can work with json-request as with standard request:
``` php
public function indexAction(Request $request)
{
    $name = $request->get('name');
}
```

Installation
------------
* Require the bundle with composer:

``` bash
composer require filament-uno/json-request-bundle
```

[package-link]: https://packagist.org/packages/filament-uno/json-request-bundle
[license-link]: https://github.com/filament-uno/json-request-bundle/blob/master/LICENSE
[license-image]: https://poser.pugx.org/Filament-uno/json-request-bundle/license

[testing-link]: https://travis-ci.org/symfony-bundles/json-request-bundle
[testing-image]: https://travis-ci.org/symfony-bundles/json-request-bundle.svg?branch=master
[stable-image]: https://poser.pugx.org/Filament-uno/json-request-bundle/v/stable

[downloads-image]: https://poser.pugx.org/Filament-uno/json-request-bundle/downloads

[code-coverage-link]: https://scrutinizer-ci.com/g/Filament-uno/json-request-bundle/?branch=main
[code-coverage-image]: https://scrutinizer-ci.com/g/Filament-uno/json-request-bundle/badges/coverage.png?b=main
[scrutinizer-code-quality-link]: https://scrutinizer-ci.com/g/Filament-uno/json-request-bundle/?branch=main
[scrutinizer-code-quality-image]: https://scrutinizer-ci.com/g/Filament-uno/json-request-bundle/badges/quality-score.png?b=main
