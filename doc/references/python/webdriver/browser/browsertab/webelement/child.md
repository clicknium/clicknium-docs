---
sidebar_position: 1
---
# child
```python
def child(self, index: int)
```  

Get child element with index.

> **Remarks:**
>- The index starts from 0.

**Parameters:**    
    &emsp;**index[Required]**: int  
        &emsp;&emsp; index specified, get the nth child

**Returns:**  
    &emsp;[WebElement](./webelement.md) object if it is found, or None if not

**Example:**

```python
from clicknium import clicknium as cc, locator, ui
    
chrome_tab = cc.chrome.open("https://bing.com")

# get web element
ele = chrome_tab.find_element(locator.chrome.bing.search_sb_form_q)

# get element's first child
first_child = ele.child[0]
```