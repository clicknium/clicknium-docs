# BrowserNotInstallError

- extends: [WebError](./doc/api/python/exceptions/weberror.md)

**BrowserNotInstallError is raised when the specified browser is not installed.**

- [message](#message)
- [stacktrace](#stacktrace)
- [browser_type](#browser_type)


### message
- type: str

Message of the exception.


### stacktrace
- type: str

A string representing all the calls prior to the function that raised the exception.

### browser_type
- type: str

Type of the browsers. The supporting browsers are as follows, "IE", "Chrome", "Firefox" and "Edge".