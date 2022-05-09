# is_exist
***def is_exist(locator, locator_variables = {}, timeout = 30)***  

check whether the ui element exist or not.  

**Parameters:**  
    &emsp;**locator[Required]**: str   
        &emsp;&emsp; locator string, the name of one locator in locator store, ex: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, locator name is search_sb_form_q
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; The locator variables, is set to initialize parameters in locator, ex: var_dict = { "row": 1,  "column": 1}, more about variable, please refer to [parametric locator](/doc/api/python/parametric_locator.md)  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the method call, unit is second, default value is 30 seconds 

**Returns:**  
    &emsp;return True if ui element exist, or return False

**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui

    cc.is_exist(locator.chrome.bing.search_sb_form_q)

    #parametric locator
    variables = {"name":"test"}
    cc.is_exist(locator.chrome.bing.search_sb_form_q, variables)
```