# clicknium.send_hotkey
***def send_hotkey(hotkey: str) -> None***  

Send hot key.  

>**Remarks:**  
This method is global send hotkey.
If you want to send hotkey on one ui element, there are two choice:
>- you should invoke [send_hotkey](/doc/api/python/uielement/send_hotkey.md) on ui element
>- before invoke this method, call [click](/doc/api/python/uielement/click.md) or [set_focus](/doc/api/python/uielement/set_focus.md) on the ui element first

**Parameters:**  
    &emsp;**hotkey[Required]**: str   
        &emsp;&emsp; hotkey string, can be one key or combined keys, each key is represented by one or more characters. To specify a single keyboard character, use the character itself. For example, to represent the letter A, pass in the string "A" to the method. To represent more than one character, append each additional character to the one preceding it. To represent the letters A, B, and C, specify the parameter as "ABC". For special keys, please refer to [hotkeys](https://docs.microsoft.com/en-au/dotnet/api/system.windows.forms.sendkeys?view=windowsdesktop-6.0#remarks)

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