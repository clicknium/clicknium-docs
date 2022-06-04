# Global functions
**Global functions provides methods over UI element, and driver for different types of applications.**

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
- window driver, `cc.window` return driver for [Window](./doc/api/python/window/window.md), window driver can be used to operate on the application window or dialog, such as maximize, minimize or restore the window
- sap driver, `cc.sap` return driver for [Sap](./doc/api/python/sap/sap.md), sap driver provides special methods for sap windows gui, such as login, call_transaction
- java driver, `cc.java` return driver for [Java](./doc/api/python/java/java.md), java driver provides method to install java extension

## methods <!-- {docsify-ignore} -->
- [clicknium.find_element](./doc/api/python/find_element.md): locate the UI element, return [UiElement](./doc/api/python/uielement/uielement.md) object
- [clicknium.find_elements](./doc/api/python/find_elements.md): get UI elements, return  list of [uielement](./doc/api/python/uielement/uielement.md) object
- [clicknium.is_exist](./doc/api/python/is_exist.md): whether the ui element exist
- [clicknium.wait_appear](./doc/api/python/wait_appear.md): wait for one ui element appear in specified timeout interval 
- [clicknium.wait_disappear](./doc/api/python/wait_disappear.md): wait for one ui element disappear in specified timeout interval
- [clicknium.wait_property](./doc/api/python/wait_property.md): wait for one ui element appear and one property's value equals the value specified in specified timeout interval 
- [clicknium.send_hotkey](./doc/api/python/send_hotkey.md): send hotkey to current cursor's position
- [clicknium.send_text](./doc/api/python/send_text.md): send text to current cursor's position

