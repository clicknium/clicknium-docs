# set property

***def set_property(
        self,
        locator: Union[_Locator, str],
        name: str,
        value: str,
        locator_variables: dict = {},
        timeout: int = 30
    ) -> None***  

In current opened browser, wait for the element appear and set its specified property with specified value. 

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the name of one locator in locator store, ex: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, locator name is search_sb_form_q  
    &emsp;**name[Required]**: str  
        &emsp;&emsp; property name, different ui elements may support different property list, for general property list, please refer to [property list](/doc/property.md)  
    &emsp;**value[Required]**: str  
        &emsp;&emsp; property value  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; The locator variables, is set to initialize parameters in locator, ex: var_dict = { "row": 1,  "column": 1}, more about variable, please refer to [parametric locator](/doc/parametric_locator.md)  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, unit is second, default value is 30 seconds 

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc, locator

browser = cc.chrome.open("https://bing.com")

# set the web propery with specified value
browser.set_property(locator.chrome.bing.search_sb_form_q, "tag", "search_tag")

# parametric locator
variables = {"name":"test"}
browser.set_property(locator.chrome.bing.search_sb_form_q, "tag", "search_tag", variables)

```