# NotSupportedOperationOptionError

- extends: [NotSupportedOperationError](./doc/api/python/exceptions/notsupportedoperationerror.md)

**NotSupportedOperationOptionError is raised when the specified option value is not supported by the target UI element.**

## Constructor<!-- {docsify-ignore} -->
- [message](#message)
- [stacktrace](#stacktrace)
- [automation_tech](#automationtech)
- [control_type](#controltype)
- [operation](#operation)
- [option](#option)


### message
- type: str

Message of the exception.


### stacktrace
- type: str

A string representing all the calls prior to the function that raised the exception.

### automation_tech
- type: str

Type of automation recorder technology. The supporting recorder technologies are as follows "UIA", "IA", "Java", "IE", "Chrome", "Firefox", "Edge" and "SAP".

### control_type
- type: str

Control type of target element. Eg: "Button", "Edit", "Document", "CheckBox", "Image", and the "Image" is specified for image UiElement.

### operation
- type: str

Operation methods of the target element. Eg: "click", "check", "highlight".

### option
- type: str

Option for the operation. Eg: `set-text` is the option for "clear_text" operation's "clear_method".