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
    &emsp;[UiElement](./uielement.md) object if it is found, or None if not

**Example:**

```python
from clicknium import clicknium as cc, locator, ui
    
ele = ui(locator.chrome.bing.li_dots_overflow)
first_child = ele.child(0)
```