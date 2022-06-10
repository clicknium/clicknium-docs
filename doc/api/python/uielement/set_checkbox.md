# set_checkbox
***def set_checkbox(
        self,
        check_type: Literal["check", "uncheck", "toggle"] = CheckType.Check,
        timeout: int = 30
    ) -> None***  

Check operation on target element

**Parameters:**  
    &emsp;**check_type**: str | CheckType   
        &emsp;&emsp; set options for checking operation, "check", "uncheck" or "toggle"  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation. The unit of parameter is second. Default set is 30 seconds.   

**Returns:**  
    &emsp;None