# BrowserTab.find_element
***def find_element(
        self,
        locator: Union[_Locator, str],
        locator_variables: dict = {}
    ) -> WebElement***  

Return the Web element defined by the given locator.

>**Remarks:**  
Use the following method,
`BrowserTab.find_element` is different with the method [clicknium.find_element](./doc/api/python/find_element.md) when locating the UI element.  
>- `clicknium.find_element()` is for both web and window UI element, and is not limited to a specific scope.  
>- `clicknium.chrome.open("https://bing.com").find_element()` will locate the element in its parent web page.  

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the visit path of locator for target UI element, eg: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, and locator name is search_sb_form_q. For more details, please refer to [Locator](./doc/automation/locator.md).   
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, set to initialize parameters in locator, eg: `{ "row": 1,  "column": 1}`, more about variables, please refer to [Parametric Locator](./doc/automation/parametric_locator.md).  

**Returns:**  
    &emsp;[WebElement](./doc/api/python/webdriver/browser/browsertab/webelement/webelement.md) object.

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