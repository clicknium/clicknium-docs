---
sidebar_position: 12
sidebar_label: screenshot_to_image
---
# WebElement.screenshot_to_image  

```python 
def screenshot_to_image(
        self,
        image_file: str,
        timeout: int = 30
    ) -> None
```  


Save target element's screenshot to file using cdp tech. Only support for chromium webelements.  

**Parameters:**  
    &emsp;**image_file[Required]**: str   
        &emsp;&emsp; File path to save image.    
    &emsp;**timeout**: int = 30   
        &emsp;&emsp; Timeout for the operation. The unit of parameter is seconds. Default is set to 30 seconds  

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc
import os,sys

file = os.path.join(os.path.abspath(sys.path[0]), "tmp.jpg")
tab = cc.chrome.open("http://clicknium.com")
web_element = tab.find_element(locator.chrome.sample)
web_element.screenshot_to_image(file, 1)
```