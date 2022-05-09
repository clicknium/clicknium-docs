# wait_appear
***def wait_appear(selector_locator, selector_variables = {}, wait_timeout = 30)***  

wait for the element appear

**Parameters:**  
    &emsp;**locator[Required]**: str   
        &emsp;&emsp; locator string, the name of one locator in locator store, ex: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, locator name is search_sb_form_q  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; The locator variables, is set to initialize parameters in locator, ex: var_dict = { "row": 1,  "column": 1}, more about variable, please refer to [parametric locator](/doc/api/python/parametric_locator.md)  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the method call, unit is second, default value is 30 seconds 

**Returns:**  
    &emsp;UiElement, return UiElement or None if the element is not appear


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