# BrowserNotInstallError

- Extends: [WebError](./doc/api/python/exceptions/weberror.md)

**BrowserNotInstallError is raised when the specified browser is not installed.**

## Constructor<!-- {docsify-ignore} -->
- [Message](#message)
- [Stacktrace](#stacktrace)
- [Browser_type](#browser_type)


### Message
- type: str

Message of the exception.


### Stacktrace
- type: str

Stack of the exception which got raised inside the exception.

### Browser_type
- type: str

Type of the browser. The supporting browsers are "ie", "chrome", "firefox" and "edge".