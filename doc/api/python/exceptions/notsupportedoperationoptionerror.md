# NotSupportedOperationOptionError

- extends: [NotSupportedOperationError](./doc/api/python/exceptions/notsupportedoperationerror.md)

**NotSupportedOperationOptionError is raised when an invoked method is supported for the target, but the specified option value is not supported. Eg: can not clear text for desktop UI element with clear method option set to `ControlClearValue`.**

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

Stack of the exception which got raised inside the exception.

### automation_tech
- type: str

Type of automation recorder technology. The supporting recorder technologies are as follows "Uia", "Ia", "Java", "IE", "Chrome", "Firefox", "Edge" and "Sap".

### control_type
- type: str

Control type of target element. Eg: "button", "edit", "document", "checkBox", "image", and the "image" is specified for image UiElement.

### operation
- type: str

Operation methods of the target element. Eg: "click", "check", "highlight".

### option
- type: str

Option for the operation. Eg: `ControlClearValue` is the option for "clear_text" operation's "clear_method".