# get_property
```python
def get_property(
        self,
        name: str,
        timeout: int = 30
    ) -> str
``` 

Get property value of the target element.  

**Parameters:**   
    &emsp;**name [Required]**: str  
        &emsp;&emsp; Property name, different UI elements may support different properties. For specific properties, please refer to [Automation Concept](./../../../concepts/concepts.md).  
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation, the unit is second, and the default value is 30 seconds.

**Returns:**  
    &emsp;str

**Example:**
***
```python
from clicknium import clicknium as cc, locator, ui
    
tag = ui(locator.chrome.bing.search_sb_form_q).get_property("tag")
```