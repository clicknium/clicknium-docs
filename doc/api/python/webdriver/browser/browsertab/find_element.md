# find_element
***def find_element(
        self,
        locator: Union[_Locator, str],
        locator_variables: dict = {}
    ) -> WebElement***  

 Initialize UI element by the given locator in current open browser.

>**Remarks:**  
Use the following method,
 `clicknium.chrome.open("https://bing.com").find_element()`, which is different with the method `clicknium.find_element()` [clicknium.find_element](./doc/api/python/find_element.md) when locating the UI element.
>- `clicknium.find_element()` is for UiElement of both web and window, and does not specify a scope to locate the element.
>- `clicknium.chrome.open("https://bing.com").find_element()` will locate the element in the specified browser.

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator    
        &emsp;&emsp; locator string, the name of one locator in locator store, eg: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, and locator name is search_sb_form_q  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, set to initialize parameters in locator, eg: var_dict = { "row": 1,  "column": 1}, more about variables, please refer to [Parametric Locator](./doc/automation/parametric_locator.md)

**Returns:**  
    &emsp;[WebElement](./doc/api/python/webdriver/browser/browsertab/webelement/webelement.md) object, you can operate as the following with the WebElement, such as click, set_text. It will locate the element to verify whether the element exists before operating.

**Example:**
***
```python
    from clicknium import clicknium as cc, locator

    chrome_tab = cc.chrome.open("https://bing.com")

    # find element
    webelement = chrome_tab.find_element(locator.chrome.bing.search_sb_form_q)

    # parametric locator
    variables = {"name":"test"}
    webelement = chrome_tab.find_element(locator.chrome.bing.search_sb_form_q, variables)
```