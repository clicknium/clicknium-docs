# is_exist
***def is_exist(
        self,
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        timeout: int = 30
    ) -> bool***  

In current opened browser, check whether the ui element exist or not.  

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the name of one locator in locator store, ex: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, locator name is search_sb_form_q  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; The locator variables, is set to initialize parameters in locator, ex: var_dict = { "row": 1,  "column": 1}, more about variable, please refer to [parametric locator](./doc/parametric_locator.md)  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, unit is second, default value is 30 seconds 

**Returns:**  
    &emsp;return True if ui element exist, or return False

**Remark**  
It should be used like `clicknium.chrome.open("https://bing.com").is_exist()`, it is different with `clicknium.is_exist()` [clicknium.is_exist](./doc/api/python/is_exist.md) when locating the ui element.
- `clicknium.is_exist()` is for both web and desktop's uielement, and does not specified a scope to locate the element
- `clicknium.chrome.open("https://bing.com").is_exist()` will locate element in the specified browser

**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui

    browser = cc.chrome.open("https://bing.com")

    # check element if exist
    browser.is_exist(locator.chrome.bing.search_sb_form_q)

    # parametric locator
    variables = {"name":"test"}
    browser.is_exist(locator.chrome.bing.search_sb_form_q, variables)
```