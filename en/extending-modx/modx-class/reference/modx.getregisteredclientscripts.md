---
title: "modX.getRegisteredClientScripts"
_old_id: "1071"
_old_uri: "2.x/developing-in-modx/other-development-resources/class-reference/modx/modx.getregisteredclientscripts"
---

## modX::getRegisteredClientScripts

Returns all registered JavaScript and HTML blocks.

## Syntax

API Doc: [modX::getRegisteredClientScripts()](http://api.modx.com/revolution/2.2/db_core_model_modx_modx.class.html#%5CmodX::getRegisteredClientScripts())

``` php
string getRegisteredClientScripts ()
```

## Example

Get all registered scripts into an array.

``` php
$scripts = $modx->getRegisteredClientScripts();
```

## See Also

- [modX](extending-modx/core-model/modx "modX")
