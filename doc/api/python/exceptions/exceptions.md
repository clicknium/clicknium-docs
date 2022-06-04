# Exceptions

Exception is raised whenever certain operations are terminated abnormally. Except for python [Built-in Exceptions](https://docs.python.org/3/library/exceptions.html#built-in-exceptions), we also define custom clicknium exceptions, which are all inherit from [BaseError](./doc/api/python/exceptions/baseerror.md).


## Clicknium Exceptions <!-- {docsify-ignore} -->

| Exception Name      | Description |
| -----------| ----------- |
| [BaseError](./doc/api/python/exceptions/baseerror.md) |All Clicknium exceptions inherit from this class|
| [ArgumentError](./doc/api/python/exceptions/argumenterror.md) |  ArgumentError is raised when one of the arguments provided to a method is not valid|
| [ArgumentNullError](./doc/api/python/exceptions/argumentnullerror.md) | ArgumentNullError is raised when a null reference is passed to a method that does not accept it as a valid argument|
| [ArgumentOutOfRangeError](./doc/api/python/exceptions/argumentoutofrangeerror.md) | ArgumentOutOfRangeError is raised when the value of an argument is outside the allowable range of values as defined by the invoked method|
| [LocatorUndefinedError](./doc/api/python/exceptions/locatorundefinederror.md) | LocatorUndefinedError is raised when the specified locator can not be found in locator store|
| [TimeoutOperationError](./doc/api/python/exceptions/timeoutoperationerror.md) | TimeoutOperationError is raised when certain operation is terminated due to timeout|
| [ElementCanNotFoundError](./doc/api/python/exceptions/elementcannotfounderror.md) | ElementCanNotFoundError is raised when the loactor can be found in locator store, but the returned ui element can not be found|
| [ExtensionOperationError](./doc/api/python/exceptions/extensionoperationerror.md) | ExtensionOperationError is raised when the specified extension with oparetion "install", "update", or "uninstall" failed|
| [NotSupportedError](./doc/api/python/exceptions/notsupportederror.md) | NotSupportedError is raised when an invoked method is not supported, or when there is an attempt to read, seek, or write to a stream that does not support the invoked functionality|
| [NotSupportedOperationError](./doc/api/python/exceptions/notsupportedoperationerror.md) | NotSupportedOperationError is raised when an invoked method, its automation technology or operation is not supported for the target. ex: can not set text for an image uielement |
| [NotSupportedOperationOptionError](./doc/api/python/exceptions/notsupportedoperationoptionerror)   | NotSupportedOperationOptionError is raised when an invoked method is supported for the target, but the specified option value is not supported. ex: can not clear text for desktop uielement with clear method option set to `ControlClearValue`|
| [InvalidOperationError](./doc/api/python/exceptions/invalidoperationerror.md)   |  InvalidOperationError is raised when a method call is invalid for the object's current state|
| [InvalidSelectedItemError](./doc/api/python/exceptions/invalidselecteditemerror.md)   | InvalidSelectedItemError is raised when a method call is valid for the object, but the set value is invalid for the object's current value. ex: can not select an invalid item for select item method|
| [WindowError](./doc/api/python/exceptions/windowerror.md)   | WindowError is raised for common window exceptions|
| [WindowsNativeError](./doc/api/python/exceptions/windowsnativeerror.md)   | WindowsNativeError is raised when a method call with win32 native has any exceptions|
| [UiaPatternNotFoundError](./doc/api/python/exceptions/uiapatternnotfounderror.md)   | UiaPatternNotFoundError is raised when a desktop uielement with uia technology can not be found|
| [ScreenOperationError](./doc/api/python/exceptions/screenoperationerror.md)   | ScreenOperationError is raised when screen operations with desktop uielement has any exceptions|
| [WebError](./doc/api/python/exceptions/weberror.md) | WebError is raised for common web automation exceptions|
| [BrowserNotRunError](./doc/api/python/exceptions/browsernotrunerror.md) | BrowserNotRunError is raised when the specified browser is not run|
| [BrowserNotInstallError](./doc/api/python/exceptions/browsernotinstallerror.md) | BrowserNotInstallError is raised when the specified browser is not installed|
| [UnreachableBrowserExtensionError](./doc/api/python/exceptions/unreachablebrowserextensionerror.md) | UnreachableBrowserExtensionError is raised when the specified browser's extension not in ready state. May be the extension is not installed, not enabled or failed to run|
| [WebElementNotRespondingError](./doc/api/python/exceptions/webelementnotrespondingerror.md) | WebElementNotRespondingError is raised when browser's visiting page is not responding|


