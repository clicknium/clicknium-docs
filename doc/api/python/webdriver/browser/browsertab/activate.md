# BrowserTab.activate

***def activate(
        self,
        is_topmost: bool = True
    ) -> None***  

Activate the browser tab.  

**Parameters:**  
    &emsp;**is_topmost**: bool    
        &emsp;&emsp; it defines whether to set the browser window to topmost.  

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc

# open chrome browser
chrome_tab = cc.chrome.open("https://www.bing.com")

# activate the tab
chrome_tab.activate()
```