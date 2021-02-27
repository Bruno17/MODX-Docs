---
title: "modX.setDebug"
_old_id: "1105"
_old_uri: "2.x/developing-in-modx/other-development-resources/class-reference/modx/modx.setdebug"
---

## modX::setDebug

Sets the debugging features of the modX instance.

## Syntax

API Doc: [modX::setDebug()](http://api.modx.com/revolution/2.2/db_core_model_modx_modx.class.html#%5CmodX::setDebug())

``` php
boolean|int setDebug ([boolean|int $debug = true], [boolean $stopOnNotice = false])
```

## Example

Turn debug mode on, and tell the process to stop if Notices occur:

``` php
$modx->setDebug(true);
```

## See Also

[modX.setDebug](extending-modx/modx-class/reference/modx.setdebug)
