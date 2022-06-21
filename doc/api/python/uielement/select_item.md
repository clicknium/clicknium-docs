# select_item
***def select_item(
        self,
        item: str,
        timeout: int = 30
    ) -> None***  

Select one option for the target element.

**Parameters:**  
    &emsp;**item [Required]**: str   
        &emsp;&emsp; option of the dropdown control, The control suppors selection, such as selecting element in web, or combobox in desktop appication.  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds.   

**Returns:**  
    &emsp;None

**Example:**
***
- select item on web input (type is select)
```python
from clicknium import clicknium as cc, locator, ui

chrome_tab = cc.chrome.open("https://getbootstrap.com/docs/5.1/forms/input-group/")
chrome_tab.find_element(locator.chrome.getbootstrap.select).select_item('One')

```

![sample](../../../img/select_item_sample1.png)  
-  select item on windows file saved as dialog  
```python
from clicknium import clicknium as cc, locator, ui

ui(locator.notepad.combobox_filetype).select_item('All Files  (*.*)')

```
![sample](../../../img/select_item_sample2.png)  