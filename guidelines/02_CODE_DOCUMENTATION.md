Code Documentation
==================

This file describes how the code documentation should look like.

File Comments
-------------

Regarding the file comments we differentiate between:

* File comments for PHP files
* File comments for CSS/JS/PHTML (Templates)/XML files

### File comments for PHP files

The file comment has to look like this:

```php
/**
 * This file is part of a FireGento e.V. module.
 *
 * This FireGento e.V. module is free software; you can redistribute it and/or
 * modify it under the terms of the GNU General Public License version 3 as
 * published by the Free Software Foundation.
 *
 * This script is distributed in the hope that it will be useful, but WITHOUT
 * ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS
 * FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.
 *
 * PHP version 5
 *
 * @category  FireGento
 * @package   FireGento_SampleModule
 * @author    FireGento Team <team@firegento.com>
 * @copyright 2013 FireGento Team (http://www.firegento.com)
 * @license   http://opensource.org/licenses/gpl-3.0 GNU General Public License, version 3 (GPLv3)
 */
```

Notes:

* The file comment has to contain the license info.
* The file comment has to contain the minimum required PHP version (PHP version 5)
* The **@category** tag must contain the name "FireGento"
* The **@package** tag must contain the module name, e.g. "FireGento_SampleModule"
* The **@author** tag must be "FireGento Team <team@firegento.com>"
* The **@copyright** tag has to contain the current year followed by "FireGento Team (http://www.firegento.com)"
* The **@license** tag has to contain the URL and Name of the GPLv3 license.


All PHP classes must contain a class comment too. The class comment should look like this:

```php
/**
 * This comment describes what the class is for.
 *
 * @category FireGento
 * @package  FireGento_MageSetup
 * @author   FireGento Team <team@firegento.com>
 */
```

Notes:

* The class comment has to contain a description of what the PHP class does.
* The class comment has to contain at least a **@category** tag, a **@package** tag and an **@author** tag.
* The values for the tags must be the same like the file comment.
* **Important:** This does not apply to setup scripts!

### File comments for CSS/JS/PHTML (Templates)/XML files

All CSS, JS, PHTML (Templates) and XML files have to contain a file comment at the beginning of the file like this:

```
/**
 * This file is part of a FireGento e.V. module.
 *
 * This FireGento e.V. module is free software; you can redistribute it and/or
 * modify it under the terms of the GNU General Public License version 3 as
 * published by the Free Software Foundation.
 *
 * This script is distributed in the hope that it will be useful, but WITHOUT
 * ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS
 * FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.
 *
 * @category  FireGento
 * @package   FireGento_SampleModule
 * @author    FireGento Team <team@firegento.com>
 * @copyright 2013 FireGento Team (http://www.firegento.com)
 * @license   http://opensource.org/licenses/gpl-3.0 GNU General Public License, version 3 (GPLv3)
 */
```

Notes:

* The values for the shown tags must be the same like the ones in the file comment of a PHP class.
