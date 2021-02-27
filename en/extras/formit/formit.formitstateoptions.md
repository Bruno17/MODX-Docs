---
title: "FormItStateOptions"
_old_id: "854"
_old_uri: "revo/formit/formit.formitstateoptions"
---

## What is FormItStateOptions?

FormItStateOptions is an assistance snippet for [FormIt](extras/formit "FormIt") 1.7.0+ that will output an option list of U.S. states. It is useful for forms that need a dropdown list of U.S. states.

## Usage

Simply add the Snippet to your form, in a `<select>` call:

``` php
<select name="state">
[[!FormItStateOptions? &selected=`[[!+fi.state]]`]]
</select>
```

Note how we are passing the value of the "fi.state" placeholder (which stores the value of the state field) into the selected parameter. This tells FormItStateOptions to select the last-selected option in the form.

### FormItStateOptions Properties

FormItStateOptions comes with some default properties you can override. They are:

| Name              | Description                                                                              | Default             |
| ----------------- | ---------------------------------------------------------------------------------------- | ------------------- |
| selected          | The country value to select.                                                             |                     |
| selectedAttribute | Optional. The HTML attribute to add to a selected country.                               | selected="selected" |
| tpl               | Optional. The chunk to use for each country dropdown option.                             |                     |
| useAbbr           | If 1, will use the state abbreviation for the value. If 0, will use the full state name. | 1                   |
| toPlaceholder     | Optional. Use this to set the output to a placeholder instead of outputting directly.    |                     |

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
