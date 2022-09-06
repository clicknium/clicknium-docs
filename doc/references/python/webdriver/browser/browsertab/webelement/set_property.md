---
sidebar_position: 2
sidebar_label: set_property
---
# WebElement.set property

***def set_property(
        self,
        name: str,
        value: str,
        timeout: int = 30
    ) -> None***  

Set the property value of the web element.  

**Parameters:**  
    &emsp;**name[Required]**: str  
        &emsp;&emsp; Property name, different UI elements may support different properties. Please refer to [Automation Concepts](./../../../../../../concepts/concepts.md) to check the properties according to the UI element types.  
    &emsp;**value[Required]**: str  
        &emsp;&emsp; Property value.    
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc, locator

chrome_tab = cc.chrome.open("https://bing.com")

# set the web propery with specified value
chrome_tab.find_element(locator.chrome.bing.search_sb_form_q).set_property("tag", "search_tag")
```