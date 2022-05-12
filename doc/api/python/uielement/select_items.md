# select_items
***def select_items(
        self,
        items: list,
        clear_selected: bool = True,
        timeout: int = 30
    )***  

select multiple option for the target  

**Parameters:**  
    &emsp;**items [Required]**: list  
        &emsp;&emsp; options of the dropdown control, the control should support multiple selection  
    &emsp;**clear_selected**: bool  
        &emsp;&emsp; whether need deselect the already selected options of target control, default is true    
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation. The unit of parameter is seconds. Default is set to 30 seconds.   

**Returns:**  
    &emsp;None

# TODO 
prepare the example
**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui

```