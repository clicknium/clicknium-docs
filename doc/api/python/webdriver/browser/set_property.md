# set property

***def set_property(
        self,
        locator: Union[_Locator, str],
        name: str,
        value: str,
        locator_variables: dict = {},
        timeout: int = 30
    ) -> None***  

Wait for the element to appear and set its specified property with specified value in current open browser

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the name of one locator in locator store, eg: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, and locator name is search_sb_form_q  
    &emsp;**name[Required]**: str  
        &emsp;&emsp; property name, Different UI elements may support different property lists. For general property list, please refer to [property list](./doc/automation/property.md)  
    &emsp;**value[Required]**: str  
        &emsp;&emsp; property value  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables,  set to initialize parameters in locator, eG: var_dict = { "row": 1,  "column": 1}, more about variables, please refer to [parametric locator](./doc/automation/parametric_locator.md)  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc, locator

chrome_tab = cc.chrome.open("https://bing.com")

# set the web propery with specified value
chrome_tab.set_property(locator.chrome.bing.search_sb_form_q, "tag", "search_tag")

# parametric locator
variables = {"name":"test"}
chrome_tab.set_property(locator.chrome.bing.search_sb_form_q, "tag", "search_tag", variables)

```