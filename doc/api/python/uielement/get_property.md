# get_property
***def get_property(
        self,
        name: str,
        timeout: int = 30
    ) -> str***  

Get property value of the element.  

**Parameters:**   
    &emsp;**name [Required]**: str  
        &emsp;&emsp; property name, Different UI elements may support different property list. For general property list, please refer to [property list](./doc/automation/property.md)  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds  

**Returns:**  
    &emsp;str

**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui
    
    tag = ui(locator.chrome.bing.search_sb_form_q).get_property("tag")
```