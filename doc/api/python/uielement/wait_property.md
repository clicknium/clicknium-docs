# wait_property
***def wait_property(
        self,
        name: str, 
        value: str, 
        wait_timeout: int = 30
    ) -> bool***  

Wait for the target element's property to be expected value within specified timeout. 

**Parameters:**  
    &emsp;**name[Required]**: str  
        &emsp;&emsp; property name, different UI elements may support different properties. For general properties, please refer to [Property List](./../../../automation/property.md).  
    &emsp;**value[Required]**: str  
        &emsp;&emsp; expected property value.  
    &emsp;**timeout**: int  
        &emsp;&emsp; wait timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;bool, return True if the UI element exists and its property value is expected, otherwise return False.

**Example:**
***
```python
from clicknium import clicknium as cc, locator

tab = cc.chrome.open("https://bing.com")

tab.find_element(locator.chrome.bing.search_sb_form).wait_property("aria-expanded", "true")

```