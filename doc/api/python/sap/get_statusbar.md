# get_statusbar

***def get_statusbar(
        self, 
        locator: Union[_Locator, str],
        locator_variables: dict = {}, 
        timeout: int = 30
    ) -> SapStatusBarInfo***  

Get sap status bar info.

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator  
        &emsp;&emsp; locator string, the name of one locator in locator store, ex: 'locator.sap.satus_bar_q', locator store is sap, locator name is satus_bar_q  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, is set to initialize parameters in locator, ex: var_dict = { "row": 1,  "column": 1}, more about variable, please refer to [parametric locator](./doc/automation/parametric_locator.md)  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, unit is second, default value is 30 seconds 

**Returns:**  
    &emsp;SapStatusBarInfo class, the class definition as following:  
```python
    class SapStatusBarInfo(object):

     def __init__(self, statusbar_info):
        self.Id = statusbar_info.Id,  # status bar id
        self.Number = statusbar_info.Number, # status bar number
        self.Text = statusbar_info.Text, # status bar text
        self.Type = statusbar_info.Type, # status bar type
```


**Example:**
***
```python
    from clicknium import clicknium as cc, locator

    # get sap driver
    sap_driver = cc.sap

    # login sap application
    sap_driver.login("path", "connection", "client", "username", "password")

    # get staus bar info
    status_bar = sap_driver.get_statusbar(locator.sap.satus_bar_q)
```