# select_item

***def select_item(
        self,
        locator: Union[_Locator, str],
        item: str,
        locator_variables: dict = {},
        timeout: int = 30
    ) -> None***  

Select sap item.

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator  
        &emsp;&emsp; locator string, the name of one locator in locator store, eg: 'locator.sap.item_q', locator store is sap, locator name is item_q  
    &emsp;**item[Required]**: str  
        &emsp;&emsp; item string, set to be selected   
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, set to initialize parameters in locator, eg: var_dict = { "row": 1,  "column": 1}, more about variable, please refer to [parametric locator](./doc/automation/parametric_locator.md)  
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

    # select item
    sap_driver.select_item(locator.sap.item_q, "item1")
```