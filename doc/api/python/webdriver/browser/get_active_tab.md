# browser.get_active_tab

***def get_active_tab(self) -> BrowserTab***  

Get browser's current active tab.

**Returns:**  
    &emsp;[BrowserTab](./doc/api/python/webdriver/browser/browser_tab.md) object, you can execute following operations in the browser tab: find_element, find_elements, close, refresh and so on.

**Example:**
***
```python
from clicknium import clicknium as cc

# get browser with type chrome
browser = cc.chrome.browsers[0]

# get active tab
tab = browser.get_active_tab()

# get tab's title
title = tab.title
print(title)
```