# clicknium.wait_disappear
***def wait_disappear(
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        wait_timeout: int = 30
    ) -> bool***  

Wait for the UI element to disappear in the given time.

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the name of one locator in locator store, eg: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, and locator name is search_sb_form_q  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, set to initialize parameters in locator, eg: var_dict = { "row": 1,  "column": 1}, more about variables, please refer to [Parametric Locator](./doc/automation/parametric_locator.md)  
    &emsp;**timeout**: int  
        &emsp;&emsp; wait timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;bool, return True if the element disappears or return False


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