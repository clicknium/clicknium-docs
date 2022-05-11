# get_position
***def get_property(
        self,
        name: str,
        timeout: int = 30
    ) ***  

Get property value of the element  

**Parameters:**   
    &emsp;**name [Required]**: str  
        &emsp;&emsp; property name, different ui elements may support different property list, for general property list, please refer to [property list](/doc/property.md)  
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation. The unit of parameter is seconds. Default is set to 30 seconds.  

**Returns:**  
    &emsp;str

**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui
    
    tag = ui(locator.chrome.bing.search_sb_form_q).get_property("tag")
```