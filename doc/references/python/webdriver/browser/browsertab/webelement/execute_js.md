---
sidebar_position: 2
sidebar_label: execute_js
---
# WebElement.execute_js

***def execute_js(
        self,
        javascript_code: str, 
        method: str = '', 
        timeout: int = 30
    ) -> str***  

Execute Javascript code for the target element.  

> **Remarks:**
> In the Javascript code, execute specified in parameter `javascript_code`, by using "_context$.currentElement." for the target element.  

**Parameters:**  
    &emsp;**javascript_code[Required]**: str    
        &emsp;&emsp; Javascript code snippet to be executed upon target element.  
    &emsp;**method**: str    
        &emsp;&emsp; the method to be invoked should be defined in the Javascript code. If any parameter needs to passed to the method, it can be included in this parameter value, for eg.: SetText(\"test\").  
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
webEle = chrome_tab.find_element(locator.chrome.bing.search_sb_form_q)
js = "function SetText(text){_context$.currentElement.value = text; console.log(\"exit 0\"); return \"success\"}"

result = webEle.execute_js(js, "SetText(\"click\")")
```