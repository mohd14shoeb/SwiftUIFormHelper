# SwiftUIFormHelper
Helper functions for creating forms with SwiftUI

## Features

- Helper to create some offset for the keyboard when visible
- Helper to dismiss the keyboard when pressing on something different then a form field
- FormValidator to validate input

### Create offset for keyboard

Simply add the helper function `.enableKeyboardOffset()` after the Form {}.

```swift
import SwiftUI 
import SwiftUIFormHelper

Form {

}.enableKeyboardOffset()
```

### Dismiss keyboard on tap

Simply add the helper function `.hideKeyboardOnTap()` after the Form {}.

```swift
import SwiftUI 
import SwiftUIFormHelper

Form {
    TextField("Name", text: $name)
        .hideKeyboardOnTap()
}
```

### Form Validator

Validate input from fields.

```swift
import SwiftUIFormHelper

let email = "fake@mailinator.com"
FormValidator.isValid(email: email)

let phoneNumber = "+31612345678"
FormValidator.isValid(phoneNumber: phoneNumber)
```
