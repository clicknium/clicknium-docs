---
sidebar_position: 3
---
# clicknium.is_existing
***def is_existing(
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        timeout: int = 30
    ) -> bool***  

Check whether the UI element exists or not.

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the visit path of locator for target UI element, eg: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, and locator name is search_sb_form_q. For more details, please refer to [Locator](./../../../tutorial/locator.md).  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, set to initialize parameters in locator, eg: `{ "row": 1,  "column": 1}`, more about variables, please refer to [Parametric Locator](./../../../tutorial/parametric_locator.md).  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for locating the target UI element, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;Return True if the UI element exists, otherwise return False.

**Example:**
***
```python
from clicknium import clicknium as cc, locator

cc.is_existing(locator.chrome.bing.search_sb_form_q)

#parametric locator
variables = {"name":"test"}
cc.is_existing(locator.chrome.bing.search_sb_form_q, variables)
```