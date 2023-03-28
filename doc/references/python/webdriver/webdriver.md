# WebDriver 

**WebDriver class provides methods to get browser object for web automation.**  

- `clicknium.ie`: IE web driver  
- `clicknium.chrome`: Chrome web driver  
- `clicknium.chromecdp`: Chrome web driver with Chrome DevTools Protocol(CDP)  
- `clicknium.edge`: Edge web driver  
- `clicknium.edgecdp`: Edge web driver with Chrome DevTools Protocol(CDP)   
- `clicknium.firefox`: Firefox web driver 
- `clicknium.chromium()`: Chromium based web driver, such as "brave", "vivaldi" and so on 

`clicknium.chromecdp` and `clicknium.edgecdp` can run without browser automation extension and support headless mode.   

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

# open chrome browser via CDP
cc.chromecdp.open("www.bing.com")

# open chrome browser via CDP with headless mode 
cc.chromecdp.open("www.bing.com", args=["--headless"])

# open chromium based browser
cc.chromium('vivaldi').open("https://www.bing.com", timeout = 10)
cc.chromium('brave').open("https://www.bing.com", timeout = 10)
```
