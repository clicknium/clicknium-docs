# find_element
***def find_element(
        self,
        locator: Union[_Locator, str],
        locator_variables: dict = {}
    ) -> UiElement***  

In current opened browser, initialize ui element by the given locator.  

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator    
        &emsp;&emsp; locator string, the name of one locator in locator store, ex: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, locator name is search_sb_form_q  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, is set to initialize parameters in locator, ex: var_dict = { "row": 1,  "column": 1}, more about variable, please refer to [parametric locator](./doc/automation/parametric_locator.md)

**Returns:**  
    &emsp;[UiElement](./doc/api/python/uielement/uielement.md) object, you can use the uielement to do the following operation, such as click, set_text, before operating, it will try locate the element to verify whether the element exist

**Remarks**  
It should be used like `clicknium.chrome.open("https://bing.com").find_element()`, it is different with `clicknium.find_element()` [clicknium.find_element](./doc/api/python/find_element.md) when locating the ui element.
- `clicknium.find_element()` is for both web and desktop's uielement, and does not specified a scope to locate the element
- `clicknium.chrome.open("https://bing.com").find_element()` will locate element in the specified browser

**Example:**
***
```python
    from clicknium import clicknium as cc, locator

    browser = cc.chrome.open("https://bing.com")

    # find element
    element = browser.find_element(locator.chrome.bing.search_sb_form_q)

    # parametric locator
    variables = {"name":"test"}
    element = browser.find_element(locator.chrome.bing.search_sb_form_q, variables)
```