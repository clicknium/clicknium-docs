---
sidebar_position: 6
---
# clicknium.wait_disappear
***def wait_disappear(
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        wait_timeout: int = 30
    ) -> bool***  

Wait for the UI element to disappear within specified timeout.

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the visit path of locator for target UI element, eg: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, and locator name is search_sb_form_q. For more details, please refer to [Locator](./../../../concepts/locator.md).  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, set to initialize parameters in locator, eg: `{ "row": 1,  "column": 1}`, more about variables, please refer to [Parametric Locator](./../../../concepts/parametric_locator.md).  
    &emsp;**wait_timeout**: int  
        &emsp;&emsp; timeout for the waiting to disappear, the unit is second, and the default value is 30 seconds. 

**Returns:** bool  
    &emsp;Return True if the element disappears within timeout otherwise return False.


**Example:**
***
```python
from clicknium import clicknium as cc, locator

#wait element disappear
cc.wait_disappear(locator.chrome.bing.search_sb_form_q)

#parametric locator
variables = {"name":"test"}
cc.wait_disappear(locator.notepad.notepad.document_151, variables)
```