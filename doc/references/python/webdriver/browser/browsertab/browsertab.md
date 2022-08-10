# BrowserTab

**BrowserTab class represents a web page to perform automation actions.**

## Properties
- `title`: str, return title of the browser tab.
- `url`: str, return url of the browser tab.
- `is_active`: bool, indicating whether the browser tab is active or not.
- `browser`: [Browser](./../browser.md), return the parent browser of the tab.

## Methods
**Operations related to [WebElement](./webelement/webelement.md) of current browser tab**
- [find_element](./find_element.md): return the Web element defined by the given locator.  
- [find_elements](./find_elements.md): return list of all matched Web elements by the given locator in current web page.  
- [is_existing](./is_existing.md): check whether the specified element of the web page exists.  
- [wait_appear](./wait_appear.md): wait for the specified element of the web page to appear within given timeout.  
- [wait_disappear](./wait_disappear.md): wait for the specified element of the web page to disappear within given timeout.  

**Operations related to the current browser tab**
- [activate](./activate.md): activate the browser tab.  
- [close](./close.md): close the browser tab. The browser will be closed too if no opened tab.  
- [goto](./goto.md): redirect current tab to the specified url.
- [refresh](./refresh.md): refresh current tab page.  
- [scroll](./scroll.md)：scroll current browser tab, if it has scroll bar.
