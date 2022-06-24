# BrowserTab <!-- {docsify-ignore-all} -->

**BrowserTab class provides methods to operate the browser tab and WebElement with current browser tab.**

## properties
- `title`: str, return title of the current browser tab.
- `url`: str, return url of the current browser tab.
- `is_active`: bool, whether the current tab is active or not.
- `browser`: [Browser](./doc/api/python/webdriver/browser/browser.md), return the browser which current tab belongs to.

## methods
**operations related to [WebElement](./doc/api/python/webdriver/browser/browsertab/webelement/webelement.md) on current browser tab**
- [find_element](./doc/api/python/webdriver/browser/browsertab/find_element.md): initialize UI element by the given locator in currently open browser, return [WebElement](./doc/api/python/webdriver/browser/browsertab/webelement/webelement.md) object
- [find_elements](./doc/api/python/webdriver/browser/browsertab/find_elements.md): find elements by the given locator, return list of [WebElement](./doc/api/python/webdriver/browser/browsertab/webelement/webelement.md) object
- [is_existing](./doc/api/python/webdriver/browser/browsertab/is_existing.md): check whether the UI element exists in currently open browser
- [wait_appear](./doc/api/python/webdriver/browser/browsertab/wait_appear.md): wait for the element to appear in currently open browser in the give time, return [WebElement](./doc/api/python/webdriver/browser/browsertab/webelement/webelement.md) object
- [wait_disappear](./doc/api/python/webdriver/browser/browsertab/wait_disappear.md): wait for the UI element to disappear in given time in currently opened browser

**operations related to the current browser tab**
- [close](./doc/api/python/webdriver/browser/browsertab/close.md): close the tab. If it is the only tab of current browser, the browser will be closed too 
- [goto](./doc/api/python/webdriver/browser/browsertab/goto.md): redirect current tab to the given url
- [refresh](./doc/api/python/webdriver/browser/browsertab/refresh.md): refresh the page of the current tab
- [activate](./doc/api/python/webdriver/browser/browsertab/activate.md): activate the current tab