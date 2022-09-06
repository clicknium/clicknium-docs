# send_hotkey
***def send_hotkey(
        self,
        hotkey: str,
        preaction: Literal["setfocus", "click"] = PreAction.SetFocus,
        timeout: int = 30
    ) -> None***  

Send hotkey to target element.

**Parameters:**  
    &emsp;**hotkey [Required]**: str   
        &emsp;&emsp; Hotkey string represents one key or combined keys. For example, to represent the letter A, input string "A". To represent the letters A, B, and C, input paremeter "ABC". For special keys, please refer to [hotkeys](https://docs.microsoft.com/en-au/dotnet/api/system.windows.forms.sendkeys?view=windowsdesktop-6.0#remarks).  
    &emsp;**preaction**: PreAction  
        &emsp;&emsp; The action to be taken before sending hotkey.  
        &emsp;&emsp; `setfocus`: default value, setting the target element to focused state before sending hotkey.  
        &emsp;&emsp; `click`: click the target element before sending hotkey.  
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation, the unit is second, and the default value is 30 seconds.  

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc, locator, ui

#send Ctrl+a   
ui(locator.chrome.bing.search_sb_form_q).send_hotkey('^a')

#send Shift+End
ui(locator.chrome.bing.search_sb_form_q).send_hotkey('+{END}')

#send Win+e, first press 'Win', then press 'E' and release, and finally release 'Win'
ui(locator.chrome.bing.search_sb_form_q).send_hotkey('{WIN DOWN}e{WIN UP}')
```