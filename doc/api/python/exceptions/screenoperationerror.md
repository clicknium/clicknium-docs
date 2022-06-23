# ScreenOperationError

- extends: [WindowsNativeError](./doc/api/python/exceptions/windowsnativeerror.md)

**ScreenOperationError is raised when screen operations with desktop UiElement have any exceptions.**

## Constructor<!-- {docsify-ignore} -->
- [message](#message)
- [stacktrace](#stacktrace)
- [name](#name)
- [native_errorcode](#native_errorcode)

### message
- type: str

Message of the exception.


### stacktrace
- type: str

A string representing all the calls prior to the function that raised the exception.

### name
- type: str

Win32 native api name.


### native_errorcode
- type: str

Win32 native error code.
