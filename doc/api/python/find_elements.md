# clicknium.find_elements
***def find_elements(
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        timeout: int = 30
    ) -> List[UiElement]***  

Find elements by the given locator.  

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the name of one locator in locator store, ex: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, locator name is search_sb_form_q  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, is set to initialize parameters in locator, ex: var_dict = { "row": 1,  "column": 1}, more about variable, please refer to [parametric locator](./doc/automation/parametric_locator.md)  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, unit is second, default value is 30 seconds 

**Returns:**  
    &emsp;list of [UiElement](./doc/api/python/uielement/uielement.md) object

**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui

    elements = cc.find_elements(locator.chrome.bing.search_sb_form_q)

    for ele in elements:
        ele.highlight()
```