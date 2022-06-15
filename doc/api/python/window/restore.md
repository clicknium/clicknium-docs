# restore

***def restore(
        self, 
        locator: Union[_Locator, str],
        locator_variables: dict = {}, 
        timeout: int = 30
    ) -> None***  

Restore the window

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator  
        &emsp;&emsp; locator string, the name of one locator in locator store, eg: 'locator.notepad.window_notitle_notepad', locator store is notepad, and locator name is window_notitle_notepad  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, set to initialize parameters in locator, eg: var_dict = { "row": 1,  "column": 1}, more about variables, please refer to [parametric locator](./doc/automation/parametric_locator.md)  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds.

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