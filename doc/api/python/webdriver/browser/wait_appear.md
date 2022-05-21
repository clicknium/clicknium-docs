# wait_appear
***def wait_appear(
        self,
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        wait_timeout: int = 30
    ) -> UiElement***  

In current opened browser, wait for the element appear.

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the name of one locator in locator store, ex: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, locator name is search_sb_form_q  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; The locator variables, is set to initialize parameters in locator, ex: var_dict = { "row": 1,  "column": 1}, more about variable, please refer to [parametric locator](./doc/automation/parametric_locator.md)  
    &emsp;**timeout**: int  
        &emsp;&emsp; wait timeout for the operation, unit is second, default value is 30 seconds 

**Returns:**  
    &emsp;[UiElement](./doc/api/python/uielement/uielement.md) object, or None if the element is not appear

**Remark**  
It should be used like `clicknium.chrome.open("https://bing.com").wait_appear()`, it is different with `clicknium.wait_appear()` [clicknium.wait_appear](./doc/api/python/wait_appear.md) when locating the ui element.
- `clicknium.wait_appear()` is for both web and desktop's uielement, and does not specified a scope to locate the element
- `clicknium.chrome.open("https://bing.com").wait_appear()` will locate element in the specified browser

**Example:**
***
```python
from clicknium import clicknium as cc, locator

browser = cc.chrome.open("https://bing.com")

# wait element appear
element = browser.wait_appear(locator.chrome.bing.search_sb_form_q)

# parametric locator
variables = {"name":"test"}
element = browser.wait_appear(locator.chrome.bing.search_sb_form_q, variables)

```