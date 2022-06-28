# NotSupportedError

- extends: [BaseError](./doc/api/python/exceptions/baseerror.md)

**NotSupportedError is raised when an invoked method is not supported, or when an attempt to read, seek, or write to a stream that does not support the invoked functionality.**

- [message](#message)
- [stacktrace](#stacktrace)


### message
- type: str

Message of the exception.


### stacktrace
- type: str

A string representing all the calls prior to the function that raised the exception.