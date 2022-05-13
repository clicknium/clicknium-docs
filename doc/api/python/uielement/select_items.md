# select_items
***def select_items(
        self,
        items: list,
        clear_selected: bool = True,
        timeout: int = 30
    ) -> None***  

Select multiple option for the target.  

**Parameters:**  
    &emsp;**items [Required]**: list  
        &emsp;&emsp; options of the dropdown control, the control should support multiple selection  
    &emsp;**clear_selected**: bool  
        &emsp;&emsp; whether need deselect the already selected options of target control, default is True    
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation. The unit of parameter is seconds. Default is set to 30 seconds   

**Returns:**  
    &emsp;None

**Example:**
***
- select items on web
  
![sample](../../../img/select_items_sample1.png)  
```python
from clicknium import clicknium as cc, locator, ui

driver = cc.chrome.open("https://getbootstrap.com/docs/5.1/forms/input-group/")
driver.find_element(locator.chrome.getbootstrap.multiselect).select_item({'One', 'Three'})

```

![sample](../../../img/select_items_sample2.png)  