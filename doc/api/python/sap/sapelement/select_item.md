# SapElement.select_item

***def select_item(
        self,
        item: str,
        timeout: int = 30
    ) -> None***  

Select the SAP item.

**Parameters:**  
    &emsp;**item[Required]**: str  
        &emsp;&emsp; item string, the item to be selected.
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc, locator

# get sap driver
sap_driver = cc.sap

# login sap application
sap_driver.login("path", "connection", "client", "username", "password")

# find sap element
sap_ele = sap_driver.find_element(locator.sap.item_q)

# select item
sap_ele.select_item("item1")
```