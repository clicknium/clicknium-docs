# Find Element
***def find_element(selector_locator, selector_variables = {}, window_mode = WindowMode.Auto)***  

Find element by giving a selector locator.  

**Parameters:**  
    &emsp;**selector_locator[Required]**: str   
        &emsp;&emsp; Selector locator string, ex: 'selectorstore.jd.loginbutton'  
        &emsp;&emsp;Tips:   
        &emsp;&emsp;&emsp;1. selector_locator must start with module selectorstore.  
        &emsp;&emsp;&emsp;2. use "ctrl + f10" to record selector.  
    &emsp;**selector_variables**: dict  
        &emsp;&emsp; The selector variables, is set to replace variables in selector locator string, ex: var_dict = { "row": 1,  "column": 1}  
    &emsp;**window_mode**: WindowMode  
        &emsp;&emsp; Window mode is set to define when operating the element, whether to set the window on topmost.  
        &emsp;&emsp;&emsp;Default value is auto, it means setting the window automatically.  
        &emsp;&emsp;&emsp;TopMost,  it means setting the window on topmost.  
        &emsp;&emsp;&emsp;NoAction,  it means ignoring the window status.  
        &emsp;&emsp;Tips：  
        &emsp;&emsp;&emsp; Import WindowMode module with `from clicknium.common.enums import WindowMode`

**Returns:**  
    &emsp;UiElement class

**Example:**
***
```python
    >>> from clicknium import clicknium as cc, selectorstore
    >>> cc.find_element(selectorstore.chrome.baidu.text_kw)
```