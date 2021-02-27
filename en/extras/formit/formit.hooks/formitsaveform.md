---
title: "FormItSaveForm"
_old_id: "1733"
_old_uri: "revo/formit/formit.hooks/formit.hooks.formitsaveform"
---

## The FormItSaveForm hook

This hook will save submitted forms inside an CMP.

FormIt 3.0 introduces an update to the encryption methods used for encrypting form submissions. Prior to 3.0 mcrypt was used, which in 3.0 is replaced with openssl, due to mcrypt being deprecated as of PHP 7.2. FormIt 3.0 comes with a migration page which is accessible from the manager. 

## Available Properties

It has the following properties to be passed into the FormIt snippet call:

| Name                                                                   | Description                                                                                                                 | Example                                                                |
| ---------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| formName                                                               | The name of the form. Defaults to "form-{resourceid}".                                                                      | |
| formEncrypt                                                            | If is set to '1' _(true)_ the submitted form will be encrypted before saving inside the DB.                                 | |
| formFields                                                             | A comma-separated list of fields that will be saved. Defaults will save all fields including the submit button.             | |
| fieldNames                                                             | Change the name of the field inside the CMP. So if the field name is email2 you could change the name to "secondary email". | &fieldnames=\`fieldname==Field display name,anotherone==Another field display name\` |

## See Also

1. [FormIt.Hooks.email](extras/formit/formit.hooks/email)
2. [FormIt.Hooks.FormItAutoResponder](extras/formit/formit.hooks/formitautoresponder)
3. [FormIt.Hooks.FormItSaveForm](extras/formit/formit.hooks/formitsaveform)
4. [FormIt.Hooks.math](extras/formit/formit.hooks/math)
5. [FormIt.Hooks.recaptcha](extras/formit/formit.hooks/recaptcha)
6. [FormIt.Hooks.redirect](extras/formit/formit.hooks/redirect)
7. [FormIt.Hooks.spam](extras/formit/formit.hooks/spam)
8. [FormIt.PreHooks.FormItLoadSavedForm](extras/formit/formit.hooks/prehooks.formitloadsavedform)
