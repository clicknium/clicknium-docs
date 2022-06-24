# SapElement.get_statusbar

***def get_statusbar(
        self, 
        timeout: int = 30
    ) -> SapStatusBarInfo***  

Get the information of the SAP status bar.

**Parameters:**  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;SapStatusBarInfo object, the class definition is as follows:  

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

# find sap element
sap_ele = sap_driver.find_element(locator.sap.satus_bar_q)

# get staus bar info
status_bar = sap_ele.get_statusbar()
```