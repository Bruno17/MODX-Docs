---
title: "modX.removeAllEventListener"
_old_id: "1096"
_old_uri: "2.x/developing-in-modx/other-development-resources/class-reference/modx/modx.removealleventlistener"
---

## modX::removeAllEventListener

Remove all registered events for the current request.

## Syntax

API Doc: [modX::removeAllEventListener()](http://api.modx.com/revolution/2.2/db_core_model_modx_modx.class.html#%5CmodX::removeAllEventListener())

``` php
void removeAllEventListener ()
```

## Example

Eliminate any other events from firing:

``` php
$modx->removeAllEventListener();
```

## See Also

- [modX](extending-modx/core-model/modx "modX")
