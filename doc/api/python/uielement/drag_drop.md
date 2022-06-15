# drag_drop
***def drag_drop(
        self,
        xpoint: int = 0,
        ypoint: int = 0,
        speed: int = 50,
        timeout: int = 30
    ) -> None***  

Hold down the left mouse button on the source element, then move to the target offset and release the mouse button. 

**Parameters:**  
    &emsp;**xpoint**: int    
        &emsp;&emsp; pixels of X-Axis will be moved  
    &emsp;**ypoint**: int   
        &emsp;&emsp; pixels of X-Axis will be moved  
    &emsp;**speed**: int  
        &emsp;&emsp; drag speed, the unit is ms/10px, and the default value is 50  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds.  

**Returns:**  
    &emsp;None

**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui
    # drag the target scroll button right to 20 pixels
    ui(locator.app.bing.scrollbutton).drag_drop(20, 0)
    # same as
    cc.find_element(locator.app.bing.scrollbutton).drag_drop(20, 0)
    
    # drag the target scroll button down to 20 pixels
    ui(locator.app.bing.scrollbutton).drag_drop(0, 20)
```

- move scroll bar of notepad  
![sample1](../../../img/drap_drop_sample1.png)  
If you need scroll down 50 pixels, invoke like this: `ui(locator.notepad.thumb_scrollbart).drag_drop(0, 50)`  
![sample1](../../../img/drap_drop_sample1_2.png)  

- move slider from left to right  
![sample2](../../../img/drap_drop_sample2_1.png)  
If you need scroll right 20 pixels, invoke like this: `ui(locator.uiautomationwpfd.thumb_thumb).drag_drop(20, 0)`  
![sample2](../../../img/drap_drop_sample2_2.png)  