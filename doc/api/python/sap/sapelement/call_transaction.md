# call_transaction

***def call_transaction(
        self,
        transaction_code: str,
        timeout: int = 30
    ) -> None***  

Call sap transaction.

**Parameters:**  
    &emsp;**transaction_code[Required]**: str  
        &emsp;&emsp; transaction code string  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds. 

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

    # find sap element
    sap_ele = sap_driver.find_element(locator.sap.control)

    # call transaction code
    sap_ele.call_transaction( "code")
```