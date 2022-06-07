# ExtensionOperationError

- Extends: [BaseError](./doc/api/python/exceptions/baseerror.md)

**ExtensionOperationError is raised when the specified extension with oparetion "install", "update", or "uninstall" failed.**

## Constructor<!-- {docsify-ignore} -->
- [ Message](#message)
- [Stacktrace](#stacktrace)
- [Extention_type](#extention_type)
- [Operation](#operation)

### Message
- type: str

Message of the exception.


### Stacktrace
- type: str

Stack of the exception which got raised inside the exception.


### Extention_type
- type: str

Type of the extension.

### Operation
- type: str

Operation of the extension.