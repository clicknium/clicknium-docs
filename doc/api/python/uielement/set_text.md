# set_text
***def set_text(
        self,
        text: str,
        input_method: Union[Literal["default", "controlsetvalue", "keyboardsimulatewithclick", "keyboardsimulatewithsetfocus"], InputMethod]= InputMethod.ControlSetValue,
        timeout: int = 30
    ) -> None***  

Set text for the target element.

**Parameters:**  
    &emsp;**text [required]**: str   
        &emsp;&emsp; text string, expected to be input  
    &emsp;**input_method**: str | InputMethod   
        &emsp;&emsp; input method is set to which method to input text.  
        &emsp;&emsp; `default` vaule is default, it will input the text automatically.   
        &emsp;&emsp; `controlsetvalue`, it uses control.   
        &emsp;&emsp; `keyboardsimulatewithclick`, it will click first then use keyboard simulate to input.  
        &emsp;&emsp; `keyboardsimulatewithsetfocus`, it will set focus first then use keyboard simulate to input.   
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation. The unit of parameter is seconds. Default is set to 30 seconds

**Returns:**  
    &emsp;None

# TODO 
prepare the example
**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui

```