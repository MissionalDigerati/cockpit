# Why a New Fork

We are using this product for internal use, and need to add several features.  Since the original developer is going to move development to Cockpit Next, we want to maintain our own version of the code.  You are welcome to fork this repo, but you may want to checkout Cockpit Next at [aheinze's repo](https://github.com/aheinze/cockpit).

Development
-----------

This repository is following the branching technique described in [this blog post](http://nvie.com/posts/a-successful-git-branching-model/).

Questions or problems? Please post them on the [issue tracker](https://github.com/MissionalDigerati/cockpit/issues). You can contribute changes by forking the project and submitting a pull request.

# Cockpit

[![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/aheinze/cockpit?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

[![Latest Stable Version](https://poser.pugx.org/aheinze/cockpit/v/stable.svg)](https://packagist.org/packages/aheinze/cockpit) [![Latest Unstable Version](https://poser.pugx.org/aheinze/cockpit/v/unstable.svg)](https://packagist.org/packages/aheinze/cockpit) [![License](https://poser.pugx.org/aheinze/cockpit/license.svg)](https://packagist.org/packages/aheinze/cockpit)

The CMS for developers. Add content management functionality to any site - plug &amp; play CMS.
Manage content like collections, regions, forms and galleries which you can reuse anywhere on your website.


![Cockpit](http://getcockpit.com/site/assets/images/teaser.png)


* Homepage: [http://getcockpit.com](http://getcockpit.com)
* Twitter: [@getcockpit](http://twitter.com/getcockpit)


### Requirements

* PHP >= 5.4
* PDO + SQLite (or MongoDB)
* GD extension

make also sure that <code>$_SERVER['DOCUMENT_ROOT']</code> exists and is set correctly.


### Installation

1. Download Cockpit and put the cockpit folder in the root of your web project or via composer <code>composer create-project aheinze/cockpit cockpit --stability="dev"</code>
2. Make sure that the __/cockpit/storage__ folder and all its subfolders are writable
3. Go to __/cockpit/install__ via Browser
4. You're ready to use Cockpit :-)

### Usage

**Embed Cockpit**

Embedding Cockpit is really easy. Just include the following snippet anywhere you want to use Cockpit:

```php
// make cockpit api available
require('path/to/cockpit/bootstrap.php');
```

**Regions**

Render regions api:

```html
<div><?php region("address") ?></div>
<div><?=get_region("address") ?></div>
```

**Collections**

Loop over collection data:

```html
<?php foreach(collection("posts")->find(["active"=>1]) as $post): ?>
    <div class="post">
        <h3><?=$post["title"];?></h3>
        <p>
            <?=$post["content"];?>
        </p>
    </div>
<?php endforeach; ?>
```

### Documentation

Please visit http://getcockpit.com/docs - any contributions are welcome: https://github.com/aheinze/cockpit-docs


### Language files

Please visit and contribute to https://github.com/aheinze/cockpit-i18n

### Support

Google group: [CockpitCMS](https://groups.google.com/d/forum/cockpitcms)


### Credits

- [BrowserStack](https://www.browserstack.com) - Enable cross-browser testing (thanks for sponsoring!).


### Copyright and license

Copyright 2013 [Agentejo](http://www.agentejo.com) under the MIT license.

The MIT License (MIT)

Copyright (c) 2013 Agentejo, http://agentejo.com

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
