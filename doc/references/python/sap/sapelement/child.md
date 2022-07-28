---
sidebar_position: 1
---
# child
***def child(self, index: int)***  

Get child element with index.

> **Remarks:**
>- The index starts from 0.

**Parameters:**    
    &emsp;**index[Required]**: int  
        &emsp;&emsp; index specified, get the nth child

**Returns:**  
    &emsp;[SapElement](./sapelement.md) object if it is found, or None if not

**Example:**

```python
from clicknium import clicknium as cc, locator, ui
    
# get sap driver
sap_driver = cc.sap

# login sap application
sap_driver.login("path", "connection", "client", "username", "password")

# find sap element
sap_ele = sap_driver.find_element(locator.sap.item_q)

# get first child
first_child = sap_ele.child[0]
```