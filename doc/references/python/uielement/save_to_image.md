# save_to_image  
````python 
def save_to_image(
        self,
        image_file: str,
        img_width: int = 0,
        img_height: int = 0,
        xoffset: int = 0,
        yoffset: int  = 0,
        timeout: int = 30
    ) -> None
```

Save target element's screenshot to file with the specified size and offset.

**Parameters:**   
    &emsp;**image_file[Required]**: str  
        &emsp;&emsp; File path of saved image.  
    &emsp;**img_width**: int  
        &emsp;&emsp; Specify the screenshot width. Default is the target element's width.  
    &emsp;**img_height**: int  
        &emsp;&emsp; Speficy the screenshot height. Default is the target element's height.  
    &emsp;**xoffset**:  int  
        &emsp;&emsp; Offset of X-Axis from the target element's left-top corner.  
    &emsp;**yoffset**: int  
        &emsp;&emsp; Offset of Y-Axis from the target element's left-top corner.  
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation, the unit is second, and the default value is 30 seconds.  

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc, locator, ui
    
ui(locator.chrome.bing.search_sb_form_q).save_to_image("D:\\screenshot.png")
```