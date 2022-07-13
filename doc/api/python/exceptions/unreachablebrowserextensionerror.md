# UnreachableBrowserExtensionError

- extends: [WebError](./weberror.md)

**UnreachableBrowserExtensionError is raised when the specified browser's extension is not in ready state. Please check if the extension is installed and enabled.**

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