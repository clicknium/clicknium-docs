# set_text
***def set_text(
        self,
        text: str,
        input_method: Union[Literal["default", "set-text", "keyboard-simulate-click", "keyboard-simulate-setfocus"], InputMethod]= InputMethod.ControlSetValue,
        timeout: int = 30
    ) -> None***  

Set text for the target element.

**Parameters:**  
    &emsp;**text[Requried]**: str  
        &emsp;&emsp; text string, set to be input  
    &emsp;**input_method**: str | InputMethod  
        &emsp;&emsp; the input method for the set text opeartion  
        &emsp;&emsp; `set-text`: invoke the action on the target element, for web element, perform through javascript; for windows application element, it should support the action, or it will be failed  
        &emsp;&emsp; `keyboard-simulate-click`: click(mouse emulator) the target element first and then input text through keyboard simulate   
        &emsp;&emsp; `keyboard-simulate-setfocus`: set focus on the target element first and then input text through keyboard simulate  
        &emsp;&emsp; `default`: for web element, use `control-invocation`; for desktop element, use `keyboard-simulate-click`  
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