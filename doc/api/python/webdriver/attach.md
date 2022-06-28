# WebDriver.attach

***def attach(
        self,
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        is_maximize: bool = True,
        timeout = 30
    ) -> BrowserTab***  

Attach to an opened browser tab with specified locator.

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator  
        &emsp;&emsp; locator string, the visit path of locator for a UI element which is of the target browser tab. For more details, please refer to [Locator](./doc/automation/locator.md).   
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, set to initialize parameters in locator, eg: `{ "row": 1,  "column": 1}`, more about variables, please refer to [Parametric Locator](./doc/automation/parametric_locator.md).  
    &emsp;**is_maximize**: bool  
        &emsp;&emsp; is_maximize is set to define whether to maximize the browser window when attaching, and the default value is True.  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;[BrowserTab](./doc/api/python/webdriver/browser/browser_tab.md) object, you can execute the following operations in the browser tab such as: find_element, find_elements, close, refresh and so on.

**Example:**
***
```python
from clicknium import clicknium as cc

# attach ie browser
ie_tab = cc.ie.attach("locator.chrome.document_newtab")

# attach chrome browser
chrome_tab = cc.chrome.attach("locator.chrome.document_newtab")

# attach edge browser
edge_tab = cc.edge.attach("locator.chrome.document_newtab", is_maximize = False)

# attach firefox browser also with parametric locator
variables = {"name":"test"}
firefox_tab = cc.firefox.attach("locator.chrome.document_newtab", variables, timeout = 10)
```