# Magento QA Tools

## Status

[![Dependencies Status](https://depending.in/frozenminds/php-qatools-magento.png)](http://depending.in/frozenminds/php-qatools-magento)

* _Currently, the [EcomDev PHPUnit](https://github.com/EcomDev/EcomDev_PHPUnit) package is not compatible with [PHPUnit](https://github.com/sebastianbergmann/phpunit) 4.0 (see [#188](https://github.com/EcomDev/EcomDev_PHPUnit/pull/188))_

## Installation

To install the QA tools for your Magento project, just add the following to your ```composer.json``` file:

```
{
    "minimum-stability": "dev",
    "require-dev": {
        "magento-hackathon/magento-composer-installer": "*",
        "frozenminds/php-qatools-magento": "*"
    },
    "repositories": [
        {
            "type": "git",
            "url":  "git@github.com:EcomDev/EcomDev_PHPUnit.git"
        },
        {
            "type": "composer",
            "url": "http://packages.firegento.com"
        }
    ],
    "extra": {
        "magento-root-dir": "./",
        "magento-deploystrategy": "copy",
        "magento-force": 1
    }
}
```

Then simply run:

```
php composer.phar update --dev
```

### Note

Make sure you include in your main ```composer.json``` also the ```repositories``` property. Otherwise Composer will ignore them.

If you include the package in the ```require-dev``` node, then use ```composer install/update``` with the ```--dev``` option on your local/testing machines but use ```---no-dev``` in production because you don't need them there.
