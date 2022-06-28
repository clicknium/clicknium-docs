# InvalidOperationError

- extends: [BaseError](./doc/api/python/exceptions/baseerror.md)

**InvalidOperationError is raised when a method call is invalid for the object's current state.**

- [message](#message)
- [stacktrace](#stacktrace)


### message
- type: str

Message of the exception.


### stacktrace
- type: str

A string representing all the calls prior to the function that raised the exception.