# save_to_image  
***def save_to_image(
        self,
        image_file: str,
        img_width: int = 0,
        img_height: int = 0,
        xoffset: int = 0,
        yoffset: int  = 0,
        timeout: int = 30
    ) -> None***

Save target element's screenshot to file with the specified size and offset.

**Parameters:**   
    &emsp;**image_file[Required]**: str  
        &emsp;&emsp; file path to save image  
    &emsp;**img_width**: int  
        &emsp;&emsp; image width. When default is 0, target element's screenshot real width will be uesed.
    &emsp;**img_height**: int  
        &emsp;&emsp; image height. When default is 0, target element's screenshot real height will be used.
    &emsp;**xoffset**:  int  
        &emsp;&emsp; offset of X-Axis, When default is 0, it means no offset.  
    &emsp;**yoffset**: int  
        &emsp;&emsp; offset of Y-Axis, When default is 0, it means no offset.  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;None

**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui
    
    ui(locator.chrome.bing.search_sb_form_q).save_to_image("D:\\screenshot.png")
```