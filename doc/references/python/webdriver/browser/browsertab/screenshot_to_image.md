---
sidebar_position: 18
sidebar_label: screenshot_to_image
---
# BrowserTab.screenshot_to_image  

***def screenshot_to_image(
        self,
        image_file: str,
        mode: Literal["bounds", "viewport", "full"] = ScreenShotMode.Full,
        rect: Rectangle = None,
        wait_for_page_delay: int = 0
    ) -> None***  


Save current browser tab's screenshot to file using CDP tech. Only support for chromium web tabs.   

**Parameters:**  
    &emsp;**image_file[Required]**: str   
        &emsp;&emsp; File path to save image.  
    &emsp;**mode**: Literal["bounds", "viewport", "full"] = ScreenShotMode.Full     
        &emsp;&emsp; Define the mode to capture browser tab's screenshot:  
        &emsp;&emsp;&emsp;&emsp; bounds: takes a screenshot of the specified rectangle of the page, using parameter `rect` to define the rectangle.  
        &emsp;&emsp;&emsp;&emsp; viewport: takes a screenshot of the currently visible viewport.  
        &emsp;&emsp;&emsp;&emsp; full: takes a screenshot of the full scrollable page, using parameter `wait_for_page_delay` to wait the page ready.      
    &emsp;**next_page_button_locator**: Union[_Locator, str] = None       
        &emsp;&emsp; The visit path of locator for goto next page UI element. If it's None, means just extract the current page data.      
    &emsp;**rect**: Rectangle = None  
        &emsp;&emsp; an object which specifies clipping of the resulting image.   
    &emsp;**wait_for_page_delay**: int = 0   
        &emsp;&emsp; The timout for waiting for the page ready, the unit is second.  

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc
from clicknium.common.enums import ScreenShotMode
import os,sys


file = os.path.join(os.path.abspath(sys.path[0]), "tmp.jpg")
tab = cc.chrome.open("http://clicknium.com")
tab.screenshot_to_image(file, ScreenShotMode.Viewport)

```