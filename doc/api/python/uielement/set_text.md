# set_text
***def set_text(
        self,
        text: str,
        by: Union[Literal["default", "set-text", "sendkey-after-click", "sendkey-after-focus"], InputTextBy]= InputTextBy.SetText,
        append: bool = False,
        timeout: int = 30
    ) -> None***  

Set text for the target element, it can be used to input text to a system.  

**Parameters:**  
    &emsp;**text[Requried]**: str  
        &emsp;&emsp; text to be input to target element.  
    &emsp;**by**: str | InputTextBy   
        &emsp;&emsp; the method to perform the text input operation.  
        &emsp;&emsp; `set-text`: call system method to set text to the target element. Some window application elements may not be supported.  
        &emsp;&emsp; `sendkey-after-click`: simulate mouse click to activate the element, then send keys by simulating keyboard.  
        &emsp;&emsp; `sendkey-after-focus`: set the target element to focused state, then sending keys by simulating keyboard.  
        &emsp;&emsp; `default`: using different methods per target element type. `set-text` for web element and `sendkey-after-click` for desktop element.  
    &emsp;**append**: bool  
        &emsp;&emsp; whether to append text, default is False.   
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds.

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc, locator, ui

ui(locator.chrome.bing.search_sb_form_q).set_text("clicknium", append = True)
```