---
sidebar_position: 4
---
# clicknium.wait_appear
***def wait_appear(
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        wait_timeout: int = 30
    ) -> UiElement***  

Wait for the UI element to appear and return it within specified timeout.

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the visit path of locator for target UI element, eg: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, and locator name is search_sb_form_q. For more details, please refer to [Locator](./../../../tutorial/locator.md).  
    &emsp;**locator_variables**: dict   
        &emsp;&emsp; locator variables, set to initialize parameters in locator, eg: `{ "row": 1,  "column": 1}`, more about variables, please refer to [Parametric Locator](./../../../tutorial/parametric_locator.md).   
    &emsp;**wait_timeout**: int  
        &emsp;&emsp; timeout for the waiting to appear, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;[UiElement](./../uielement/uielement.md) object, or None if the element does not appear.  


**Example:**
***
```python
from clicknium import clicknium as cc, locator

#wait element appear
cc.wait_appear(locator.chrome.bing.search_sb_form_q)

#parametric locator
variables = {"name":"test"}
cc.wait_appear(locator.notepad.notepad.document_151, variables)
```