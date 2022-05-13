# clicknium
**clicknium class provides global methods over UI element, and driver for different types of applications.**

- import
  ```
  from clicknium import clicknium as cc
  ```

## driver <!-- {docsify-ignore} -->
- web driver, through the following way can get web driver for different browser type, current support IE, chrome, edge, firefox
  - `cc.ie`: ie web driver
  - `cc.chrome`: chrome web driver
  - `cc.edge`: edge web driver
  - `cc.firefox`: firefox web driver

  &emsp;the [Webdriver](./doc/api/python/webdriver/webdriver.md) can be used to operate browser, such as open new browser, attach to existing browser window
- desktop driver, `cc.desktop` return driver for [Desktop](./doc/api/python/desktop/desktop.md), desktop driver can be used to operate on the desktop application window or dialog, such as maximize, minimize or restore the window
- sap driver, `cc.sap` return driver for [Sap](./doc/api/python/sap/sap.md), sap driver provides special methods for sap windows gui, such as login, call_transaction
- java driver, `cc.java` return driver for [Java](./doc/api/python/java/java.md), java driver provides method to install java extension

## methods <!-- {docsify-ignore} -->
- [find_element](./doc/api/python/find_element.md): locate the UI element, return [UiElement](./doc/api/python/uielement/uielement.md) object
- [is_exist](./doc/api/python/is_exist.md): whether the ui element exist
- [send_hotkey](./doc/api/python/send_hotkey.md): send hotkey
- [wait_appear](./doc/api/python/wait_appear.md): wait for one ui element appear in specified timeout interval 
- [wait_disappear](./doc/api/python/wait_disappear.md): wait for one ui element disappear in specified timeout interval
- [wait_property](./doc/api/python/wait_property.md): wait for one ui element appear and one property's value equals the value specified in specified timeout interval 

