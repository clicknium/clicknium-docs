# Click
***def click(self, click_type = ClickType.Click, mouse_button = MouseButton.Left, click_location = ClickLocation.Center, click_method = ClickMethod.Default, modifier_key = ModifierKey.NoneKey, xoffset = 0, yoffset= 0, xrate=0, yrate = 0, timeout = 30)***  

Click an element with single click, up click or down click.  

**Parameters:**  
    &emsp;**click_type**: ClickType   
        &emsp;&emsp; Click type for single, up and down.'  
    &emsp;**mouse_button**: MouseButton  
        &emsp;&emsp; Mouse button is set to define the mouse button to click. Default value is left, it will click with mouse left button.  
    &emsp;**click_location**: ClickLocation  
        &emsp;&emsp; Click location is set to define the element position to click. Default value is center, it will click the element's center position.  
    &emsp;**click_method**: ClickMethod  
        &emsp;&emsp; Click method is set to which method to use when clicking the element. Default vaule is dafult, it click with default method.Mouse emulation, it click like mouse perform. Control invocation, it click like control.  
    &emsp;**modifier_key**: ModifierKey  
        &emsp;&emsp; X offset is set the click position based on element's center position. Default value is 0.  
    &emsp;**xoffset**: int  
        &emsp;&emsp; Y offset is set the click position based on element's center position. Default value is 0.  
    &emsp;**yoffset**: int  
        &emsp;&emsp; X rate percent is set the click position based on element's center position. Default value is 0.  
    &emsp;**xrate**: int  
        &emsp;&emsp; X rate percent is set the click position based on element's center position. Default value is 0.    
    &emsp;**yrate**: int  
        &emsp;&emsp; Modifier key  is set to click with the modifier key(Control, Alt, Shift, Win). Default vaule is none.  
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for locating element. The unit of parameter is seconds. Default is set to 30 seconds.  

**Tips:**  
        &emsp;Import ClickType, MouseButton, ClickLocation, ClickMethod, ModifierKey modules with   
        &emsp;`from clicknium.common.enums import ClickType, MouseButton, ClickLocation, ClickMethod, ModifierKey` **Or**  
        &emsp;`from clicknium.common.enums import *`

**Returns:**  
    &emsp;None

**Example:**
***
```python
    >>> from clicknium import clicknium as cc, selectorstore
    from clicknium.common.enums import MouseButton
    >>> cc.find_element(selectorstore.chrome.baidu.text_kw).click(mouse_button = MouseButton.Right)
```