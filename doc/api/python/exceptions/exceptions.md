# Exceptions

Exception is raised whenever certain operations are terminated abnormally. Except for python [Built-in Exceptions](https://docs.python.org/3/library/exceptions.html#built-in-exceptions), we also define custom clicknium exceptions, which are all inherit from [BaseError](./doc/api/python/exceptions/baseerror.md).


## Clicknium Exceptions <!-- {docsify-ignore} -->

| Exception Name      | Description |
| -----------| ----------- |
| BaseError  |All Clicknium exceptions inherit from this class|
| ArgumentError   |  ArgumentError is raised when one of the arguments provided to a method is not valid|
| ArgumentNullError | ArgumentNullError is raised when a null reference is passed to a method that does not accept it as a valid argument|
| ArgumentOutOfRangeError   | ArgumentOutOfRangeError is raised when the value of an argument is outside the allowable range of values as defined by the invoked method|
| LocatorUndefinedError | LocatorUndefinedError is raised when the specified locator can not be found in locator store|
| TimeoutOperationError   | TimeoutOperationError is raised when certain operation is terminated due to timeout|
| ElementCanNotFoundError   | ElementCanNotFoundError is raised when the loactor can be found in locator store, but the returned ui element can not be found|
| ExtensionOperationError | ExtensionOperationError is raised when the specified extension with oparetion "install", "update", or "uninstall" failed|
| NotSupportedError   | NotSupportedError is raised when an invoked method is not supported, or when there is an attempt to read, seek, or write to a stream that does not support the invoked functionality|
| NotSupportedOperationError   | NotSupportedOperationError is raised when an invoked method, its automation technology or operation is not supported for the target. ex: can not set text for an image uielement |
| NotSupportedOperationOptionError   | NotSupportedOperationOptionError is raised when an invoked method is supported for the target, but the specified option value is not supported. ex: can not clear text for desktop uielement with clear method option set to `ControlClearValue`|
| InvalidOperationError   |  InvalidOperationError is raised when a method call is invalid for the object's current state|
| InvalidSelectedItemError   | InvalidSelectedItemError is raised when a method call is valid for the object, but the set value is invalid for the object's current value. ex: can not select an invalid item for select item method|
| DesktopError   | DesktopError is raised for common desktop exceptions|
| WindowsNativeError   | WindowsNativeError is raised when a method call with win32 native has any exceptions|
| UiaPatternNotFoundError   | UiaPatternNotFoundError is raised when a desktop uielement with uia technology can not be found|
| ScreenOperationError   | ScreenOperationError is raised when screen operations with desktop uielement has any exceptions|
| WebError | WebError is raised for common web automation exceptions|
| BrowserNotRunError | BrowserNotRunError is raised when the specified browser is not run|
| BrowserNotInstallError | BrowserNotInstallError is raised when the specified browser is not installed|
| UnreachableBrowserExtensionError | UnreachableBrowserExtensionError is raised when the specified browser's extension not in ready state. May be the extension is not installed, not enabled or failed to run|
| WebElementNotRespondingError | WebElementNotRespondingError is raised when browser's visiting page is not responding|


