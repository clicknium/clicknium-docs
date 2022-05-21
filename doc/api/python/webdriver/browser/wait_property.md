# wait_property
***def wait_property(
        self,
        locator: Union[_Locator, str],
        name: str,
        value: str,
        locator_variables: dict = {},
        wait_timeout: int = 30
    ) -> bool***  

In current opened browser, wait for the element appear and the value of specified property is same as the expected value. 

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the name of one locator in locator store, ex: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, locator name is search_sb_form_q  
    &emsp;**name[Required]**: str  
        &emsp;&emsp; property name, different ui elements may support different property list, for general property list, please refer to [property list](./doc/automation/property.md)  
    &emsp;**value[Required]**: str  
        &emsp;&emsp; expected property value  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, is set to initialize parameters in locator, ex: var_dict = { "row": 1,  "column": 1}, more about variable, please refer to [parametric locator](./doc/automation/parametric_locator.md)  
    &emsp;**timeout**: int  
        &emsp;&emsp; wait timeout for the operation, unit is second, default value is 30 seconds 

**Returns:**  
    &emsp;bool, return True if ui element exist and the property value equals expected value, or return False

**Remarks**  
It should be used like `clicknium.chrome.open("https://bing.com").wait_property()`, it is different with `clicknium.wait_property()` [clicknium.wait_property](./doc/api/python/wait_property.md) when locating the ui element.
- `clicknium.wait_property()` is for both web and desktop's uielement, and does not specified a scope to locate the element
- `clicknium.chrome.open("https://bing.com").wait_property()` will locate element in the specified browser

**Example:**
***
```python
from clicknium import clicknium as cc, locator

browser = cc.chrome.open("https://bing.com")

# wait for the web propery with expected value
browser.wait_property(locator.chrome.bing.search_sb_form_q)

# parametric locator, wait for the element is enabled, for example the element is blocked by one popup dialog
variables = {"name":"test"}
browser.wait_property(locator.chrome.bing.search_sb_form_q, variables)

```