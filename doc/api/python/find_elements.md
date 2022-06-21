# clicknium.find_elements
***def find_elements(
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        timeout: int = 30
    ) -> List[UiElement]***  

Find elements by the given locator, currently only supporting web automation.

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the name of one locator in locator store, eg: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, and locator name is search_sb_form_q  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, set to initialize parameters in locator, eg: var_dict = { "row": 1,  "column": 1}, more about variables, please refer to [Parametric Locator](./doc/automation/parametric_locator.md)  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;list of [UiElement](./doc/api/python/uielement/uielement.md) object

**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui

    cc.edge.open("https://www.bing.com/")
    ui(locator.new_store.sample.bing.search_sb_form_q).set_text('clicknium')
    ui(locator.new_store.sample.bing.svg).click()

    result_elements = ui(locator.new_store.sample.bing.a_search_result)
    for elem in result_elements:
        elem.highlight(duration=1)
```