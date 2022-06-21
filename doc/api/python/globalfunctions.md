# Global functions <!-- {docsify-ignore-all} -->
**Global functions provides methods to UI element, and the driver of applications with different types.**

- import
  ```
  from clicknium import clicknium as cc
  ```

## driver 
- web driver, get web driver with different browsers by the following way, currently supporting IE, Chrome, Edge, Firefox  
  - `cc.ie`: IE web driver
  - `cc.chrome`: Chrome web driver
  - `cc.edge`: Edge web driver
  - `cc.firefox`: Firefox web driver  
the [Webdriver](./doc/api/python/webdriver/webdriver.md) can be used to operate browser, eg: open new browser, attach to existing browser window
- window driver, `cc.window` return driver for [Window](./doc/api/python/window/window.md), window driver can be used to operate on the application window or dialog, eg: maximize, minimize or restore the window
- sap driver, `cc.sap` return driver for [Sap](./doc/api/python/sap/sap.md), sap driver provides special methods to sap windows gui, eg: login and call_transaction
- java driver, `cc.java` return driver for [Java](./doc/api/python/java/java.md), java driver provides method to installing java extension

## methods
- [clicknium.find_element](./doc/api/python/find_element.md): initialize UI element by the given locator, return [UiElement](./doc/api/python/uielement/uielement.md) object
- [clicknium.find_elements](./doc/api/python/find_elements.md): find elements by the given locator, currently only supporting web automation, return list of [UiElement](./doc/api/python/uielement/uielement.md) object
- [clicknium.is_exist](./doc/api/python/is_exist.md): check whether the ui element exists or not
- [clicknium.wait_appear](./doc/api/python/wait_appear.md): wait for the UI element to appear in specified timeout interval 
- [clicknium.wait_disappear](./doc/api/python/wait_disappear.md): wait for the UI element to disappear in specified timeout interval
- [clicknium.send_hotkey](./doc/api/python/send_hotkey.md): send hotkey to the current cursor's position
- [clicknium.send_text](./doc/api/python/send_text.md): send text to the current cursor's position

