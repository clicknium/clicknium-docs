# clear_text
***def clear_text(
        self,
        clear_method: Union[Literal["set-text", "send-hotkey"], ClearMethod],
        clear_hotkey: Union[Literal["CAD", "ESHD", "HSED"], ClearHotKey] = ClearHotKey.CtrlA_Delete,
        preaction: Literal["setfocus", "click"] = PreAction.SetFocus,
        timeout: int = 30
    ) -> None***  

Clear text of the element.

**Parameters:**  
     &emsp;**clear_method**: ClearMethod  
        &emsp;&emsp; the method to clear text for the target element  
        &emsp;&emsp; `set-text`: clear the target element's text by setting its property.    
        &emsp;&emsp; `send-hotkey`: clear text by sending hotkey to the target element. "clear_hotkey" and "preaction" parameters also need to be specified accordingly.  
    &emsp;**clear_hotkey**: ClearHotKey  
        &emsp;&emsp; if clear_method is set to "send_hotkey", then specify hotkey with this parameter, default is `{CTRL}{A}{DELETE}`  
        &emsp;&emsp; `CAD` means`{CTRL}{A}-{DELETE}`: send the combined hotkey "{CTRL}{A}" first, then send hotkey "{DELETE}"  
        &emsp;&emsp; `ESHD` means `{END}-{SHIFT}{HOME}-{DELETE}`: send the hotkey "{END}" first, then send combined hotkey "{SHIFT}{HOME}, then send hotkey "{DELETE}"  
        &emsp;&emsp; `HSED` means `{HOME}-{SHIFT}{END}-{DELETE}`: send the hotkey "{HOME}" first, then send combined hotkey "{SHIFT}{END}, then send hotkey "{DELETE}"  
    &emsp;**preaction**: PreAction  
        &emsp;&emsp; pre action, action should be taken on the target element before clear text  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds.  

**Returns:**  
    &emsp;None

**Example:**
***
- Desktop file "Save As" dialog   
![sample1](../../../img/clear_text_sample1.png)  
For the file "Save As" dialog, use clear_text to clear the existing content in "File name" input box, the clear_method can be set to "set_property" in this case.


```python
    from clicknium import clicknium as cc, locator, ui  
    ui(locator.chrome.edit_1001).clear_text(clear_method="controlclearvalue")
```

- Wechat message input box  
![sample1](../../../img/clear_text_sample2.png)  
The UI element does not support "set_property". If there is a need to clear text, use the following way.  

```python
    from clicknium import clicknium as cc, locator, ui  
    ui(locator.wechat.edit1).clear_text(clear_method="sendhotkey", clear_hotkey="{CTRL}{A}{DELETE}", preaction="click")

```

- Web input

```python
chrome_tab = cc.chrome.open("https://getbootstrap.com/docs/5.1/forms/input-group/")
chrome_tab.find_element(locator.chrome.getbootstrap.text).set_text("hello")
chrome_tab.find_element(locator.chrome.getbootstrap.text).clear_text(clear_method=ClearMethod.ControlClearValue)
```