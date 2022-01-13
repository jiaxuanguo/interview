## [Specific Form Types](https://web.dev/learn/forms/identity/)

### Identity
- only require sign-up if absolutely necessary
- keep the sign-up form minimal, allow the user to fill in details after sign-up
- take advantage of browser autofill
- [allow password pasting](https://www.ncsc.gov.uk/blog-post/let-them-paste-passwords)
- never store or transmit passwords in plain text. salt and hash as soon as they are obtained
- make sure sign-in and sign-up buttons are obvious and tappable
- ensure users can see the password they entered
- users should be able to change their account details
- follow the [.well-known convention](https://w3c.github.io/webappsec-change-password-url/) for password changing api

### Payment
wip

### Address
- single field for name; allow unicode characters
- single filed for street address
- [address line 2 causes confusion](https://baymard.com/blog/address-line-2), make it optional and hidden by default
- two values for country `autocomplete`: `country` and `country-name`
- 
