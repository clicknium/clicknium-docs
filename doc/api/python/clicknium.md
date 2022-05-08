# clicknium
clicknium class provides global methods over UI element, and driver for different type of application.

- import
  ```
  from clicknium import clicknium as cc
  ```

## driver
- web driver, through the following way can get web driver for different browser type, current support IE, chrome, edge, firefox
  - cc.ie: ie web driver
  - cc.chrome: chrome web driver
  - cc.edge: edge driver
  - cc.firefox: firefox driver

the [webdriver](web/webdriver.md) can be used to operate browser, such as open new browser, attach to existing browser window
- desktop driver, `cc.desktop` return driver for [desktop](desktop/desktop.md), desktop driver can be used to operate on the desktop application window or dialog, such as maximize, minimize or restore the window.
- sap driver, `cc.sap` return driver for [sap](sap/sap.md), sap driver provides special methods for sap windows gui, such as login, call_transaction.
- java driver, `cc.java` return driver for [java](java/java.md), java driver provides method to install java extension.
  
## methods
- [find_element](find_element.md): locate the UI element, return [uielement](uielement/uielement.md) object
- [is_exist](is_exist.md): whether the ui element exist
- [send_hotkey](./doc/api/python/send_hotkey.md): send hotkey
- [wait_appear](./doc/api/python/wait_appear.md): wait for one ui element appear in the timeout interval specified
- [wait_disappear](./doc/api/python/wait_disappear.md): wait for one ui element disappear in the timeout interval specified
- [wait_property](./doc/api/python/wait_property.md): wait for one ui element appear and one property's value equals the value specified 

