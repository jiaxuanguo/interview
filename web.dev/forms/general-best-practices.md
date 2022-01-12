##[General Best Practices](https://web.dev/learn/forms/design-basics/)

### Design basics
  - visible and well-written ```label``` on every form control; **```placeholder``` is not a label** 
  - keep the labels concise
  - [label placement and font styles matter](https://www.uxmatters.com/mt/archives/2006/07/label-placement-in-forms.php)
  - choose the appropriate form control
  - different types of form controls should look different
  - avoid [multi-column forms](https://baymard.com/blog/avoid-multi-column-forms) and complex flows
  - forms should be accessible by using keyboard only
  - avoid accidental interactions by setting appropriate ```margin```, ```padding``` and ```font-size```; set ```font-size``` to at least ```16px``` to [prevent automatic zooming](https://css-tricks.com/16px-or-larger-text-prevents-ios-form-zoom/)
  - do a media query on pointer size and adjust sizing accordingly
  - show errors where they happen; navigate to the first invalid form control on submit
  - tell users how will the entered value be validated
  - if most fields in a form are required, maybe indicate those that are not

### Accessibility
 - everything from [Design basics](#design-basics)
 - use ```aria-``` attributes, more on that later ~~(or not)~~
 - prefer built-in form elements to ```div```s
 - the ```inputmode``` attribute hints type of data that might be entered by the user
 - do not rely only on color when indicating state
 - visual order of form controls should match their dom order
 - always indicate focused state 

### Internationalization and localization
 - set the ```lang``` attribute on ```html``` element
 - use ```<link rel="alternate"/>``` with the ```hreflang``` attribute set to link to an alternate version of a different language
 - define text statically in html instead of dynamically in javascript to take advantage of translation tools
 - use [css logical properties](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Logical_Properties) to accommodate different writing systems
 - use a single name field if its format is unclear
 - use generic text inputs for address if its format is unclear

### Security and privacy
 - secure means user data cannot be accessed without authorization; private means user is in full control of their data
 - submit form data over HTTPS
 - encrypt data before storing it locally
 - prefer third-party identity providers
 - be transparent about how user data will be used; allow user to access, modify, and delete personal data and collected data
 - always validate and sanitize user provided inputs on the backend
 - prevent spam submissions; use captcha or honeypots

### Autofill
 - use ```:autofill``` to select form controls filled by the browser
 - help the browser determine what to fill by adding values to the [```autocomplete```](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/autocomplete) attribute
 - use ```autocomplete="current-password"``` and ```autocomplete="new-password"``` to help the browser's password manager
 - set ```autocomplete="one-time-code"``` on SMS code input
 - set ```autocomplete="off"``` on one-off inputs
 - setup autofill for payment information
