# save_to_image  
***def save_to_image(
        self,
        image_file: str,
        img_width: int = 0,
        img_height: int = 0,
        xoffset: int = 0,
        yoffset: int  = 0,
        timeout: int = 30)***

Save target element's screenshot to file with specified size and offset.

**Parameters:** 
    &emsp;**image_file**: str  
        file path to save image  
    &emsp;**img_width**: int  
        &emsp;&emsp;image width. Default 0, will use target element's screenshot real width  
    &emsp;**img_height**: int  
        &emsp;&emsp;image height. Default 0, will use target element's screenshot real height  
    &emsp;**xoffset**:  int  
        &emsp;&emsp; offset of X-Axis, Default 0, means not offset  
    &emsp;**yoffset**: int  
        &emsp;&emsp; offset of Y-Axis, Default 0, means not offset  
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation. The unit of parameter is seconds. Default is set to 30 seconds.  

**Returns:**  
    &emsp;None

**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui
    
    ui(locator.chrome.bing.search_sb_form_q).save_to_image("D:\screenshot.png")
```