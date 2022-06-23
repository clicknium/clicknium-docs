# clicknium.find_element
***def find_element(
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        window_mode: Literal["auto", "topmost", "noaction"] = WindowMode.Auto
    ) -> UiElement***  

Initialize UI element by the given locator.

> **Remarks:**  
>- An aliase method UI to shortening clicknium.find_element,  `clicknium.find_element()` can be written as `ui()`

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the name of one locator in locator store, eg: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, and locator name is search_sb_form_q  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, set to initialize parameters in locator, eg: var_dict = { "row": 1,  "column": 1}, more about variables, please refer to [Parametric Locator](./doc/automation/parametric_locator.md)  
    &emsp;**window_mode**: WindowMode  
        &emsp;&emsp; Window mode defines whether to set the window on topmost with the following operation on the element.  
        &emsp;&emsp;`auto`：Default value is auto, which means setting the window automatically. We set the internal context for automation operation, and the context stores info of the operated UI element, including process name, main window title etc. If current UI element's info is same as previous, there no need to set window topmost, otherwise, set window topmost.  
        &emsp;&emsp;`topmost`：always set the window on topmost   
        &emsp;&emsp;`noaction`： always do not set the window on topmost 

**Returns:**  
    &emsp;[UiElement](./doc/api/python/uielement/uielement.md) object, you can execute the following operations with the UiElement, such as click, set_text. Before operating, it will try locate the element to verify whether the element exists.

**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui

    cc.find_element(locator.chrome.bing.search_sb_form_q)
    #or 
    ui(locator.chrome.bing.search_sb_form_q)

    #parametric locator
    variables = {"name":"test"}
    ui(locator.chrome.bing.search_sb_form_q, variables)
```