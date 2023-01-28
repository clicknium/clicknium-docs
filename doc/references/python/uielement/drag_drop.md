# drag_drop
```python
def drag_drop(
        self,
        xpoint: int = 0,
        ypoint: int = 0,
        speed: int = 50,
        timeout: int = 30
    ) -> None
```  

Hold down the mouse left button on the source element, then move to the target offset and release the mouse button. 

**Parameters:**  
    &emsp;**xpoint**: int    
        &emsp;&emsp; Moved pixels in X-Axis.  
    &emsp;**ypoint**: int   
        &emsp;&emsp; Moved pixels in Y-Axis.  
    &emsp;**speed**: int  
        &emsp;&emsp; Drag speed, the unit is ms/10px, and the default value is 50.  
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation, the unit is second, and the default value is 30 seconds.  

**Returns:**  
    &emsp;None

**Examples:**
***
```python
from clicknium import clicknium as cc, locator, ui

# drag the scroll button right 20 pixels
ui(locator.app.bing.scrollbutton).drag_drop(20, 0)
  
# drag the scroll button down 20 pixels
ui(locator.app.bing.scrollbutton).drag_drop(0, 20)
```

- Drag scroll bar button of notepad  
Scroll down 50 pixels like this: `ui(locator.notepad.thumb_scrollbar).drag_drop(0, 50)`  
![sample1](../../../img/drap_drop_sample1_2.png)  

- Move slider button from left to right  
Scroll right 20 pixels like this: `ui(locator.uiautomationwpfd.thumb_thumb).drag_drop(20, 0)`  
![sample2](../../../img/drap_drop_sample2_2.png)  