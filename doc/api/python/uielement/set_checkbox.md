# set_checkbox
***def set_checkbox(
        self,
        check_type: Literal["check", "uncheck", "toggle"] = CheckType.Check,
        timeout: int = 30
    ) -> None***  

Do check operation on target element.

**Parameters:**  
    &emsp;**check_type**: str | CheckType   
        &emsp;&emsp; set option for check operation, "check", "uncheck" or "toggle"  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation. The unit of parameter is seconds. Default is set to 30 seconds   

**Returns:**  
    &emsp;None

# TODO 
prepare the example
**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui

```