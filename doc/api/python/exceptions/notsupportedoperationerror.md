# NotSupportedOperationError

- extends: [NotSupportedError](./doc/api/python/exceptions/notsupportederror.md)

**NotSupportedOperationError is raised when the method is invoked by a UI element which does not support the type of operation. Eg: can not set text for an image UiElement.**

## Constructor<!-- {docsify-ignore} -->
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

Stack of the exception which got raised inside the exception.

### automation_tech
- type: str

Type of automation recorder technology. The supporting technologies are as follows,"UIA", "IA", "Java", "IE", "Chrome", "Firefox", "Edge" and "SAP".

### control_type
- type: str

Control type of target element. Eg: "Button", "Edit", "Document", "CheckBox", "Image", and the "Image" is specified for image UiElment.

### operation
- type: str

Opration methods of the target element. Eg: "click", "check", "highlight".