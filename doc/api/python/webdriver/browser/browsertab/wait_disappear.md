---
sidebar_position: 6
sidebar_label: wait_disappear
---
# BrowserTab.wait_disappear
***def wait_disappear(
        self,
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        wait_timeout: int = 30
    ) -> bool***  

Wait for the specified element of the web page to disappear within given timeout.

>**Remarks:**  
`BrowserTab.wait_disappear` is different with [clicknium.wait_disappear](./../../../globalfunctions/wait_disappear.md) when locating the UI element.
>- `clicknium.wait_disappear()` is for both web and window uielement, and not limited to a specific scope.  
>- `clicknium.chrome.open("https://bing.com").wait_disappear()` will locate element in its parent web page.  

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the visit path of locator for target UI element, eg: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, and locator name is search_sb_form_q. For more details, please refer to [Locator](./../../../../../automation/locator.md).   
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, set to initialize parameters in locator, eg: `{ "row": 1,  "column": 1}`, more about variables, please refer to [Parametric Locator](./../../../../../automation/parametric_locator.md).  
    &emsp;**timeout**: int  
        &emsp;&emsp; wait timeout for the operation, the unit is second, default value is 30 seconds.  

**Returns:**  
    &emsp;bool, return True if the element disappears within given timeout otherwise return False.  

**Example:**
***
```python
from clicknium import clicknium as cc, locator

chrome_tab = cc.chrome.open("https://bing.com")

# wait element disappear
chrome_tab.wait_disappear(locator.chrome.bing.search_sb_form_q)

# parametric locator
variables = {"name":"test"}
chrome_tab.wait_disappear(locator.chrome.bing.search_sb_form_v, variables)

```