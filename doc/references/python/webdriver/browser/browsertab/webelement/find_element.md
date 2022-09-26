---
sidebar_position: 3
sidebar_label: find_element
---
# WebElement.find_element
***def find_element(
        self,
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        timeout: int = 30
    ) -> WebElement***  

Return the Web element defined by the given locator.

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the visit path of locator for target UI element, eg: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, and locator name is search_sb_form_q. For more details, please refer to [Locator](./../../../../../concepts/locator.md).   
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, set to initialize parameters in locator, eg: `{ "row": 1,  "column": 1}`, more about variables, please refer to [Parametric Locator](./../../../../../concepts/locator.md#parametric-locator).  
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation, the unit is second, and the default value is 30 seconds.

**Returns:**  
    &emsp;[WebElement](./webelement/webelement.md) object.

**Example:**
***
```python
from clicknium import clicknium as cc, locator

chrome_tab = cc.chrome.open("https://bing.com")

# find element
webelement = chrome_tab.find_element(locator.chrome.bing.search_sb_form_q)

# find sub element   
subelement = webelement.find_element(locator.chrome.bing.search_icon)

```