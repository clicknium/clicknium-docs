# send_hotkey
***def send_hotkey(
        self,
        hotkey: str,
        preaction: Literal["setfocus", "click"] = PreAction.SetFocus,
        timeout: int = 30
    ) -> None***  

Send hot key based on target element  

**Parameters:**  
    &emsp;**hotkey [Required]**: str   
        &emsp;&emsp; hotkey string, one key or combined keys, Each key is represented by one or more characters. To specify a single keyboard character, use the character itself. For example, representing the letter A, pass in the string "A" to the method. Representing more than one character, append each additional character to the one preceding it. Representing the letters A, B, and C, specify the parameter as "ABC". For special keys, please refer to [hotkeys](https://docs.microsoft.com/en-au/dotnet/api/system.windows.forms.sendkeys?view=windowsdesktop-6.0#remarks)  
    &emsp;**preaction**: PreAction  
        &emsp;&emsp; Which action should be taken on the target element  before sending hotkey.  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds.

**Returns:**  
    &emsp;None

**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui

    #send Ctrl+A  
    ui(locator.chrome.bing.search_sb_form_q).send_hotkey('{CTRL}A')  
    ui(locator.chrome.bing.search_sb_form_q).send_hotkey('^A')
    # same as  
    cc.find_element(locator.chrome.bing.search_sb_form_q).send_hotkey('{CTRL}A')

    #send Shift+End
    ui(locator.chrome.bing.search_sb_form_q).send_hotkey('+{END}')
```