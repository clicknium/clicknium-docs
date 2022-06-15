# wait_property
***def wait_property(
        self,
        locator: Union[_Locator, str],
        name: str,
        value: str,
        locator_variables: dict = {},
        wait_timeout: int = 30
    ) -> bool***  

In current open browser, wait for the element to appear and the value of specified property is the same as expected. 

>**Remarks:**  
Use the following method, `clicknium.chrome.open("https://bing.com").wait_property()`, which is different with the method `clicknium.wait_property()` [clicknium.wait_property](./doc/api/python/wait_property.md) when locating the UI element.
>- `clicknium.wait_property()` is for UiElement of both web and desktop, and does not specify a scope to locate the element.
>- `clicknium.chrome.open("https://bing.com").wait_property()` will locate element in the specified browser.

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the name of one locator in locator store, eg: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, and locator name is search_sb_form_q  
    &emsp;**name[Required]**: str  
        &emsp;&emsp; property name, different UI elements may support different property lists. For general property list, please refer to [property list](./doc/automation/property.md)  
    &emsp;**value[Required]**: str  
        &emsp;&emsp; expected property value  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, set to initialize parameters in locator, eg: var_dict = { "row": 1,  "column": 1}, more about variables, please refer to [parametric locator](./doc/automation/parametric_locator.md)  
    &emsp;**timeout**: int  
        &emsp;&emsp; wait timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;bool, return True if UI element exists and the property value equals expected value, otherwise return False

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