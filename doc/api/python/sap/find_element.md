# clicknium.sap.find_element
***def find_element(
        self,
        locator: Union[_Locator, str],
        locator_variables: dict = {}
    ) -> SapElement***  

Return the first matched SAP UI element by the given locator.

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the visit path of locator for target SAP UI element.
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables,  set to initialize parameters in locator.

**Returns:**  
    &emsp;[SapElement](./doc/api/python/sap/sapelement/sapelement.md) object.

**Example:**
***
```python
from clicknium import clicknium as cc, locator, ui

# login sap application
cc.sap.login("path", "connection", "client", "username", "password")

# find sap element
sap_ele1 = cc.sap.find_element(locator.sap.items_control1)
sap_ele1.select_item("item1")

# parametric locator
variables = {"name":"test"}
sap_ele2 = cc.sap.find_element(locator.sap.bar_control, variables)
sap_ele2.get_statusbar()
```