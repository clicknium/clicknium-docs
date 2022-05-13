# get_text
***def get_text(self, timeout: int = 30) -> str***  

Get text of the element.

**Parameters:**    
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation. The unit of parameter is seconds. Default is set to 30 seconds  

**Returns:**  
    &emsp;str

**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui
    
    text = ui(locator.chrome.bing.search_sb_form_q).get_text()
```

- edit control on windows application: will return value
```python
    from clicknium import clicknium as cc, locator, ui
    
    # return value of the edit document
    text = ui(locator.notepad.document).get_text()
```

- button, menuitem etc on windows application: will return name
```python
    from clicknium import clicknium as cc, locator, ui
    
    # return value of the edit document
    text = ui(locator.notepad.menuitem_format).get_text()

    #text is 'format'
```

- element on web page: will return innerText