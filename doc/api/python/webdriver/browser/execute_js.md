# execute_js

***def execute_js(
        self,
        locator: Union[_Locator, str], 
        javascript_code: str, 
        method_invoke: str = '', 
        locator_variables: dict = {}, 
        timeout: int = 30
    ) -> str***  

Execute javascript code snippet for the target element

> **Remarks:**
>
>- For javascript code, use "_context$.currentElement." as the target element.
>- For method invoke, valid method_invoke string should like "run()", or when passing parameters should like "run("execute js", 20)".

**Parameters:**  
    &emsp;**locator[Required]**: str | _Locator  
        &emsp;&emsp; locator string, the name of one locator in locator store, eg: 'locator.chrome.bing.search_sb_form_q', locator store is chrome, and locator name is search_sb_form_q  
    &emsp;**javascript_code[Required]**: str    
        &emsp;&emsp; javascript code snippet string, execute code to target element, use `_context$.currentElement` as the target element, ex: "function SetText(st){_context$.currentElement.value = st; console.log("execute js"); return \"success\"}"  
    &emsp;**method_invoke**: str    
        &emsp;&emsp; For method invoke string, it should be like "run()", or when passing parameters, it should be like "run("execute js", 20)", eg: for above javascript code, we can set to "SetText(\"execute\")"  
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables,set to initialize parameters in locator, eg: var_dict = { "row": 1,  "column": 1}, more about variables, please refer to [parametric locator](./doc/automation/parametric_locator.md)  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;str, execution result

**Example:**
***
```python
    from clicknium import clicknium as cc

    # open chrome browser
    chrome_tab = cc.chrome.open("https://www.bing.com")

    # execute js, set text for target element
    result = chrome_tab.execute_js("locator.chrome.cn.search_sb_form_q", "function SetText(text){_context$.currentElement.value = text; console.log("exit 0"); return \"success\"}", "SetText(\"click\")")
```