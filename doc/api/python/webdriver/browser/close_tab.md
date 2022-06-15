# close_tab

***def close_tab(
        self, 
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        timeout: int = 30
    ) -> None***  

Close specified tab.

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator  
        &emsp;&emsp; locator string, the name of one locator in locator store, eg: 'locator.chrome.document_newtab', locator store is chrome, and locator name is document_newtab  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, set to initialize parameters in locator, eg: var_dict = { "row": 1,  "column": 1}, more about variables, please refer to [parametric locator](./doc/automation/parametric_locator.md)  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;None

**Example:**
***
```python
    from clicknium import clicknium as cc

    # open chrome browser
    chrome_browser = cc.chrome.open("https://www.bing.com")

    # close tab
    chrome_browser.close_tab("locator.chrome.document_newtab")

    # parametric locator
    variables = {"name":"test"}
    chrome_browser.close_tab("locator.chrome.document_newtab", variables)
```