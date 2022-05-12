# select_item
***def select_item(
        self,
        item: str,
        timeout: int = 30
    )***  

select one option for the target

**Parameters:**  
    &emsp;**item [Required]**: str   
        &emsp;&emsp; option of the dropdown control, the control support selection, such as select element in web, or combobox in desktop apllcaiton
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation. The unit of parameter is seconds. Default is set to 30 seconds.   

**Returns:**  
    &emsp;None

**Example:**
***
- select item on web input(type is select)
```python
from clicknium import clicknium as cc, locator, ui

driver = cc.chrome.open("https://getbootstrap.com/docs/5.1/forms/input-group/")
driver.find_element(locator.chrome.getbootstrap.select).select_item('One')

```

![sample](../../../img/select_item_sample1.png)  
-  select item on windows file save as dialog  
```python
from clicknium import clicknium as cc, locator, ui

ui(locator.notepad.combobox_filetype).select_item('All Files  (*.*)')

```
![sample](../../../img/select_item_sample2.png)  