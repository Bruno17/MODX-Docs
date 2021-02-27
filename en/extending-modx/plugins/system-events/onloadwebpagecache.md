---
title: "OnLoadWebPageCache"
_old_id: "430"
_old_uri: "2.x/developing-in-modx/basic-development/plugins/system-events/onloadwebpagecache"
---

## Event: OnLoadWebPageCache

Fires after a Resource is loaded from the cache. If the Resource is not cached, this event will not fire. NOTE: this event is not particularly useful until MODX 2.3 (see [Issue 9841](http://bugs.modx.com/issues/9841)).

- Service: 4 - Cache Service Events
- Group: None

## Event Parameters

None.

## Notes

This event is triggered inside the getResource() function in modrequest.class.php.

- **\_content** : contains the _rendered_ resource (i.e. its template). Any cached placeholders will replaced with values, any uncached placeholders will appear as is.

In MODX 2.3 and later you can access the resource properties (see [Issue 9841](http://bugs.modx.com/issues/9841)):

``` php
// Override Output
$modx->event->params['resource']->_content = 'Overridden...';
```

You can access resource properties like so:

``` php
// Override Pagetitle
$modx->event->params['resource']->pagetitle = 'My New Pagetitle';
```

TVs are a trickier. They get cached as an standard array. For reading and overriding values, you will focus on element 1:

``` php
// Reading value of TV named "my_tv"
$my_tv = $modx->event->params['resource']->my_tv[1];
/*
// Where our array
array (
    0 => 'name_of_tv',
    1 => 'Value of TV Goes here',
    2 => 'default',
    3 => NULL,
    4 => 'text', // <-- TV type
)
*/
```

Such a plugin will replace pagetitle, TV and content meaning:

```php
<?php
$eventName = $modx->event->name;
switch($eventName) {
    case 'OnLoadWebPageCache':
        $modx->event->params['resource']->pagetitle = 'New title';
        // меняем значение ТВ
        $tv = $modx->event->params['resource']->price[1] = '128';
        /*
        // массив значений ТВ 
        array (
            0 => 'name', //название ТВ
            1 => 'значение', //значение ТВ
            2 => 'default', //параметры вывода ТВ
            3 => NULL,
            4 => 'text', //тип ТВ
        )
        */
        $modx->event->params['resource']->_content = 'New content'.$tv;
        break;
}
```

For further education, take a look at the cached files generated inside the `core/cache/resource/web/resources/` folder.

## See Also

- [System Events](extending-modx/plugins/system-events "System Events")
- [Plugins](extending-modx/plugins "Plugins")
