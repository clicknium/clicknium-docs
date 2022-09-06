---
sidebar_position: 4
sidebar_label: is_existing
---
# BrowserTab.is_existing
***def is_existing(
        self,
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        timeout: int = 30
    ) -> bool***  

 Check whether the specified element of the web page exists.  

>**Remarks:**  
`BrowserTab.is_existing` is different with the method [clicknium.is_existing](./../../../globalfunctions/is_existing.md) when locating the UI element.
>- `clicknium.is_existing()` is for both web and window UI element, and not limited to a specific scope.
>- `clicknium.chrome.open("https://bing.com").is_existing()` will locate element in its parent web page.


**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; Locator string, the visit path of locator for target UI element, eg: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, and locator name is search_sb_form_q. For more details, please refer to [Locator](./../../../../../concepts/locator.md).   
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; Locator variables, set to initialize parameters in locator, eg: `{ "row": 1,  "column": 1}`, more about variables, please refer to [Parametric Locator](./../../../../../concepts/locator.md#parametric-locator).  
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;Return True if UI element exists, otherwise return False

**Example:**
***
```python
from clicknium import clicknium as cc, locator, ui

chrome_tab = cc.chrome.open("https://bing.com")

# check element if exist
chrome_tab.is_existing(locator.chrome.bing.search_sb_form_q)

# parametric locator
variables = {"name":"test"}
chrome_tab.is_existing(locator.chrome.bing.search_sb_form_q, variables)
```