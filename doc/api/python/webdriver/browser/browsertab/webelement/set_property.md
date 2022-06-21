# set property

***def set_property(
        self,
        name: str,
        value: str,
        timeout: int = 30
    ) -> None***  

Set UI element's property value.

**Parameters:**  
    &emsp;**name[Required]**: str  
        &emsp;&emsp; property name, different UI elements may support different property lists. For general property list, please refer to [Property List](./doc/automation/property.md)  
    &emsp;**value[Required]**: str  
        &emsp;&emsp; property value  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc, locator

chrome_tab = cc.chrome.open("https://bing.com")

# set the web propery with specified value
chrome_tab.set_property(locator.chrome.bing.search_sb_form_q, "tag", "search_tag")

# parametric locator
variables = {"name":"test"}
chrome_tab.set_property(locator.chrome.bing.search_sb_form_q, "tag", "search_tag", variables)

```