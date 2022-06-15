# wait_disappear
***def wait_disappear(
        self,
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        wait_timeout: int = 30
    ) -> bool***  

Wait for the element disappear in current open browser

>**Remarks:**  
It should be used like `clicknium.chrome.open("https://bing.com").wait_disappear()`, it is different with `clicknium.wait_disappear()` [clicknium.wait_disappear](./doc/api/python/wait_disappear.md) when locating the ui element.
>- `clicknium.wait_disappear()` is for both web and desktop's uielement, and does not specified a scope to locate the element
>- `clicknium.chrome.open("https://bing.com").wait_disappear()` will locate element in the specified browser

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the name of one locator in locator store, ex: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, locator name is search_sb_form_q  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, is set to initialize parameters in locator, ex: var_dict = { "row": 1,  "column": 1}, more about variable, please refer to [parametric locator](./doc/automation/parametric_locator.md)  
    &emsp;**timeout**: int  
        &emsp;&emsp; wait timeout for the operation, the unit is second, default value is 30 seconds 

**Returns:**  
    &emsp;bool, return True if the element is disappear in given time or return False

**Example:**
***
```python
from clicknium import clicknium as cc, locator

browser = cc.chrome.open("https://bing.com")

# wait element disappear
browser.wait_disappear(locator.chrome.bing.search_sb_form_q)

# parametric locator
variables = {"name":"test"}
browser.wait_disappear(locator.chrome.bing.search_sb_form_q, variables)

```