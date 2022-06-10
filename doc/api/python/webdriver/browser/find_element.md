# find_element
***def find_element(
        self,
        locator: Union[_Locator, str],
        locator_variables: dict = {}
    ) -> UiElement***  

 Initialize UI element by the given locator in current open browser

>**Remarks:**  
Use the following method,
 `clicknium.chrome.open("https://bing.com").find_element()`, which is different with the method `clicknium.find_element()` [clicknium.find_element](./doc/api/python/find_element.md) when locating the UI element.
>- `clicknium.find_element()` is for UiElement of both web and desktop, and does not specify a scope to locate the element.
>- `clicknium.chrome.open("https://bing.com").find_element()` will locate the element in the specified browser.

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator    
        &emsp;&emsp; locator string, the name of one locator in locator store, eg: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, and locator name is search_sb_form_q  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, set to initialize parameters in locator, eg: var_dict = { "row": 1,  "column": 1}, more about variables, please refer to [parametric locator](./doc/automation/parametric_locator.md)

**Returns:**  
    &emsp;[UiElement](./doc/api/python/uielement/uielement.md) object, you can operate as the following with the UiElement, such as click, set_text.It will locate the element to verify whether the element exists before operating.

**Example:**
***
```python
    from clicknium import clicknium as cc, locator

    browser = cc.chrome.open("https://bing.com")

    # find element
    element = browser.find_element(locator.chrome.bing.search_sb_form_q)

    # parametric locator
    variables = {"name":"test"}
    element = browser.find_element(locator.chrome.bing.search_sb_form_q, variables)
```