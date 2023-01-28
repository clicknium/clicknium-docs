---
sidebar_position: 5
---
# clicknium.wait_disappear
```python 
def wait_disappear(
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        wait_timeout: int = 30
    ) -> bool
```

Wait for the UI element to disappear within specified timeout.

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; Locator string, the visit path of locator for target UI element, eg: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, and locator name is search_sb_form_q. For more details, please refer to [Locator](./../../../concepts/locator.md).  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; Locator variables, set to initialize parameters in locator, eg: `{ "row": 1,  "column": 1}`, more about variables, please refer to [Parametric Locator](./../../../concepts/locator.md#parametric-locator).  
    &emsp;**wait_timeout**: int  
        &emsp;&emsp; Timeout for the waiting to disappear, the unit is second, and the default value is 30 seconds. 

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