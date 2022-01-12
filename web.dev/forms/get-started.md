##[Get started with forms](https://web.dev/learn/forms/form-element/)

### Use forms to get data from users
- form control elements nested in a ```form``` element
- ```action``` attribute of form element determines url of the submit request; ```method``` attribute determines the request method
- use get method when input data should be part of url; post when action is not idempotent

### Help users enter data in forms
- describe form controls with ```label```; its ```for``` attribute should match the ```id``` of the form control element it's coupled with
- a form control's ```name``` attribute determines the field name of the data it collected
- ```type``` attribute of ```input``` determines what ui the browser renders
- ```textarea``` is a multi-lined ```<input type="text" />```
- use ```select``` to let the user select from a list of ```option```s
- preselect an ```option``` by adding a ```selected``` attribute to it
- couple ```input``` and ```datalist``` to provide suggestion to a text input
- group form controls with `fieldset`; it requires a ```legend``` as its first children
- every ```button``` inside ```form``` acts as a submit button by default; add ```type="button"``` to disable this behavior
- an ```<input type="submit" />``` can also be used as a submit button; pressing ```Enter``` when a form field has focus also works

### Help users avoid re-entering data in forms
- autofill functionality is provided by the browser, it checks ```autocomplete```, ```id```, ```name``` and other attributes on a form control to determine whether to fill it with previously filled data
- help the browser recognise fields by using sensible values in these attributes

### Help users enter the right data in forms
- form controls can handle simple data validation; error messages' language and styles are browser-determinant but can be customized
- add a ```required``` attribute to indicate a form control requires data
- add a ```type="email"``` to let the browser test whether the value entered is a valid email address; this standardized approach is usually better than testing it with javascript regular expressions
- provide a custom regular expression to test with the ```pattern``` attribute
- ```minlength```, ```maxlength```, ```min``` and ```max``` are some other validation attributes
- select form controls with pseudo-classes: 
  - ```:required``` for required form controls
  - ```:invalid``` and ```:valid``` for invalid or valid form controls respectively
  - form controls are marked with ```:invalid``` even **before user interaction**; use ```:user-invalid``` to select elements that change to an invalid state **after user interaction**
  - ```formControl.setCustomValidity(message)``` to change the error message
  - use javascript and the validation api to do custom validation

### Test your forms
- test the form on different devices with different input methods
- Form Troubleshooter extension for Chrome
- Lighthouse, bundled or headless
