# clear_text
***def clear_text(
        self,
        clear_method: Union[Literal["set-text", "send-hotkey"], ClearMethod],
        clear_hotkey: Union[Literal["CAD", "ESHD", "HSED"], ClearHotKey] = ClearHotKey.CtrlA_Delete,
        preaction: Literal["setfocus", "click"] = PreAction.SetFocus,
        timeout: int = 30
    ) -> None***  

Clear text of the target element.

**Parameters:**  
     &emsp;**clear_method**: ClearMethod  
        &emsp;&emsp; The method to clear text for the target element  
        &emsp;&emsp; `set-text`: clear the target element's text by setting its property.  
        &emsp;&emsp; `send-hotkey`: clear text by sending hotkey to the target element. "clear_hotkey" and "preaction" parameters also need to be specified accordingly.   
    &emsp;**clear_hotkey**: ClearHotKey  
        &emsp;&emsp; If clear_method is set to "send-hotkey", then specify hotkey with this parameter, default is `CAD`.  
        &emsp;&emsp; `CAD` means`{CTRL}{A}-{DELETE}`: send the combined keys "{CTRL}{A}" first, then send "{DELETE}".  
        &emsp;&emsp; `ESHD` means `{END}-{SHIFT}{HOME}-{DELETE}`: send "{END}" first, and send combined keys "{SHIFT}{HOME}, then send key "{DELETE}".  
        &emsp;&emsp; `HSED` means `{HOME}-{SHIFT}{END}-{DELETE}`: send "{HOME}" first, and send combined keys "{SHIFT}{END}, then send "{DELETE}".  
    &emsp;**preaction**: PreAction  
        &emsp;&emsp; If clear_method is set to "send-hotkey", specify this parameter for the action to be taken before sending hotkey to clear text.   
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds.  

**Returns:**  
    &emsp;None

**Example:**
***
- Desktop file "Save As" dialog   
![sample1](../../../img/clear_text_sample1.png)  
For the file "Save As" dialog, use clear_text to clear the existing content in "File name" input box, the clear_method can be set to "set-text" in this case.


```python
from clicknium import clicknium as cc, locator, ui  

ui(locator.chrome.edit_1001).clear_text(clear_method="set-text")
```

- Wechat message input box  
![sample1](../../../img/clear_text_sample2.png)  
This type of UI element does not support "set-text" to clear text, then use the following way.  

```python
from clicknium import clicknium as cc, locator, ui  

ui(locator.wechat.edit1).clear_text(clear_method="send-hotkey", clear_hotkey="CAD", preaction="click")

```

- Web input textbox

```python
chrome_tab = cc.chrome.open("https://contoso.com/")
chrome_tab.find_element(locator.chrome.contoso.text).set_text("hello")
chrome_tab.find_element(locator.chrome.contoso.text).clear_text(clear_method=ClearMethod.SetText)
```