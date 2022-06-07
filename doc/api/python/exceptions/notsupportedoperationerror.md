# NotSupportedOperationError

- Extends: [NotSupportedError](./doc/api/python/exceptions/notsupportederror.md)

**NotSupportedOperationError is raised when an invoked method, its automation technology or operation is not supported for the target. ex: can not set text for an image uielement.**

## Constructor<!-- {docsify-ignore} -->
- [Message](#message)
- [Stacktrace](#stacktrace)
- [Automation_tech](#automationtech)
- [Control_type](#controltype)
- [Operation](#operation)


### Message
- type: str

Message of the exception.


### Stacktrace
- type: str

Stack of the exception which got raised inside the exception.

### Automation_tech
- type: str

Type of automation recorder technology. The supporting technologies are as follows, "Uia", "ia", "Java", "IE", "Chrome", "Firefox", "Edge" and "SAP".

### Control_type
- type: str

Control type of target element. Eg: "Button", "Edit", "Document", "CheckBox", "Image", and the "Image" is specified for image UI elment.

### Operation
- type: str

Opration methods of the target element. Eg: "Click", "Check", "Highlight".