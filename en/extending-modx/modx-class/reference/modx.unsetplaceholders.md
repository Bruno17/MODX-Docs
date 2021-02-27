---
title: "modX.unsetPlaceholders"
_old_id: "1113"
_old_uri: "2.x/developing-in-modx/other-development-resources/class-reference/modx/modx.unsetplaceholders"
---

## modX::unsetPlaceholders

Unset multiple placeholders, either by prefix or an array of keys.

## Syntax

API Doc: [modX::unsetPlaceholders()](http://api.modx.com/revolution/2.2/db_core_model_modx_modx.class.html#%5CmodX::unsetPlaceholders())

``` php
void unsetPlaceholders (string|array $keys)
```

## Example

Unset the 'my.name' and 'my.email' Placeholders.

``` php
$modx->unsetPlaceholders(array('my.name','my.email'));
```

Unset all Placeholders that are prefixed with 'my.'

``` php
$modx->unsetPlaceholders('my.');
```

## See Also

- [modX.unsetPlaceholder](extending-modx/modx-class/reference/modx.unsetplaceholder "modX.unsetPlaceholder")
- [modX.setPlaceholder](extending-modx/modx-class/reference/modx.setplaceholder "modX.setPlaceholder")
- [modX.setPlaceholders](extending-modx/modx-class/reference/modx.setplaceholders "modX.setPlaceholders")
- [modX.toPlaceholder](extending-modx/modx-class/reference/modx.toplaceholder "modX.toPlaceholder")
- [modX.toPlaceholders](extending-modx/modx-class/reference/modx.toplaceholders "modX.toPlaceholders")
