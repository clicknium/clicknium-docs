---
sidebar_position: 3
sidebar_label: find_elements
---
# BrowserTab.find_elements
***def find_elements(
        self,
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        timeout: int = 30
    ) -> List[WebElement]***  

Return list of all matched Web elements by the given locator in current web page.

> **Remarks:**  
`BrowserTab.find_elements` is different with the method [clicknium.find_elements](./../../../globalfunctions/find_elements.md) when locating the UI elements.  
>- `clicknium.find_elements()` is for both web and window UI element, and is not  limited to a specific scope.  
>- `clicknium.chrome.open("https://bing.com").find_elements()` will locate elements in its parent web page.  

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the visit path of locator for target UI element, eg: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, and locator name is search_sb_form_q. For more details, please refer to [Locator](./../../../../../concepts/locator.md).   
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, set to initialize parameters in locator, eg: `{ "row": 1,  "column": 1}`, more about variables, please refer to [Parametric Locator](./../../../../../concepts/parametric_locator.md).  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds.

**Returns:**  
    &emsp;List of [WebElement](./webelement/webelement.md) objects.  

**Example:**
***
```python
from clicknium import clicknium as cc, locator, ui

tab = cc.edge.open("https://www.bing.com/")
tab.find_element(locator.new_store.sample.bing.search_sb_form_q).set_text('clicknium')
tab.find_element(locator.new_store.sample.bing.svg).click()
result_elements = tab.find_elements(locator.new_store.sample.bing.a_search_result)
for elem in result_elements:
    elem.highlight(duration=1)
tab.close()
```