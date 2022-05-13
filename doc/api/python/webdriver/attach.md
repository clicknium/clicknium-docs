# attach

***def attach(
        self,
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        is_maximize: bool = True,
        timeout = 30
    ) -> Browser***  

Attach to opened broswer.

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator  
        &emsp;&emsp; locator string, the name of one locator in locator store, ex: 'locator.chrome.document_newtab', locator store is chrome, locator name is document_newtab  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; The locator variables, is set to initialize parameters in locator, ex: var_dict = { "row": 1,  "column": 1}, more about variable, please refer to [parametric locator](./doc/parametric_locator.md  
    &emsp;**is_maximize**: bool  
        &emsp;&emsp; is_maximize is set to define whether to maximize the browser window. Default is True  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, unit is second, default value is 30 seconds 

**Returns:**  
    &emsp;[Browser](./doc/api/python/webdriver/browser/browser.md) object, you can use the browser to do the following operation: find_element, close_tab, refresh and so on

**Example:**
***
```python
    from clicknium import clicknium as cc

    # attach ie browser
    ie_browser = cc.ie.attach("locator.chrome.document_newtab")

    # attach chrome browser
    chrome_browser = cc.chrome.attach("locator.chrome.document_newtab")

    # attach edge browser
    edge_browser = cc.edge.attach("locator.chrome.document_newtab", is_maximize = False)

    # attach firefox browser also with parametric locator
    variables = {"name":"test"}
    firefox_browser = cc.firefox.attach("locator.chrome.document_newtab", variables, timeout = 10)
```