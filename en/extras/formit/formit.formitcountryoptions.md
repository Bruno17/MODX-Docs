---
title: "FormItCountryOptions"
_old_id: "852"
_old_uri: "revo/formit/formit.formitcountryoptions"
---

## What is FormItCountryOptions?

FormItCountryOptions is an assistance snippet for [FormIt](extras/formit "FormIt") 1.7.0+ that will output an option list of countries in the world. It is useful for forms that need a dropdown list of countries.

## Usage

Simply add the Snippet to your form, inside a `<select>` element:

``` html
<select name="country">
    [[!FormItCountryOptions? &selected=`[[!+fi.country]]`]]
</select>
```

Note how we are passing the value of the "fi.country" placeholder (which stores the value of the country field) into the selected parameter. This tells FormItCountryOptions to select the last-selected option in the form.

### FormItCountryOptions Properties

FormItCountryOptions comes with some default properties you can override. They are:

| Name                 | Description                                                                                                                                                                                                     | Default             |
| -------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------- |
| selected             | The country value to select.                                                                                                                                                                                    |                     |
| selectedAttribute    | Optional. The HTML attribute to add to a selected country.                                                                                                                                                      | selected="selected" |
| tpl                  | Optional. The chunk to use for each country dropdown option.                                                                                                                                                    |                     |
| useIsoCode           | If 1, will use the ISO country code for the value. If 0, will use the country name.                                                                                                                             | 1                   |
| prioritized          | Optional. A comma-separated list of ISO codes for countries that will move them into a prioritized "Frequent Visitors" group at the top of the dropdown. This can be used for your commonly-selected countries. |                     |
| prioritizedGroupText | Optional. If set and &prioritized is in use, will be the text label for the prioritized option group.                                                                                                           |
| allGroupText         | Optional. If set and &prioritized is in use, will be the text label for the all other countries option group.                                                                                                   |
| optGroupTpl          | Optional. If set and &prioritized is in use, will be the chunk tpl to use for the option group markup.                                                                                                          | optgroup            |
| toPlaceholder        | Optional. Use this to set the output to a placeholder instead of outputting directly.                                                                                                                           |                     |

### Prioritizing Countries

Sometimes you want to have certain countries appear at the top of the list, in an option group. FormItCountryOptions supports this, with the `&prioritized` option. For example:

``` php
[[!FormItCountryOptions?
    &selected=`[[+fi.country]]`
    &prioritized=`US,GB,DE,RU,JP,FR,NL,CA,AU,UA`
]]
```

Will output a list that looks like this:

![](20110707-ckb8i6wtgk9gwrtds59nra4smh.jpeg)

You simply pass the ISO codes of the countries you wish to prioritize in the &prioritized parameter. You can also adjust the text of the option groups with the `&prioritizedGroupText` and `&allGroupText` properties.

## See Also


1. [FormIt.Hooks](extras/formit/formit.hooks)
    1. [FormIt.Hooks.email](extras/formit/formit.hooks/email)
    2. [FormIt.Hooks.FormItAutoResponder](extras/formit/formit.hooks/formitautoresponder)
    3. [FormIt.Hooks.math](extras/formit/formit.hooks/math)
    4. [FormIt.Hooks.recaptcha](extras/formit/formit.hooks/recaptcha)
    5. [FormIt.Hooks.redirect](extras/formit/formit.hooks/redirect)
    6. [FormIt.Hooks.spam](extras/formit/formit.hooks/spam)
    7. [FormIt.Hooks.FormItSaveForm](extras/formit/formit.hooks/formitsaveform)
2. [FormIt.Validators](extras/formit/formit.validators)
3. [FormIt.FormItRetriever](extras/formit/formit.formitretriever)
4. [FormIt.Tutorials and Examples](extras/formit/formit.tutorials-and-examples)
    1. [FormIt.Examples.Custom Hook](extras/formit/formit.tutorials-and-examples/examples.custom-hook)
    2. [FormIt.Examples.Simple Contact Page](extras/formit/formit.tutorials-and-examples/examples.simple-contact-page)
    3. [FormIt.Handling Selects, Checkboxes and Radios](extras/formit/formit.tutorials-and-examples/handling-selects,-checkboxes-and-radios)
    4. [FormIt.Using a Blank NoSpam Field](extras/formit/formit.tutorials-and-examples/using-a-blank-nospam-field)
5. [FormIt.FormItCountryOptions](extras/formit/formit.formitcountryoptions)
6. [FormIt.FormItStateOptions](extras/formit/formit.formitstateoptions)
