# InvalidSelectedItemError

- extends: [InvalidOperationError](./doc/api/python/exceptions/invalidoperationerror.md)

**InvalidSelectedItemError is raised when a method call is valid for the object, but the set value is invalid for the object's current value. Eg: can not select an invalid item for selecting item method.**

## Constructor<!-- {docsify-ignore} -->
- [message](#message)
- [stacktrace](#stacktrace)
- [item](#item)

### message
- type: str

Message of the exception.


### stacktrace
- type: str

A string representing all the calls prior to the function that raised the exception.

### item
- type: str

Value set for the method.