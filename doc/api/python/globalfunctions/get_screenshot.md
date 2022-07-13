---
sidebar_position: 9
---
# clicknium.get_screenshot
***def get_screenshot(image_file: str) -> None***  

Saves a screenshot of the current window to an image file.

**Parameters:**  
    &emsp;**image_file[Required]**: str   
        &emsp;&emsp; file path to save image

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc

cc.get_screenshot("D:\\screenshot.png")

```