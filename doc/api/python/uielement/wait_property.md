# wait_property
***def wait_property(
        self,
        name: str, 
        value: str, 
        wait_timeout: int = 30
    ) -> bool***  

Wait for the element's value of specified property to be the same as expected.

**Parameters:**  
    &emsp;**name[Required]**: str  
        &emsp;&emsp; property name, different UI elements may support different property lists. For general property list, please refer to [Property List](./doc/automation/property.md)  
    &emsp;**value[Required]**: str  
        &emsp;&emsp; expected property value  
    &emsp;**timeout**: int  
        &emsp;&emsp; wait timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;bool, return True if the UI element exists and the property value equals the expected one, otherwise return False.

**Example:**
***
```python
from clicknium import clicknium as cc, locator

chrome_tab = cc.chrome.open("https://bing.com")

# wait for the propery with expected value
chrome_tab.wait_property(locator.chrome.bing.search_sb_form_q)

# parametric locator, wait for the element to be enabled, for example, the element is blocked by one popup dialog
variables = {"name":"test"}
chrome_tab.wait_property(locator.chrome.bing.search_sb_form_q, variables)

```