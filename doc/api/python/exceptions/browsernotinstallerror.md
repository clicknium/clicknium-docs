# BrowserNotInstallError

- extends: [WebError](./doc/api/python/exceptions/weberror.md)

**BrowserNotInstallError is raised when the specified browser is not installed.**

## Constructor<!-- {docsify-ignore} -->
- [message](#message)
- [stacktrace](#stacktrace)
- [browser_type](#browser_type)


### message
- type: str

Message of the exception.


### stacktrace
- type: str

Stack of the exception which got raised inside the exception.

### browser_type
- type: str

Type of the browser. The supported browsers are "ie", "chrome", "firefox" and "edge".