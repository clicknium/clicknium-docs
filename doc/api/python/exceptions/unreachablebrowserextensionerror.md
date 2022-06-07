# UnreachableBrowserExtensionError

- Extends: [WebError](./doc/api/python/exceptions/weberror.md)

**UnreachableBrowserExtensionError is raised when the specified browser's extension not in ready state. May be the extension is not installed, not enabled or failed to run.**

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

Type of the browser. The supporting browsers are "IE", "Chrome", "Firefox" and "Edge".