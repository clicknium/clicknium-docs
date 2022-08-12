---
sidebar_position: 10
sidebar_label: scroll
---
# BrowserTab.scroll

***def scroll(
        self,
        delta_x: int = 0,
        delta_y: int = 0
    ) -> None***  

Scroll the current browser tab with the scroll bar.

**Parameters:**  
    &emsp;**delta_x**: int   
        &emsp;&emsp; pixels to scroll horizontally.  
    &emsp;**delta_y**: int   
        &emsp;&emsp; pixels to scroll vertically. 

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc

# open chrome browser
chrome_tab = cc.chrome.open("https://www.clicknium.com")

# scroll tab
chrome_tab.scroll(0, 500)
```