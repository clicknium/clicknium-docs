# set_text
***def set_text(
        self,
        text: str,
        input_method: Union[Literal["default", "set-text", "sendkey-after-click", "sendkey-after-focus"], InputMethod]= InputMethod.SetText,
        timeout: int = 30
    ) -> None***  

Set text for the target element.

**Parameters:**  
    &emsp;**text[Requried]**: str  
        &emsp;&emsp; text string, set to be input  
    &emsp;**input_method**: str | InputMethod  
        &emsp;&emsp; the input method for the set text opeartion  
        &emsp;&emsp; `set-text`: invoke operations on target elements, if it is a Web element, the action will be implemented by javascript. But actions may not be supported if it is a Window element.    
        &emsp;&emsp; `sendkey-after-click`: click(mouse emulator) the target element first and then input text through keyboard simulate   
        &emsp;&emsp; `sendkey-after-focus`: set focus on the target element first and then input text through keyboard simulate  
        &emsp;&emsp; `default`: for web element, use `control-invocation`; for desktop element, use `sendkey-after-click`  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds.

**Returns:**  
    &emsp;None

**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui

    ui(locator.chrome.bing.search_sb_form_q).set_text("clicknium")
```