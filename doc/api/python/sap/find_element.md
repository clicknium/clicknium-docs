# find_element
***def find_element(
        self,
        locator: Union[_Locator, str],
        locator_variables: dict = {}
    ) -> SapElement***  

Initialize SAP UI element by the given locator.

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the name of one locator in locator store  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables,  set to initialize parameters in locator

**Returns:**  
    &emsp;[SapElement](./doc/api/python/sap/sapelement/sapelement.md) object, you can execute the following operations with the SapElement, such as select_item, get_statusbar. Before operating, it will try locate the element to verify whether the element exists.

**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui

    # get sap driver
    sap_driver = cc.sap

    # login sap application
    sap_driver.login("path", "connection", "client", "username", "password")

    # find sap element
    sap_ele = sap_driver.find_element(locator.sap.items_control)

    # parametric locator
    variables = {"name":"test"}
    sap_ele = sap_driver.find_element(locator.sap.items_control, variables)
```