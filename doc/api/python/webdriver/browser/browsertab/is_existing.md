# is_existing
***def is_existing(
        self,
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        timeout: int = 30
    ) -> bool***  

 Check whether the UI element exists in currently open browser.

>**Remarks:**  
Use the following method, `clicknium.chrome.open("https://bing.com").is_existing()`, it is different with the method `clicknium.is_existing()` [clicknium.is_existing](./doc/api/python/is_existing.md) when locating the UI element.
>- `clicknium.is_existing()` is for  UiElement of both web and window, and does not specify a scope to locate the element.
>- `clicknium.chrome.open("https://bing.com").is_existing()` will locate element in the specified browser.


**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the name of one locator in locator store, eg: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, and locator name is search_sb_form_q  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, set to initialize parameters in locator, eg: var_dict = { "row": 1,  "column": 1}, more about variables, please refer to [Parametric Locator](./doc/automation/parametric_locator.md)  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;return True if UI element exists, otherwise return False

**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui

    chrome_tab = cc.chrome.open("https://bing.com")

    # check element if exist
    chrome_tab.is_existing(locator.chrome.bing.search_sb_form_q)

    # parametric locator
    variables = {"name":"test"}
    chrome_tab.is_existing(locator.chrome.bing.search_sb_form_q, variables)
```