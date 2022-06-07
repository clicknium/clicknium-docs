# NotSupportedOperationOptionError

- Extends: [NotSupportedOperationError](./doc/api/python/exceptions/notsupportedoperationerror.md)

**NotSupportedOperationOptionError is raised when an invoked method is supported for the target, but the specified option value is not supported. Eg: can not clear text for desktop uielement with clear method option set to `ControlClearValue`.**

## Constructor<!-- {docsify-ignore} -->
- [Message](#message)
- [Stacktrace](#stacktrace)
- [Automation_tech](#automationtech)
- [Control_type](#controltype)
- [Operation](#operation)
- [Option](#option)


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

Operation method of the target element. Eg: "Click", "Check", "Highlight".

### Option
- type: str

Option of the operation. Eg: `ControlClearValue` is the option for "clear_text" operation's "clear_method".