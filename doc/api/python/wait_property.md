# wait_property
***def wait_property(
        locator: Union[_Locator, str],
        name: str, 
        value: str, 
        locator_variables: dict = {},
        wait_timeout: int = 30
    ) -> bool***  

Wait for the element appear and the value of specified property is same as the expected value. 

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the name of one locator in locator store, ex: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, locator name is search_sb_form_q  
    &emsp;**name[Required]**: str  
        &emsp;&emsp; property name, different ui elements may support different property list, for general property list, please refer to [property list](./doc/property.md)  
    &emsp;**value[Required]**: str  
        &emsp;&emsp; expected property value  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, is set to initialize parameters in locator, ex: var_dict = { "row": 1,  "column": 1}, more about variable, please refer to [parametric locator](./doc/parametric_locator.md)  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, unit is second, default value is 30 seconds 

**Returns:**  
    &emsp;bool, return True if ui element exist and the property value equals expected value, or return False


**Example:**
***
```python
from clicknium import clicknium as cc, locator

#wait for the web page loadding ready
cc.wait_property(locator.chrome.bing.search_sb_form_q, 'readystate', '1')

#parametric locator, wait for the element is enabled, for example the element is blocked by one popup dialog
variables = {"name":"test"}
cc.wait_property(locator.notepad.notepad.document_151,'IsEnabled', 'True', variables)
```