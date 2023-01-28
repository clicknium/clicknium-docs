---
sidebar_position: 1
---
# clicknium.find_element
```python
def find_element(
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        window_mode: Literal["auto", "topmost", "noaction"] = WindowMode.Auto
    ) -> UiElement 
```

Return the UI element defined by the given locator.

> **Remarks:**  
>An alias method `ui()` is equivalent to `clicknium.find_element()`. 

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the visit path of locator for target UI element, eg: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, and locator name is search_sb_form_q. For more details, please refer to [Locator](./../../../concepts/locator.md).   
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, set to initialize parameters in locator, eg: `{ "row": 1,  "column": 1}`.  
        &emsp;&emsp; More about variables, please refer to [Parametric Locator](./../../../concepts/locator.md#parametric-locator).  
    &emsp;**window_mode**: WindowMode  
        &emsp;&emsp; It defines whether to set the UI element's parent window to topmost before an action is invoked.  
        &emsp;&emsp;`auto`: default value, set the window to topmost by default.  
        &emsp;&emsp;`topmost`: always set the window to topmost  
        &emsp;&emsp;`noaction`: doing nothing for topmost mode 

**Returns:**  
    &emsp;The first matched UI element with type [UiElement](./../../python/uielement/uielement.md).

**Example:**
***
```python
from clicknium import clicknium as cc, locator, ui

searchBox = cc.find_element(locator.chrome.bing.search_sb_form_q)
#or 
searchBox = ui(locator.chrome.bing.search_sb_form_q)

#parametric locator
variables = {"name":"test"}
searchBox = ui(locator.chrome.bing.search_sb_form_q, variables)
```