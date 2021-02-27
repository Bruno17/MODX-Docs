---
title: "OnBeforeWebLogout"
_old_id: "399"
_old_uri: "2.x/developing-in-modx/basic-development/plugins/system-events/onbeforeweblogout"
---

## Event: OnBeforeWebLogout

Fires right before a user logs out of a non-mgr context. The logout hasn't occured yet.

- Service: 3 - Web Access Events
- Group: None

## Event Parameters

| Name               | Description                                                                          |
| ------------------ | ------------------------------------------------------------------------------------ |
| **&** user         | A reference to the modUser object of the user. **Passed by reference**               |
| userid             | The user ID of the user. (deprecated)                                                |
| username           | The username of the user. (deprecated)                                               |
| **&** loginContext | The context key this logout is occurring in. **Passed by reference**                 |
| **&** addContexts  | Additional contexts in which the logout is also occuring in. **Passed by reference** |

## Example

Такой плагин запишет в "Журнал ошибок" id вышедшего пользователя и откуда он вышел:

```php
<?php
$eventName = $modx->event->name;
switch($eventName) {
    case 'OnBeforeWebLogout':
        $u = $user->get('id');
        $modx->log(modX::LOG_LEVEL_ERROR, 'User with id '.$u.' logged out in context '.$loginContext.' and also in these'.print_r($addContexts));
        break;
}
```    

## See Also

- [OnBeforeManagerLogout event](extending-modx/plugins/system-events/onbeforemanagerlogout "OnBeforeManagerLogout")
- [OnWebLogout event](extending-modx/plugins/system-events/onweblogout "OnWebLogout")
- [OnManagerLogout event](extending-modx/plugins/system-events/onmanagerlogout "OnManagerLogout")
- [System Events](extending-modx/plugins/system-events "System Events")
- [Plugins](extending-modx/plugins "Plugins")
