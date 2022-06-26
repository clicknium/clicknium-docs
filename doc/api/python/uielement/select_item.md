# select_item
***def select_item(
        self,
        item: str,
        timeout: int = 30
    ) -> None***  

Select one option for the target element when it is a dropdown type control.

**Parameters:**  
    &emsp;**item [Required]**: str   
        &emsp;&emsp; target option of the dropdown control.
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds.   

**Returns:**  
    &emsp;None

**Example:**
***
- Select item on web (type is select)
![sampel1](../../../img/select-item-sample1.png)

```python
from clicknium import clicknium as cc, locator, ui

chrome_tab = cc.chrome.open("https://contoso.com")
chrome_tab.find_element(locator.chrome.page.select).select_item('One')

```
-  Select item on window file "Saved As" dialog  

![sample](../../../img/select_item_sample2.png)  
```python
from clicknium import clicknium as cc, locator, ui

ui(locator.notepad.combobox_filetype).select_item('All Files  (*.*)')

```