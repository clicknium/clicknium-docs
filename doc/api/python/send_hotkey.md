# clicknium.send_hotkey
***def send_hotkey(hotkey: str) -> None***  

Send hotkey to the current cursor's position.

>**Remarks:**  
This method is global send hotkey.
If you want to send hotkey on one UI element, there are two options:
>- You can invoke [send_hotkey](/doc/api/python/uielement/send_hotkey.md) on UI element
>- Before invoking this method, you can call [click](/doc/api/python/uielement/click.md) or [set_focus](/doc/api/python/uielement/set_focus.md) on the UI element.

**Parameters:**  
    &emsp;**hotkey[Required]**: str   
        &emsp;&emsp; hotkey string means one key or combined keys. Each key represents one or more characters. To specify a single keyboard character, use the character itself. For example, to represent the letter A, input string "A". To represent the letters A, B, and C, input paremeter "ABC". For special keys, please refer to [hotkeys](https://docs.microsoft.com/en-au/dotnet/api/system.windows.forms.sendkeys?view=windowsdesktop-6.0#remarks)

**Returns:**  
    &emsp;None

**Example:**
***
```python
    from clicknium import clicknium as cc

    #send Ctrl+A
    cc.send_hotkey('{CTRL}A')
    #or
    cc.send_hotkey('^A')

    #send Shift+End
    cc.send_hotkey('+{END}')
```