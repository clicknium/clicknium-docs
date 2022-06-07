# InvalidSelectedItemError

- Extends: [InvalidOperationError](./doc/api/python/exceptions/invalidoperationerror.md)

**InvalidSelectedItemError is raised when a method call is valid for the object, but the set value is invalid for the object's current value. Eg: can not select an invalid item with selecting item method.**

## Constructor<!-- {docsify-ignore} -->
- [Message](#message)
- [Stacktrace](#stacktrace)
- [Item](#item)

### Message
- type: str

Message of the exception.


### Stacktrace
- type: str

Stack of the exception which got raised inside the exception.

### Item
- type: str

Value set for the method.