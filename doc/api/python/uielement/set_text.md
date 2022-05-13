# set_text
***def set_text(
        self,
        text: str,
        input_method: Union[Literal["default", "controlsetvalue", "keyboardsimulatewithclick", "keyboardsimulatewithsetfocus"], InputMethod]= InputMethod.ControlSetValue,
        timeout: int = 30
    ) -> None***  

Set text for the target element.

**Parameters:**  
    &emsp;**text[Requried]**: str  
    &emsp;**input_method**: str  
        &emsp;&emsp;the input method for the set text opeartion
        &emsp;&emsp; `controlsetvalue`: invoke the action on the target element, for web element, perform through javascript; for windows application element, it should support the action, or will be failed.
        &emsp;&emsp; `keyboardsimulatewithclick`: click(mouse emulator) the target element first and then input text through keyboard simulate  
        &emsp;&emsp; `keyboardsimulatewithsetfocus`: set focus on the target element first and then input text through keyboard simulate  
        &emsp;&emsp; `default`: for web element, will use `controlinvocation`; for desktop element, will use `keyboardsimulatewithclick`
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation. The unit of parameter is seconds. Default is set to 30 seconds

**Returns:**  
    &emsp;None

**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui

    ui(locator.chrome.bing.search_sb_form_q).set_text("clicknium")
```