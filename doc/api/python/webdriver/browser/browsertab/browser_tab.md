# BrowserTab <!-- {docsify-ignore-all} -->

**BrowserTab class represents a web page to perform automation actions.**

## Properties
- `title`: str, return title of the browser tab.
- `url`: str, return url of the browser tab.
- `is_active`: bool, indicating whether the browser tab is active or not.
- `browser`: [Browser](./doc/api/python/webdriver/browser/browser.md), return the parent browser of the tab.

## Methods
**Operations related to [WebElement](./doc/api/python/webdriver/browser/browsertab/webelement/webelement.md) of current browser tab**
- [find_element](./doc/api/python/webdriver/browser/browsertab/find_element.md): return the Web element defined by the given locator.  
- [find_elements](./doc/api/python/webdriver/browser/browsertab/find_elements.md): return list of all matched Web elements by the given locator in current web page.  
- [is_existing](./doc/api/python/webdriver/browser/browsertab/is_existing.md): check whether the specified element of the web page exists.  
- [wait_appear](./doc/api/python/webdriver/browser/browsertab/wait_appear.md): wait for the specified element of the web page to appear within given timeout.  
- [wait_disappear](./doc/api/python/webdriver/browser/browsertab/wait_disappear.md): wait for the specified element of the web page to disappear within given timeout.  

**Operations related to the current browser tab**
- [activate](./doc/api/python/webdriver/browser/browsertab/activate.md): activate the browser tab.  
- [close](./doc/api/python/webdriver/browser/browsertab/close.md): close the browser tab. The browser will be closed too if no opened tab.  
- [goto](./doc/api/python/webdriver/browser/browsertab/goto.md): redirect current tab to the specified url.
- [refresh](./doc/api/python/webdriver/browser/browsertab/refresh.md): refresh current tab page.  
