# InvalidSelectedItemError

- extends: [InvalidOperationError](./invalidoperationerror.md)

**InvalidSelectedItemError is raised when the item to be selected is invalid for the object's current state.**

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