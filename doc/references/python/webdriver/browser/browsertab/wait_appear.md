---
sidebar_position: 5
sidebar_label: wait_appear
---
# BrowserTab.wait_appear
***def wait_appear(
        self,
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        wait_timeout: int = 30
    ) -> WebElement***  

Wait for the specified element of the web page to appear within given timeout.  

>**Remarks:**  
`BrowserTab.wait_appear` is different with [clicknium.wait_appear](./../../../globalfunctions/wait_appear.md) when locating the UI element.
>- `clicknium.wait_appear()` is for both the web and window UI element, and not limited to a specific scope.  
>- `clicknium.chrome.open("https://bing.com").wait_appear()` will locate element in its parent web page.  

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the visit path of locator for target UI element, eg: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, and locator name is search_sb_form_q. For more details, please refer to [Locator](./../../../../../automation/locator.md).   
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, set to initialize parameters in locator, eg: `{ "row": 1,  "column": 1}`, more about variables, please refer to [Parametric Locator](./../../../../../automation/parametric_locator.md).  
    &emsp;**timeout**: int  
        &emsp;&emsp; wait timeout for the operation, the unit is second, default value is 30 seconds.  

**Returns:**  
    &emsp;[WebElement](./webelement/webelement.md) object, or None if the element does not appear.  

**Example:**
***
```python
from clicknium import clicknium as cc, locator

chrome_tab = cc.chrome.open("https://bing.com")

# wait element appear
element = chrome_tab.wait_appear(locator.chrome.bing.search_sb_form_q)

# parametric locator
variables = {"name":"test"}
element = chrome_tab.wait_appear(locator.chrome.bing.search_sb_form_q, variables)

```