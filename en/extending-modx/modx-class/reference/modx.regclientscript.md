---
title: "modX.regClientScript"
_old_id: "1092"
_old_uri: "2.x/developing-in-modx/other-development-resources/class-reference/modx/modx.regclientscript"
---

## modX::regClientScript

Register JavaScript to be injected before the closing BODY tag.

## Syntax

API Doc: [modX::regClientScript()](http://api.modx.com/revolution/2.2/db_core_model_modx_modx.class.html#%5CmodX::regClientScript())

``` php
void regClientScript (string $src, [boolean $plaintext = false])
```

## Example

Add some JS to the end of the page.

``` php
$modx->regClientScript('assets/js/footer.js');
```

## See Also

- [modX](extending-modx/core-model/modx "modX")
- [modX.regClientCSS](extending-modx/modx-class/reference/modx.regclientcss "modX.regClientCSS")
- [modX.regClientHTMLBlock](extending-modx/modx-class/reference/modx.regclienthtmlblock "modX.regClientHTMLBlock")
- [modX.regClientStartupHTMLBlock](extending-modx/modx-class/reference/modx.regclientstartuphtmlblock "modX.regClientStartupHTMLBlock")
- [modX.regClientStartupScript](extending-modx/modx-class/reference/modx.regclientstartupscript "modX.regClientStartupScript")
- [modX.getRegisteredClientScripts](extending-modx/modx-class/reference/modx.getregisteredclientscripts "modX.getRegisteredClientScripts")
- [modX.getRegisteredClientStartupScripts](extending-modx/modx-class/reference/modx.getregisteredclientstartupscripts "modX.getRegisteredClientStartupScripts")
