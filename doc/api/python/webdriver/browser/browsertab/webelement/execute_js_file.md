# execute_js_file

***def execute_js_file(
        self,
        javascript_file: str, 
        method_invoke: str = '', 
        timeout: int = 30
    ) -> str***  

Execute javascript file for the target element.

> **Remarks:**
>
>- For javascript script, use "_context$.currentElement." as the target element
>- For the invoked method, valid method_invoke string should be like "run()", or when passing parameters, it should be like "run("execute js", 20)"

**Parameters:**  
    &emsp;**javascript_file[Required]**: str    
        &emsp;&emsp; javascript file, execute code to target element, use "_context$.currentElement." as the target element, ex: we can set javascript file's content as "function SetText(st){_context$.currentElement.value = st; console.log("execute js"); return \"success\"}"  
    &emsp;**method_invoke**: str    
        &emsp;&emsp; For method invoke string, it should be like "run()", or when passing parameters, it should be like "run("execute js", 20)", eg: for above javascript code, we can set to "SetText(\"execute\")"  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;str, execution result

**Example:**
***
```python
    from clicknium import clicknium as cc

    # open Chrome browser
    chrome_tab = cc.chrome.open("https://www.bing.com")

    # execute js, set text for target element
    # test.js's content can be "function SetText(st){_context$.currentElement.value = st; console.log("execute js"); return \"success\"}"
    result = chrome_tab.execute_js_file("locator.chrome.cn.search_sb_form_q", "C:\\test\\test.js", "SetText(\"click\")")
```