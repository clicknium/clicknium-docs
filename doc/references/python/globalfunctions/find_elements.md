---
sidebar_position: 2
---
# clicknium.find_elements
```python 
def find_elements(
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        timeout: int = 30
    ) -> List[UiElement]
```

Return list of all matched UI elements by the given locator.

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; Locator string, the visit path of locator for target UI element, eg: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, and locator name is search_sb_form_q. For more details, please refer to [Locator](./../../../concepts/locator.md).  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; Locator variables, set to initialize parameters in locator, eg: `{ "row": 1,  "column": 1}`, more about variables, please refer to [Parametric Locator](./../../../concepts/locator.md#parametric-locator).  
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for locating all matched UI elements, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;List of matched elements with type [UiElement](./../../python/uielement/uielement.md).

**Example:**
***
```python
from clicknium import clicknium as cc, locator, ui

cc.edge.open("https://www.bing.com/")
ui(locator.store.sample.bing.search_sb_form_q).set_text('clicknium')
ui(locator.store.sample.bing.svg).click()

result_elements = cc.find_elements(locator.store.sample.bing.a_search_result)
for elem in result_elements:
    elem.highlight(duration=1)
```