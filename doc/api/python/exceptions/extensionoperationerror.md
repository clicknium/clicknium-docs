# ExtensionOperationError

- extends: [BaseError](./doc/api/python/exceptions/baseerror.md)

**ExtensionOperationError is raised when the specified extension fails in operation "install", "update" or "uninstall".**

## Constructor<!-- {docsify-ignore} -->
- [message](#message)
- [stacktrace](#stacktrace)
- [extention_type](#extention_type)
- [operation](#operation)

### message
- type: str

Message of the exception.


### stacktrace
- type: str

A string representing all the calls prior to the function that raised the exception.


### extention_type
- type: str

Type of the extension.

### operation
- type: str

Operation of the extension.