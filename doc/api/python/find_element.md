# find_element
***def find_element(
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        window_mode: Literal["auto", "topmost", "noaction"] = WindowMode.Auto
    ) -> UiElement***  

Initialize ui element by the given locator.  

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, the name of one locator in locator store, ex: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, locator name is search_sb_form_q  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, is set to initialize parameters in locator, ex: var_dict = { "row": 1,  "column": 1}, more about variable, please refer to [parametric locator](../../parametric_locator.md)  
    &emsp;**window_mode**: WindowMode  
        &emsp;&emsp; Window mode define whether to set the window on topmost for the following operation on the element  
        &emsp;&emsp;**Auto**：Default value is auto, it means setting the window automatically, we set the internal context for automation operation, the context stores info about the ui element operated just now, include process name, main window title etc. if current ui element's info is same as previous, then don't need set window topmost as it should be already set; or will set window topmost  
        &emsp;&emsp;**TopMost**：always setting the window on topmost  
        &emsp;&emsp;**NoAction**： always don't setting the window on topmost 

**Returns:**  
    &emsp;[UiElement](./doc/api/python/uielement/uielement.md) object, you can use the uielement to do the following operation, such as click, set_text, before operating, it will try locate the element to verify whether the element exist

**Remark:**  
    &emsp;There is a aliase method ui for shorten clicknium.find_element,  `clicknium.find_element()` can be written as `ui()`

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