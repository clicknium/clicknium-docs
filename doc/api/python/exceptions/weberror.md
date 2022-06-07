# WebError

- Extends: [BaseError](./doc/api/python/exceptions/baseerror.md)

**WebError is raised for common web automation exceptions.**

## Constructor<!-- {docsify-ignore} -->
- [message](#message)
- [stacktrace](#stacktrace)
- [browser_type](#browser_type)


### Message
- type: str

Message of the exception.


### Stacktrace
- type: str

Stack of the exception which got raised inside the exception.

### Browser_type
- type: str

Type of the browser. The supporting browsers are "IE", "Chrome", "Firefox" and "Edge".