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
- [find_element_by_xpath](./find_element_by_xpath.md): find element by the given xpath.  
- [find_element_by_css_selector](./find_element_by_css_selector.md): find element by the given css selector.
- [find_elements](./find_elements.md): return list of all matched Web elements by the given locator in current web page.  
- [find_elements_by_xpath](./find_elements_by_xpath.md): find elements by the given xpath.
- [find_elements_by_css_selector](./find_elements_by_css_selector.md): find elements by the given css selector.
- [is_existing](./is_existing.md): check whether the specified element of the web page exists.  
- [is_existing_by_xpath](./is_existing_by_xpath.md): check whether the ui element exist or not by the given xpath.
- [is_existing_by_css_selector](./is_existing_by_css_selector.md): check whether the ui element exist or not by the given css selector.
- [wait_appear](./wait_appear.md): wait for the specified element of the web page to appear within given timeout.  
- [wait_appear_by_xpath](./wait_appear_by_xpath.md): wait for the element appear by the given xpath.
- [wait_appear_by_css_selector](./wait_appear_by_css_selector.md): wait for the element appear by the given css selector.
- [wait_disappear](./wait_disappear.md): wait for the specified element of the web page to disappear within given timeout.  
- [wait_disappear_by_xpath](./wait_disappear_by_xpath.md): wait for the element disappear by the given xpath.
- [wait_disappear_by_css_selector](./wait_disappear_by_css_selector.md): wait for the element disappear by the given css selector.

**Operations related to the current browser tab**
- [activate](./activate.md): activate the browser tab.  
- [close](./close.md): close the browser tab. The browser will be closed too if no opened tab.  
- [goto](./goto.md): redirect current tab to the specified url.
- [refresh](./refresh.md): refresh current tab page.  
- [scroll](./scroll.md)：scroll the current browser tab with the scroll bar.
