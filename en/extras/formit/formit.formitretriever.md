---
title: "FormItRetriever"
_old_id: "853"
_old_uri: "revo/formit/formit.formitretriever"
---

## What is FormItRetriever?

FormItRetriever is an assistance snippet for [FormIt](extras/formit "FormIt") that will grab the data of a user's last form submission via FormIt. This is useful for "Thank You" pages where a user is sent after submitting a form.

## Usage

Simply add this Snippet to whatever page you are redirecting from using FormIt's &redirectTo property, and set &store=`1` in the FormIt call:

``` php
[[!FormItRetriever]]
```

And then display your form data with placeholders relating to the names of your form fields like such:

``` php
<p>Thanks [[!+fi.name]] for submitting. An email will be sent to you at [[!+fi.email]].</p>
```

Remember to set &store=`1` in your FormIt call, so FormIt knows to store the value.

Make sure to call the placeholders uncached. This data changes on every request, so therefore the placeholders need to change every request too.

### FormItRetriever Properties

FormItRetriever comes with some default properties you can override. They are:

| Name                 | Description                                                                                                                                                                 | Default |
| -------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------- |
| placeholderPrefix    | A string to prefix all placeholders for form fields that will be set by this Snippet.                                                                                       | fi.     |
| redirectToOnNotFound | If the data is not found and if this is set, redirect to the Resource with this ID.                                                                                         |         |
| eraseOnLoad          | If true, will erase the stored form data on load. Strongly recommended to leave to false unless you only want the data to load once.                                        |
| storeLocation        | Where to get the form data from. Should be equal to the storeLocation property of your FormIt snippet call. Possible values are 'cache' and 'session'. Defaults to 'cache'. | cache   |

## Example

Submit a form with auto-response and anti-spam protection, then redirect to a Thank You page where it loads the last form submission, and if it's not found, redirects to the resource with ID 444.

On your form page:

``` php
[[!FormIt?
    &submitVar=`go`
    &hooks=`spam,FormItAutoResponder,redirect`
    &emailTo=`my@email.com`
    &store=`1`
    &redirectTo=`123`
]]
<form action="[[~[[*id]]]]" method="post">
    <input type="hidden" name="nospam" value="" />
    <label for="name">Name: [[!+fi.error.name]]</label>
    <input type="text" name="name:required" id="name" value="[[!+fi.name]]" />
    <label for="email">Email: [[!+fi.error.email]]</label>
    <input type="text" name="email:email:required" id="email" value="[[!+fi.email]]" />
    <label for="message">Message: [[!+fi.error.message]]</label>
    <textarea name="message:stripTags" id="message" cols="55" rows="7">[[!+fi.message]]</textarea>
    <br />
    <input type="submit" name="go" value="Send Contact Inquiry" />
</form>
```

On your Thank You page (Resource ID 123):

``` php
[[!FormItRetriever? &redirectToOnNotFound=`444`]]
<p>Thanks [[!+fi.name]] for submitting. An auto-response email will be sent to you at [[!+fi.email]]. Here's a copy of your message:</p>
[[!+fi.message]]
```

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
