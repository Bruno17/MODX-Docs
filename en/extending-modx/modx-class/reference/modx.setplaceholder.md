---
title: "modX.setPlaceholder"
_old_id: "1106"
_old_uri: "2.x/developing-in-modx/other-development-resources/class-reference/modx/modx.setplaceholder"
---

## modX::setPlaceholder

Sets a Placeholder value, corresponding to the "+" syntax.

## Syntax

API Doc: [modX::setPlaceholder()](http://api.modx.com/revolution/2.2/db_core_model_modx_modx.class.html#%5CmodX::setPlaceholder())

``` php
void setPlaceholder (string $key, mixed $value)
```

## Example

``` php
$modx->setPlaceholder('name','Barry');
```

This causes the placeholder `[[+name]]` to be available inside your templates or page content.

## See Also

- [modX.getPlaceholder](extending-modx/modx-class/reference/modx.getplaceholder "modX.getPlaceholder")
- [modX.setPlaceholders](extending-modx/modx-class/reference/modx.setplaceholders "modX.setPlaceholders")
- [modX.toPlaceholder](extending-modx/modx-class/reference/modx.toplaceholder "modX.toPlaceholder")
- [modX.toPlaceholders](extending-modx/modx-class/reference/modx.toplaceholders "modX.toPlaceholders")
