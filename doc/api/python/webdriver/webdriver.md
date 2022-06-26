# WebDriver <!-- {docsify-ignore-all} -->

**WebDriver class provides methods to get browser object for web automation.**  

- `clicknium.ie`: IE web driver  
- `clicknium.chrome`: Chrome web driver  
- `clicknium.edge`: Edge web driver  
- `clicknium.firefox`: Firefox web driver  

## Properties
- `browsers`: List[[Browser](./doc/api/python/webdriver/browser/browser.md)], return all open browsers by current browser type.  
- `extension`: [WebExtension](./doc/api/python/webdriver/webextension/webextension.md), return the web extenion by current browser type.

## Methods
- [open](./doc/api/python/webdriver/open.md): open browser with the specified url, return a [BrowserTab](./doc/api/python/webdriver/browser/browsertab/browser_tab.md) object.
- [attach](./doc/api/python/webdriver/attach.md): attach to an opened browser tab with the specified locator, return a [BrowserTab](./doc/api/python/webdriver/browser/browsertab/browser_tab.md) object.
- [attach_by_title_url](./doc/api/python/webdriver/attach_by_title_url.md): attach to an opened browser tab with the specified title and/or url, return a [BrowserTab](./doc/api/python/webdriver/browser/browsertab/browser_tab.md) object.

## Examples
```python
from clicknium import clicknium as cc

# install chrome extension to automate chrome browser
cc.chrome.extension.install()

# open chrome browser
cc.chrome.open("www.bing.com")
```
