# NotSupportedOperationError

- extends: [NotSupportedError](./doc/api/python/exceptions/notsupportederror.md)

**NotSupportedOperationError is raised when an invoked method, its automation technology or operation is not supported for the target. ex: can not set text for an image uielement.**

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

Type of automation recorder technology. The supported technologies are "UIA", "IA", "Java", "IE", "Chrome", "Firefox", "Edge" and "SAP".

### control_type
- type: str

Control type of target element. ex: "Button", "Edit", "Document", "CheckBox", "Image", and the "Image" is specified for image uielment.

### operation
- type: str

Opration method of the target element. ex: "click", "check", "highlight".