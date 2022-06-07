# WebElementNotRespondingError

- Extends: [WebError](./doc/api/python/exceptions/weberror.md)

**WebElementNotRespondingError is raised when browser's visiting page is not responding.**

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