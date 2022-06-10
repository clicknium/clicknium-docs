# clear_text
***def clear_text(
        self,
        clear_method: Union[Literal["controlclearvalue", "sendhotkey"], ClearMethod],
        clear_hotkey: Union[Literal["{CTRL}{A}{DELETE}", "{END}{SHIFT}{HOME}{DELETE}", "{HOME}{SHIFT}{END}{DELETE}"], ClearHotKey] = ClearHotKey.CtrlA_Delete,
        preaction: Literal["setfocus", "click"] = PreAction.SetFocus,
        timeout: int = 30
    ) -> None***  

Clear the element's text.

**Parameters:**  
     &emsp;**clear_method**: ClearMethod  
        &emsp;&emsp; the method to clear text for the target element  
        &emsp;&emsp; `set_property`: clear the target element's text by setting its property.    
        &emsp;&emsp; `send_hotkey`: clear text by sending hotkey to the target element. "clear_hotkey" and "preaction" parameters also need to be specified accordingly.  
    &emsp;**clear_hotkey**: ClearHotKey  
        &emsp;&emsp; clear hotkey, default is `{CTRL}{A}{DELETE}`  
        &emsp;&emsp; `{CTRL}{A}{DELETE}`: send the combined hotkey "{CTRL}{A}" first, then send hotkey "{DELETE}"  
        &emsp;&emsp; `{END}{SHIFT}{HOME}{DELETE}`: send the hotkey "{END}" first, then send combined hotkey "{SHIFT}{HOME}, then send hotkey "{DELETE}"  
        &emsp;&emsp; `{HOME}{SHIFT}{END}{DELETE}`: send the hotkey "{HOME}" first, then send combined hotkey "{SHIFT}{END}, then send hotkey "{DELETE}"  
    &emsp;**preaction**:  
        &emsp;&emsp; pre action, action should be taken on the target element before clear text  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, The unit is second. Default is 30 seconds.  

**Returns:**  
    &emsp;None

**Example:**
***
- Desktop file save as dialog   
![sample1](../../../img/clear_text_sample1.png)  
For the file saveas dialog, use clear_text to clear the existing content in filename input box as the control supports ValueAction, "controlclearvalue" method can be used.


```python
    from clicknium import clicknium as cc, locator, ui  
    ui(locator.chrome.edit_1001).clear_text(clear_method="controlclearvalue")
```

- Wechat message input box  
![sample1](../../../img/clear_text_sample2.png)  
The UI element does not support "controlclearvalue". If there is a need to clear text, use the following way.  

```python
    from clicknium import clicknium as cc, locator, ui  
    ui(locator.wechat.edit1).clear_text(clear_method="sendhotkey", clear_hotkey="{CTRL}{A}{DELETE}", preaction="click")

```

- Web input
```python
driver = cc.chrome.open("https://getbootstrap.com/docs/5.1/forms/input-group/")
driver.find_element(locator.chrome.getbootstrap.text).set_text("hello")
driver.find_element(locator.chrome.getbootstrap.text).clear_text(clear_method=ClearMethod.ControlClearValue)

```