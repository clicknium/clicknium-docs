# Exceptions

Exception is raised whenever a certain operation is terminated abnormally. Besides python [Built-in Exceptions](https://docs.python.org/3/library/exceptions.html#built-in-exceptions), we also define clicknium exceptions which all inherit from [BaseError](./baseerror.md).


## Clicknium Exceptions 

| Exception      | Description |
| -----------| ----------- |
| [BaseError](./baseerror.md) |All Clicknium exceptions inherit from this class.|
| [ArgumentError](./argumenterror.md) | ArgumentError is raised when at least one of the arguments provided to a method is not valid.|
| [ArgumentNullError](./argumentnullerror.md) | ArgumentNullError is raised when a null reference is passed to a method that does not accept it as a valid argument.|
| [ArgumentOutOfRangeError](./argumentoutofrangeerror.md) | ArgumentOutOfRangeError is raised when the value of an argument is out of the allowable range of values as defined by the invoked method.|
| [BrowserNotInstallError](./browsernotinstallerror.md) | BrowserNotInstallError is raised when the specified browser is not installed.|
| [BrowserNotRunError](./browsernotrunerror.md) | BrowserNotRunError is raised when the specified browser is not running.|
| [ElementNotFoundError](./elementcannotfounderror.md) | ElementNotFoundError is raised when the target UI element can not be found by the given locator.|
| [ExtensionOperationError](./extensionoperationerror.md) | ExtensionOperationError is raised when an extension fails in operation "install", "update" or "uninstall".|
| [InvalidOperationError](./invalidoperationerror.md)   | InvalidOperationError is raised when a method call is invalid for the object's current state.|
| [InvalidSelectedItemError](./invalidselecteditemerror.md)   | InvalidSelectedItemError is raised when the item to be selected is invalid for the object's current state.|
| [LocatorRequestError](./locatorrequesterror.md) | LocatorRequestError is raised when the cloud locator cannot be acquired due to server request error.|
| [LocatorUndefinedError](./locatorundefinederror.md) | LocatorUndefinedError is raised when the specified locator can not be found in locator store.|
| [NotSupportedError](./notsupportederror.md) | NotSupportedError is raised when an invoked method is not supported, or when an attempt to read, seek, or write to a stream that does not support the invoked functionality.|
| [NotSupportedOperationError](./notsupportedoperationerror.md) | NotSupportedOperationError is raised when the method is invoked by a UI element which does not support the type of operation.|
| [NotSupportedOperationOptionError](./notsupportedoperationoptionerror)   | NotSupportedOperationOptionError is raised when the specified option value is not supported by the target UI element.|
| [OperationTimeoutError](./timeoutoperationerror.md) | OperationTimeoutError is raised when a certain operation is not completed within given time.|
| [ProjectSettingNotFoundError](./projectsettingnotfounderror.md) | ProjectSettingNotFoundError is raised when project setting file 'clicknium.yaml' is missing.|
| [ScreenOperationError](./screenoperationerror.md)   | ScreenOperationError is raised when screen operations of window desktop UI element fail.|
| [UiaPatternNotFoundError](./uiapatternnotfounderror.md)   | UiaPatternNotFoundError is raised when a window UI element can not be found by UIA technology.|
| [UnAuthorizedError](./unauthoriederror.md) | UnAuthorizedError is raised when user does not sign in or the sign in state is expired.|
| [UnreachableBrowserExtensionError](./unreachablebrowserextensionerror.md) | UnreachableBrowserExtensionError is raised when the specified browser's extension is not in ready state. Please check if the extension is installed and enabled.|
| [WebElementNotRespondingError](./webelementnotrespondingerror.md) | WebElementNotRespondingError is raised when the web page is not responding.|
| [WebError](./weberror.md) | WebError is raised for common web automation exceptions.|
| [WindowError](./windowerror.md)   | WindowError is raised for common window exceptions.|
| [WindowsNativeError](./windowsnativeerror.md)   | WindowsNativeError is raised when an underneath win32 method fails.|


