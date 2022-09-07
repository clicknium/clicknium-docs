# restore

***def restore(
        self, 
        locator: Union[_Locator, str],
        locator_variables: dict = {}, 
        timeout: int = 30
    ) -> None***  

Restore the window specified by locator.  

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; Locator string, the visit path of locator for target UI element, eg: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, and locator name is search_sb_form_q. For more details, please refer to [Locator](./../../../concepts/locator.md).   
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; Locator variables, set to initialize parameters in locator, eg: `{ "row": 1,  "column": 1}`, more about variables, please refer to [Parametric Locator](./../../../concepts/locator.md#parametric-locator).  
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation, the unit is second, and the default value is 30 seconds.

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc

# get window driver
window_driver = cc.window

# restore window
window_driver.restore("locator.notepad.window_notitle_notepad")

# parametric locator
variables = {"name":"test"}
window_driver.restore("locator.notepad.window_notitle_notepad", variables)
```