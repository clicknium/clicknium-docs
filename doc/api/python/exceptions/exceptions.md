# Exceptions

Exception is raised whenever a certain operation is terminated abnormally. Besides python [Built-in Exceptions](https://docs.python.org/3/library/exceptions.html#built-in-exceptions), we also define clicknium exceptions which all inherit from [BaseError](./doc/api/python/exceptions/baseerror.md).


## Clicknium Exceptions <!-- {docsify-ignore} -->

| Exception      | Description |
| -----------| ----------- |
| [BaseError](./doc/api/python/exceptions/baseerror.md) |All Clicknium exceptions inherit from this class.|
| [ArgumentError](./doc/api/python/exceptions/argumenterror.md) | ArgumentError is raised when at least one of the arguments provided to a method is not valid.|
| [ArgumentNullError](./doc/api/python/exceptions/argumentnullerror.md) | ArgumentNullError is raised when a null reference is passed to a method that does not accept it as a valid argument.|
| [ArgumentOutOfRangeError](./doc/api/python/exceptions/argumentoutofrangeerror.md) | ArgumentOutOfRangeError is raised when the value of an argument is out of the allowable range of values as defined by the invoked method.|
| [BrowserNotInstallError](./doc/api/python/exceptions/browsernotinstallerror.md) | BrowserNotInstallError is raised when the specified browser is not installed.|
| [BrowserNotRunError](./doc/api/python/exceptions/browsernotrunerror.md) | BrowserNotRunError is raised when the specified browser is not running.|
| [ElementNotFoundError](./doc/api/python/exceptions/elementcannotfounderror.md) | ElementNotFoundError is raised when the target UI element can not be found by the given locator.|
| [ExtensionOperationError](./doc/api/python/exceptions/extensionoperationerror.md) | ExtensionOperationError is raised when an extension fails in operation "install", "update" or "uninstall".|
| [InvalidOperationError](./doc/api/python/exceptions/invalidoperationerror.md)   | InvalidOperationError is raised when a method call is invalid for the object's current state.|
| [InvalidSelectedItemError](./doc/api/python/exceptions/invalidselecteditemerror.md)   | InvalidSelectedItemError is raised when the item to be selected is invalid for the object's current state.|
| [LocatorRequestError](./doc/api/python/exceptions/locatorrequesterror.md) | LocatorRequestError is raised when the cloud locator cannot be acquired due to server request error.|
| [LocatorUndefinedError](./doc/api/python/exceptions/locatorundefinederror.md) | LocatorUndefinedError is raised when the specified locator can not be found in locator store.|
| [NotSupportedError](./doc/api/python/exceptions/notsupportederror.md) | NotSupportedError is raised when an invoked method is not supported, or when an attempt to read, seek, or write to a stream that does not support the invoked functionality.|
| [NotSupportedOperationError](./doc/api/python/exceptions/notsupportedoperationerror.md) | NotSupportedOperationError is raised when the method is invoked by a UI element which does not support the type of operation.|
| [NotSupportedOperationOptionError](./doc/api/python/exceptions/notsupportedoperationoptionerror)   | NotSupportedOperationOptionError is raised when the specified option value is not supported by the target UI element.|
| [OperationTimeoutError](./doc/api/python/exceptions/timeoutoperationerror.md) | OperationTimeoutError is raised when a certain operation is not completed within given time.|
| [ProjectSettingNotFoundError](./doc/api/python/exceptions/projectsettingnotfounderror.md) | ProjectSettingNotFoundError is raised when project setting file 'app.yaml' is missing.|
| [ScreenOperationError](./doc/api/python/exceptions/screenoperationerror.md)   | ScreenOperationError is raised when screen operations of window desktop UI element fail.|
| [UiaPatternNotFoundError](./doc/api/python/exceptions/uiapatternnotfounderror.md)   | UiaPatternNotFoundError is raised when a window UI element can not be found by UIA technology.|
| [UnAuthorizedError](./doc/api/python/exceptions/unauthoriederror.md) | UnAuthorizedError is raised when user does not sign in or the sign in state is expired.|
| [UnreachableBrowserExtensionError](./doc/api/python/exceptions/unreachablebrowserextensionerror.md) | UnreachableBrowserExtensionError is raised when the specified browser's extension is not in ready state. Please check if the extension is installed and enabled.|
| [WebElementNotRespondingError](./doc/api/python/exceptions/webelementnotrespondingerror.md) | WebElementNotRespondingError is raised when the web page is not responding.|
| [WebError](./doc/api/python/exceptions/weberror.md) | WebError is raised for common web automation exceptions.|
| [WindowError](./doc/api/python/exceptions/windowerror.md)   | WindowError is raised for common window exceptions.|
| [WindowsNativeError](./doc/api/python/exceptions/windowsnativeerror.md)   | WindowsNativeError is raised when an underneath win32 method fails.|


