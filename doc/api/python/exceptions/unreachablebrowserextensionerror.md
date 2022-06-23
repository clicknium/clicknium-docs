# UnreachableBrowserExtensionError

- extends: [WebError](./doc/api/python/exceptions/weberror.md)

**UnreachableBrowserExtensionError is raised when the specified browser's extension not in ready state. Maybe the extension is not installed, not enabled or failed to run.**

## Constructor<!-- {docsify-ignore} -->
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

Type of the browses. The supporting browsers are as follows, "IE", "Chrome", "Firefox" and "Edge".