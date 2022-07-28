# NotSupportedOperationError

- extends: [NotSupportedError](./notsupportederror.md)

**NotSupportedOperationError is raised when the method is invoked by a UI element which does not support the type of operation.**

- [message](#message)
- [stacktrace](#stacktrace)
- [automation_tech](#automationtech)
- [control_type](#controltype)
- [operation](#operation)


### message
- type: str

Message of the exception.


### stacktrace
- type: str

A string representing all the calls prior to the function that raised the exception.

### automation_tech
- type: str

Type of automation recorder technology. The supporting technologies are as follows,"UIA", "IA", "Java", "IE", "Chrome", "Firefox", "Edge" and "SAP".

### control_type
- type: str

Control type of target element. Eg: "Button", "Edit", "Document", "CheckBox", "Image", and the "Image" is specified for image UiElment.

### operation
- type: str

Opration methods of the target element. Eg: "click", "check", "highlight".