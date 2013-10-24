Module
======

This file describes some common rules regarding an official FireGento module.


### Module Naming

* FireGento is spelled with an uppercase "G" ;-)
* A FireGento module name should sort of describe what the extension does.
  * E.g.: "MageSetup" => Configures Magento
  * E.g.: "Logger" => Provides more options for logging
  * E.g.: "Pdf" => Provides a better pdf layout


### Developers

* Every developer should be listed with their name and link to the Github account in the README.md of the module.
* For every module there should be at least 1 developer but max. 2 developers defined as "LEAD". A lead developer in this case means that they are "responsible" for the extension, reviewing issues and pull requests, ..


### Folder structure

A FireGento module has to contain 2 main folders in the repository:

* docs
* src

The `src` folder contains the FireGento module. The `docs` folder should contain all documentation files, e.g. the description of all features, the generated API docs via phpDox, ..

Other folders are allowed if applicable or useful (e.g. for Selenium tests).


### Versioning

A FireGento module has to use the "Semantic Versioning" scheme.
You can read more about this scheme on its website [semver.org](http://semver.org/)


### Code Pool

A FireGento module is located in the *community* code pool of Magento.


### README

A FireGento module must contain a proper README file which provides information what the extension does, how to install and uninstall the extension, ..

You can use the [README.md](https://github.com/firegento/codingstandard/blob/master/README.md) of the FireGento_SampleModule as a template.


### LICENSE

All FireGento modules are explicitly licensed under the General Public License, version 3 (GPLv3).

Therefore, a FireGento module must contain a `LICENSE.md` file of the General Public License, version 3 (GPLv3) in the module root directory and must have the license notice in every module file.
You can copy the license file from [here](https://github.com/firegento/codingstandard/blob/master/LICENSE.md) and check the sample module for how to implement the license docs in the module file.


### modman

Every FireGento module must contain a valid `modman` file in the module root directory.


### Composer

Every FireGento module must contain a valid `composer.json` file in the module root directory.

Example:

```json
{
  "name": "firegento/samplemodule",
  "license": ["GPL-3.0"],
  "type": "magento-module",
  "description": "This is a short description of what the module does.",
  "homepage": "https://github.com/firegento/firegento-samplemodule",
  "require": {
    "magento-hackathon/magento-composer-installer": "*"
  },
  "repositories": [
    {
      "type": "composer",
      "url": "http://packages.firegento.com"
    }
  ]
}
```

After the module is published, please make sure that it is added to the `satis.json` for the composer registry of [packages.firegento.com](http://packages.firegento.com/).
You can find the composer registry [here](https://github.com/magento-hackathon/composer-repository).


### phpDox

We use [phpDox](http://phpdox.de/) for the generation of the API docs of our Magento modules.

You can find an example phpDox configuration file in the sample module [here](https://github.com/firegento/codingstandard/blob/master/sample-module/phpdox.xml.dist). This file should be copied to the repository root of the new FireGento module. The module name in this file has to be changed afterwards.
