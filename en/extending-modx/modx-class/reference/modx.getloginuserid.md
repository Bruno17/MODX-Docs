---
title: "modX.getLoginUserID"
_old_id: "1066"
_old_uri: "2.x/developing-in-modx/other-development-resources/class-reference/modx/modx.getloginuserid"
---

## modX::getLoginUserID

Returns the current user ID, for the current or specified context.

## Syntax

API Doc: [modX::getLoginUserID()](http://api.modx.com/revolution/2.2/db_core_model_modx_modx.class.html#%5CmodX::getLoginUserID())

``` php
string getLoginUserID ([string $context = ''])
```

## Example

Get the current login user ID for the 'sports' context.

``` php
$id = $modx->getLoginUserID('sports');
```

## See Also

- [modX](extending-modx/core-model/modx "modX")
