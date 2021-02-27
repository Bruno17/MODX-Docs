---
title: "getMany"
_old_id: "1175"
_old_uri: "2.x/class-reference/xpdoobject/related-object-accessors/getmany"
---

## xPDOObject::getMany()

Gets a collection of objects related by aggregate or composite relations.

## Syntax

API Docs: [xPDOObject::getMany()](http://api.modx.com/revolution/2.2/db_core_xpdo_om_xpdoobject.class.html#%5CxPDOObject::getMany())

``` php
array &getMany (
   string $alias,
   [object $criteria = null],
   [boolean|integer $cacheFlag = true]
)
```

## Example

Get all the Chunks in a Category and output their names.

``` php
$category = $xpdo->getObject('Category',1);
$chunks = $category->getMany('Chunk');
foreach ($chunks as $chunk) {
   echo $chunk->get('name').'<br />';
}
```

## See Also

- [getOne](extending-modx/xpdo/class-reference/xpdoobject/related-object-accessors/getone "getOne")
- [Working with Related Objects](extending-modx/xpdo/retrieving-objects/related-objects "Working with Related Objects")
