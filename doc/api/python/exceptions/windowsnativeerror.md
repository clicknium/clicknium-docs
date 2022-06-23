# WindowsNativeError

- extends: [WindowError](./doc/api/python/exceptions/windowerror.md)

**WindowsNativeError is raised when a method call with win32 native has any exception.**

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