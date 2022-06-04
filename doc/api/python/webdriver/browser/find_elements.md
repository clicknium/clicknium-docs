# find_elements
***def find_elements(
        self,
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        timeout: int = 30
    ) -> List[UiElement]***  

Find elements by the given locator.  

> **Remarks:**  
It should be used like `clicknium.chrome.open("https://bing.com").find_elements()`, it is different with `clicknium.find_elements()` [clicknium.find_elements](./doc/api/python/find_elements.md) when locating the ui elements.
>- `clicknium.find_elements()` is for both web and desktop's uielements, and does not specified a scope to locate the elements
>- `clicknium.chrome.open("https://bing.com").find_elements()` will locate elements in the specified browser

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the name of one locator in locator store, ex: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, locator name is search_sb_form_q  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, is set to initialize parameters in locator, ex: var_dict = { "row": 1,  "column": 1}, more about variable, please refer to [parametric locator](./doc/automation/parametric_locator.md)  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, unit is second, default value is 30 seconds

**Returns:**  
    &emsp;[UiElement](./doc/api/python/uielement/uielement.md) object, you can use the uielement to do the following operation, such as click, set_text, before operating, it will try locate the element to verify whether the element exist&emsp;list of [UiElement](./doc/api/python/uielement/uielement.md) object, you can use each of the uielement to do the following operation, such as click, set_text, before operating, it will try locate the element to verify whether the element exist

**Example:**
***
```python
    from clicknium import clicknium as cc, locator

    browser = cc.chrome.open("https://bing.com")

    # find elements
    elements = browser.find_elements(locator.chrome.bing.search_sb_form_q)

    for ele in elements:
        ele.highlight()
```