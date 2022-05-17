# UnreachableBrowserExtensionError

- extends: [WebError](./doc/api/python/exceptions/weberror.md)

**UnreachableBrowserExtensionError is raised when the specified browser's extension not in ready state. May be the extension is not installed, not enabled or failed to run.**

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