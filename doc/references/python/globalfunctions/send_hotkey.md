---
sidebar_position: 7
---
# clicknium.send_hotkey
***def send_hotkey(hotkey: str) -> None***  

Send hotkey to the cursor's current position.

>**Remarks:**  
It is a method that sends hotkey to the system. If you need to send the hotkey to a specific UI element, you need to set the UI element to focused state before calling this method. Or you may use another [send_hotkey](./send_hotkey.md) which is bound to a UI element.

**Parameters:**  
    &emsp;**hotkey[Required]**: str   
        &emsp;&emsp; hotkey string represents one key or combined keys. For example, to represent the letter A, input string "A". To represent the letters A, B, and C, input paremeter "ABC". For special keys, please refer to [hotkeys](https://docs.microsoft.com/en-au/dotnet/api/system.windows.forms.sendkeys?view=windowsdesktop-6.0#remarks).

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc

#send Ctrl+a
cc.send_hotkey('^a')

#send Shift+End
cc.send_hotkey('+{END}')

#send Win+e, first press 'Win', then press 'E' and release, and finally release 'Win'
cc.send_hotkey('{WIN DOWN}e{WIN UP}')
```