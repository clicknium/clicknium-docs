# WebElement.execute_js_file

***def execute_js_file(
        self,
        javascript_file: str, 
        method: str = '', 
        timeout: int = 30
    ) -> str***  

Execute javascript file for the target element.

> **Remarks:**
> In the javascript file to execute specified in parameter `javascript_file`, use "_context$.currentElement." for the target element.  

**Parameters:**  
    &emsp;**javascript_file[Required]**: str    
        &emsp;&emsp; javascript file path, eg.: "c:\\test\test.js".  
    &emsp;**method**: str    
        &emsp;&emsp; the method to be invoked should be defined in the javascript file. If any parameter need to passed to the method, it can be included in this parameter value, for eg.: SetText(\"test\").  
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

# test.js content can be:  
#  function SetText(st){  
#     _context$.currentElement.value = st;
#     console.log("execute js");
#     return "success"
#  }

result = chrome_tab.find_element(locator.chrome.bing.search_sb_form_q).execute_js_file("C:\\test\\test.js", "SetText(\"click\")")
```