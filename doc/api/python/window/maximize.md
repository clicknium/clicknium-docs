# maximize

***def maximize(
        self, 
        locator: Union[_Locator, str],
        locator_variables: dict = {}, 
        timeout: int = 30
    ) -> None***  

Maximize the window.

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator  
        &emsp;&emsp; locator string, the name of one locator in locator store, ex: 'locator.notepad.window_notitle_notepad', locator store is notepad, locator name is window_notitle_notepad  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, is set to initialize parameters in locator, ex: var_dict = { "row": 1,  "column": 1}, more about variable, please refer to [parametric locator](./doc/automation/parametric_locator.md)  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, unit is second, default value is 30 seconds 

**Returns:**  
    &emsp;None

**Example:**
***
```python
    from clicknium import clicknium as cc

    # get window driver
    window_driver = cc.window

    # maximize window
    window_driver.maximize("locator.notepad.window_notitle_notepad")

    # parametric locator
    variables = {"name":"test"}
    window_driver.maximize("locator.notepad.window_notitle_notepad", variables)
```