# ClickLocation
**ClickLocation class which can be initialized for mouse action on target element: click, double_click, mouse_up or mouse_down.**

**Parameters:**  
    &emsp;**Location**: Location  
        &emsp;&emsp; The relative position to the target element to perform the mouse action. The available values are 'center', 'left-top', 'left-bottom', 'right-top' and 'right-bottom', and the default value is 'center'.  
    &emsp;**Xoffset**: int   
        &emsp;&emsp; x offset sets the click position based on Location. When default value is 0, it means no offset.  
    &emsp;**Yoffset**: int  
        &emsp;&emsp; y offset sets the click position based on Location. Default value is 0.  
    &emsp;**Xrate**: int  
        &emsp;&emsp; x rate percent of the click position is based on Location. When default value is 0, it means no offset. If xrate is 1, it means X of click postion moving to right. The distance is 1*element's width pixsels.  
    &emsp;**Yrate**: int  
        &emsp;&emsp; y rate percent sets the click position based on Location. When default value is 0, it means no offset. If xrate is 1, it means Y of click postion moving to right. The distance is element's height pixsels. 
    
**Definition:**
```python
    class ClickLocation(object):

     def __init__(self, location: Literal["center", "left-top", "left-bottom", "right-top","right-bottom"] = Location.Center, xoffset=0, yoffset=0, xrate=0, yrate=0):
        self.Location = location
        self.Xoffset = xoffset
        self.Yoffset = yoffset
        self.Xrate = xrate
        self.Yrate = yrate
     
```