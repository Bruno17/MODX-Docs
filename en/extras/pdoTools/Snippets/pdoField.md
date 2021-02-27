---
title: "pdoField"
---

This snippet has the functionality of both [getResourceField](extras/getresourcefield) and [UltimateParent][2], that is, it displays any field from the specified resource or of its parent, including TV values.

Unlike its analogue it works with documents in any context and has the ability to specify additional parameters in the snippet call, allowing output of resources normally not displayed, for example, hidden resources. By specifying the parameter **&class** it can get the field of any MODX object. It may be called as an [Output Modifier] [3].

## Properties

It takes [the general properties and sampling results](extras/pdoTools/General_settings) of pdoTools and some of its own:

| Property           | Default          | Description                                                                                                                      |
| ------------------ | ---------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| **&id**            | Current resource | Resource ID.                                                                                                                     |
| **&field**         | pagetitle        | Resource field.                                                                                                                  |
| **&top**           |                  | Selects the root-level parent of the specified resource.                                                                         |
| **&topLevel**      |                  | Selects the resource's parent at this level from the root level.                                                                 |
| **&default**       |                  | Specifies the resource field to return if **&field** is empty. Faster than the Output Modifier filter *:default =*               |
| **&output**        |                  | It specifies the string that is returned if **&default** and **&field** are all empty .                                          |
| **&toPlaceholder** |                  | If not empty, the snippet will save the field value to a placeholder with the same name, instead of displaying it to the screen. |

*If you specify **&top** or **&topLevel**, but not a **&context**, an additional request to the database will be made to determine the context.*

Does not support working with chunk or snippet objects, as it returns only one field.

## Examples

The snippet can be used as an Output Modifier:

```php
[[*id:pdofield=`longtitle`]]
```

You can specify properties in a JSON array. For example, selecting the second parent of the resource and returning its «longtitle»:

```php
[[*id:pdofield=`{"top":2,"field":"longtitle"}`]]
```

But it is better to use a normal snippet call - it is faster and more convenient:

```php
[[pdoField?
    &id=`[[*id]]`
    &field=`longtitle`
    &top=`2`
]]
```

[2]: https://modx.com/extras/package/ultimateparent
[3]: https://rtfm.modx.com/revolution/2.x/making-sites-with-modx/customizing-content/input-and-output-filters-%28output-modifiers%29
