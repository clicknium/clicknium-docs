# get_text
***def get_text(self, timeout: int = 30) -> str***  

Get text of the target element.

**Parameters:**    
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;str

**Examples:**
***
```python
from clicknium import clicknium as cc, locator, ui
    
text = ui(locator.chrome.bing.search_sb_form_q).get_text()
```

- For edit control of windows application, it returns value of the edit control.
```python
from clicknium import clicknium as cc, locator, ui
    
# return value of the edit document
text = ui(locator.notepad.document).get_text()
```

- For control like button, menuitem of windows application, it returns name of the control.
```python
from clicknium import clicknium as cc, locator, ui
    
# return name of the menuitem
text = ui(locator.notepad.menuitem_format).get_text()
# text is 'format'
```

- For web element, it returns innerText.
```python
from clicknium import clicknium as cc, locator
tab = cc.chrome.open("https://contoso.com")
# return inner text of div
text = tab.find_element(locator.chrome.form.divItem).get_text()
```