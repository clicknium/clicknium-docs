# BrowserTab

**BrowserTab class provides ways to operate the browser tab and web UiElement with current browser tab.**

## properties <!-- {docsify-ignore} -->
- title: str, return title of current browser tab.
- url: str, return url of current browser tab.
- browser: [Browser](./doc/api/python/webdriver/browser/browser.md), return the browser which current tab belongs to.
  
## methods <!-- {docsify-ignore} -->
### operations related to [uielement](./doc/api/python/uielement/uielement.md) on current browser tab
- [find_element](./doc/api/python/webdriver/browser/find_element.md): locate the UI elements, and return [uielement](./doc/api/python/uielement/uielement.md) object.
- [find_elements](./doc/api/python/webdriver/browser/find_elements.md): get UI elements, and return  list of [uielement](./doc/api/python/uielement/uielement.md) object.
- [is_exist](./doc/api/python/webdriver/browser/is_exist.md): whether the UI elements exist.
- [wait_appear](./doc/api/python/webdriver/browser/wait_appear.md): wait for one UI element to appear in the given timeout interval, and return [uielement](./doc/api/python/uielement/uielement.md) object.
- [wait_disappear](./doc/api/python/webdriver/browser/wait_disappear.md): wait for one UI element to disappear in given timeout interval. 
- [wait_property](./doc/api/python/webdriver/browser/wait_property.md): wait for one UI element to appear and its value equals the expected value. 
- [set_property](./doc/api/python/webdriver/browser/set_property.md): set UI element's property value.
- [execute_js](./doc/api/python/webdriver/browser/execute_js.md): execute javascript code snippet for the target element.
- [execute_js_file](./doc/api/python/webdriver/browser/execute_js_file.md): execute javascript file for the target element.
  
### operations related to the current browser tab
- is_active: whether the current tab is active or not.  
  ***def is_active(self) -> bool***
- close: close the tab. If it is the only tab of current browser, the browser will be closed too.  
  ***def close(self) -> None***
- [goto](./doc/api/python/webdriver/browser/navigate.md): redirect current tab to the given url.
- [refresh](./doc/api/python/webdriver/browser/refresh.md): refresh the page of the current tab.
- activate: activate the current tab.  
  ***def activate(self,is_topmost: bool = True) -> None***