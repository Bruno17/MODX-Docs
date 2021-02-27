---
title: "OnManagerLogin"
_old_id: "432"
_old_uri: "2.x/developing-in-modx/basic-development/plugins/system-events/onmanagerlogin"
---

## Event: OnManagerLogin

Fires anytime a user successfully logs into the manager after performing any autentification checks successfully. Doesn't affect the autentification process.

- Service: 2 - Manager Access Events
- Group: None

## Event Parameters

| Name       | Description                                                                      |
| ---------- | -------------------------------------------------------------------------------- |
| user       | A reference to the modUser object.                                               |
| attributes | An array of: - rememberme - Boolean set if user wants password to be remembered. |
|            | - lifetime - The session cookie lifetime for this login.                         |
|            | - loginContext - The context key this login is occurring in.                     |
|            | - addContexts - Additional contexts in which the login is also occuring in.      |

## Event Login Workflow

1. _[_OnBeforeWebLogin_](extending-modx/plugins/system-events/onbeforeweblogin)_ || _[OnBeforeManagerLogin](extending-modx/plugins/system-events/onbeforemanagerlogin)_ - Inside this event the developer can check for erroneous parameters which will **disallow** further logging in process. If plugins executed by this event return something except true, the logging in will be aborted with the specified error.
2. _[OnUserNotFound](extending-modx/plugins/system-events/onusernotfound)_ - This event is executed only if the provided username is not found inside MODX database. The developer can provide it's own modUser object in the event output to continue the login process.
3. _[OnWebAuthentication](extending-modx/plugins/system-events/onwebauthentication)_ || _[OnManagerAuthentication](extending-modx/plugins/system-events/onmanagerauthentication)_ - Inside this event the developer can check for parameters which will **override the default checking by password** and **allow** further logging in process. If one of the plugins executed from this event return true, the user is considered verified and logged in.
4. _[OnWebLogin](extending-modx/plugins/system-events/onweblogin)_ || **_OnManagerLogin_** - This event is fired after the logging in process has finished and the user is considered logged in. It **doesn't change** the logging in process **behaviour**.

## Example

Such a plugin will write to the "Error log" who logged in and where:

```php
<?php
$eventName = $modx->event->name;
switch($eventName) {
    case 'OnManagerLogin':
        $id = $user->get('id');
        $modx->log(modX::LOG_LEVEL_ERROR, 'User logged in with id '.$id.print_r($attributes));
        break;
}
```

## See Also

- [System Events](extending-modx/plugins/system-events "System Events")
- [Plugins](extending-modx/plugins "Plugins")
