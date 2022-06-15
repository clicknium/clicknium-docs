# clicknium.is_exist
***def is_exist(
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        timeout: int = 30
    ) -> bool***  

Check whether the ui element exist or not.  

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the name of one locator in locator store, eG: 'locator.chrome.bing.search_sb_form_q', and locator store is chrome, locator name is search_sb_form_q  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables,  set to initialize parameters in locator, eg: var_dict = { "row": 1,  "column": 1}, more about variables, please refer to [parametric locator](./doc/automation/parametric_locator.md)  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;return True if the UI element exists, otherwise return False

**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui

    cc.is_exist(locator.chrome.bing.search_sb_form_q)

    #parametric locator
    variables = {"name":"test"}
    cc.is_exist(locator.chrome.bing.search_sb_form_q, variables)
```