# NotSupportedOperationOptionError

- extends: [NotSupportedOperationError](./doc/api/python/exceptions/notsupportedoperationerror.md)

**NotSupportedOperationOptionError is raised when an invoked method is supported for the target, but the specified option value is not supported. ex: can not clear text for desktop uielement with clear method option set to `ControlClearValue`.**

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

Type of automation recorder technology. The supported technologies are "uia", "ia", "java", "ie", "chrome", "firefox", "edge" and "sap".

### control_type
- type: str

Control type of target element. ex: "Button", "Edit", "Document", "CheckBox", "Image", and the "Image" is specified for image uielment.

### operation
- type: str

Operation method of the target element. ex: "click", "check", "highlight".

### option
- type: str

Option of the operation. ex: `ControlClearValue` is the option for "clear_text" operation's "clear_method".