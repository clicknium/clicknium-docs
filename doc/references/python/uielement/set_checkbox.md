# set_checkbox
***def set_checkbox(
        self,
        check_type: Literal["check", "uncheck", "toggle"] = CheckType.Check,
        timeout: int = 30
    ) -> None***  

Set check state for a checkbox control.

**Parameters:**  
    &emsp;**check_type**: str | CheckType   
        &emsp;&emsp; The check action types: "check", "uncheck" or "toggle".  
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation, the unit is second, and the default value is 30 seconds.

**Returns:**  
    &emsp;None