# call_transaction

***def call_transaction(
        self,
        locator: Union[_Locator, str],
        transaction_code: str,
        locator_variables: dict = {},
        timeout: int = 30
    ) -> None***  

Call sap transaction.

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator  
        &emsp;&emsp; locator string, the name of one locator in locator store, ex: 'locator.sap.transaction_input', locator store is sap, locator name is transaction_input  
    &emsp;**transaction_code[Required]**: str  
        &emsp;&emsp; transaction code string  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, is set to initialize parameters in locator, ex: var_dict = { "row": 1,  "column": 1}, more about variable, please refer to [parametric locator](./doc/parametric_locator.md)  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, unit is second, default value is 30 seconds 

**Returns:**  
    &emsp;None

**Example:**
***
```python
    from clicknium import clicknium as cc, locator

    # get sap driver
    sap_driver = cc.sap

    # login sap application
    sap_driver.login("path", "connection", "client", "username", "password")

    # call transaction code
    sap_driver.call_transaction(locator.sap.transaction_input, "code")
```