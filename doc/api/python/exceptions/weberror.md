# WebError

- extends: [BaseError](./doc/api/python/exceptions/baseerror.md)

**WebError is raised for common web automation exceptions.**

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

Type of the browsers. The supporting browsers are as follows, "IE", "Chrome", "Firefox" and "Edge".