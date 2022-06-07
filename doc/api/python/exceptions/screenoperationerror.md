# ScreenOperationError

- Extends: [WindowsNativeError](./doc/api/python/exceptions/windowsnativeerror.md)

**ScreenOperationError is raised when screen operations with desktop uielement has any exceptions.**

## Constructor<!-- {docsify-ignore} -->
- [Message](#message)
- [Stacktrace](#stacktrace)
- [Name](#name)
- [Native_errorcode](#native_errorcode)

### Message
- type: str

Message of the exception.


### Stacktrace
- type: str

Stack of the exception which got raised inside the exception.

### Name
- type: str

Win32 native API name.


### Native_errorcode
- type: str

Win32 native error code.
