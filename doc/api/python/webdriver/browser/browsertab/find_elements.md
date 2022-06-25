# find_elements
***def find_elements(
        self,
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        timeout: int = 30
    ) -> List[WebElement]***  

Find elements by the given locator.  

> **Remarks:**  
Use the following method, `clicknium.chrome.open("https://bing.com").find_elements()`, which is different with the method`clicknium.find_elements()` [clicknium.find_elements](./doc/api/python/find_elements.md) when locating the UI elements.
>- `clicknium.find_elements()` is for  UiElements of both web and window, and does not specify a scope to locate the elements.
>- `clicknium.chrome.open("https://bing.com").find_elements()` will locate elements in the specified browser.

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the name of one locator in locator store, eg: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, and locator name is search_sb_form_q  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, set to initialize parameters in locator, eg: var_dict = { "row": 1,  "column": 1}, more about variables, please refer to [Parametric Locator](./doc/automation/parametric_locator.md)  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds.

**Returns:**  
    &emsp;[WebElement](./doc/api/python/webdriver/browser/browsertab/webelement/webelement.md) object, ou can operate as the following with the UiElement, such as click, set_text.It will locate the element to verify whether the element exists before operating.

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