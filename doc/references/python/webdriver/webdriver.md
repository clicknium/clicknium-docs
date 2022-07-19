# WebDriver 

**WebDriver class provides methods to get browser object for web automation.**  

- `clicknium.ie`: IE web driver  
- `clicknium.chrome`: Chrome web driver  
- `clicknium.edge`: Edge web driver  
- `clicknium.firefox`: Firefox web driver  

## Properties
- `browsers`: List[[Browser](./browser/browser.md)], return all open browsers by current browser type.  
- `extension`: [WebExtension](./webextension/webextension.md), return the web extenion by current browser type.

## Methods
- [open](./open.md): open browser with the specified url, return a [BrowserTab](./browser/browsertab/browsertab.md) object.
- [attach](./attach.md): attach to an opened browser tab with the specified locator, return a [BrowserTab](./browser/browsertab/browsertab.md) object.
- [attach_by_title_url](./attach_by_title_url.md): attach to an opened browser tab with the specified title and/or url, return a [BrowserTab](./browser/browsertab/browsertab.md) object.

## Examples
```python
from clicknium import clicknium as cc

# install chrome extension to automate chrome browser
cc.chrome.extension.install()

# open chrome browser
cc.chrome.open("www.bing.com")
```
