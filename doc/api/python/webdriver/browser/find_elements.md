# find_elements
***def find_elements(
        self,
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        timeout: int = 30
    ) -> List[UiElement]***  

Find elements in the given locator.  

> **Remarks:**  
Use the following method, `clicknium.chrome.open("https://bing.com").find_elements()`, which is different with the method`clicknium.find_elements()` [clicknium.find_elements](./doc/api/python/find_elements.md) when locating the UI elements.
>- `clicknium.find_elements()` is for  UiElements of both web and desktop, and does not specify a scope to locate the elements.
>- `clicknium.chrome.open("https://bing.com").find_elements()` will locate elements in the specified browser.

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the name of one locator in locator store, eg: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, and locator name is search_sb_form_q  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, set to initialize parameters in locator, eg: var_dict = { "row": 1,  "column": 1}, more about variables, please refer to [parametric locator](./doc/automation/parametric_locator.md)  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, Unit is second, and default value is 30 seconds.

**Returns:**  
    &emsp;[UiElement](./doc/api/python/uielement/uielement.md) object, ou can operate as the following with the UiElement, such as click, set_text.It will locate the element to verify whether the element exists before operating.

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