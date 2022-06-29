# click <!-- {docsify-ignore-all} -->
***def click(
        self,
        mouse_button: Literal["left", "middle", "right"] = MouseButton.Left,
        click_location: ClickLocation = ClickLocation(),
        click_method: Union[Literal["default", "mouse-emulation", "control-invocation"], ClickMethod] = ClickMethod.Default,
        modifier_key: Literal["nonekey", "alt", "ctrl", "shift","win"]  = ModifierKey.NoneKey,
        timeout: int = 30
    ) -> None***  

Single click the target element.

**Parameters:**  
    &emsp;**mouse_button**: MouseButton  
        &emsp;&emsp; The available values are: 'left', 'right' and 'center', default is 'left'.  
    &emsp;**click_location**: ClickLocation  
        &emsp;&emsp; it is set to define the position where the element to be clicked. Default position is center of element. Customize position by defining a [ClickLocation](./doc/api/python/uielement/clicklocation.md) object.   
    &emsp;**click_method**: ClickMethod  
        &emsp;&emsp; Defines the method to click the UI element.  
        &emsp;&emsp; `mouse-emulation`: click the target UI element by simulating mouse.  
        &emsp;&emsp; `control-invocation`: click the target UI element by invoking its UI method. It may not be supported if it is a window desktop element.  
        &emsp;&emsp; `default`: automatically choose method per element type. For Web element, use `control-invocation`; for Window element, use `mouse-emulation`.  
    &emsp;**modifier_key**: ModifierKey  
        &emsp;&emsp; The modifier key("alt", "ctrl", "shift", "win") to be pressed along with click, and default is none.      
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;None

**Examples:**

- Click left button
***
```python
from clicknium import clicknium as cc, locator, ui
ui(locator.chrome.bing.svg).click(mouse_button = "left")

tab = cc.chrome.open("https://contoso.com")
tab.find_element(locator.chrome.contoso.svg).click(mouse_button = "left")
```

- Click with customized ClickLocation
For button '5' as the target element in below application, we can click other buttons by setting its ClickLocation.
![sample1](../../../img/click_sample1.png)

> Remarks
>- ClickLocation is defined in `clicknium.common.models.clicklocation`


```python
from clicknium import clicknium as cc, locator, ui
from clicknium.common.models.clicklocation import ClickLocation

# click center of button '5'
ui(locator.applicationframe.button_num5butto).click()

# click button '6' 
# The click position is 100% of target element width away from the center of button '5' in x direction
ui(locator.applicationframe.button_num5butto).click(click_location=ClickLocation(xrate=1))

# click button '8'
# The click position is -100% of target element height away from the center of button '5' in y direction
ui(locator.applicationframe.button_num5butto).click(click_location=ClickLocation(yrate=-1))
```

- Click along with modifier_key  
For windows file explorer as follows:  
![sample2-1](../../../img/click_sample21.png)  
  - Click on folder 'test3' as `ui(locator.explorer.edit_system_item).click()`, then selection changed from 'test1' to 'test3'
![sample2-2](../../../img/click_sample22.png)  
  - Click on folder 'test3' as `ui(locator.explorer.edit_system_item).click(modifier_key=ModifierKey.Ctrl)`, then both 'test1' and 'test3' are in selection.
![sample2-3](../../../img/click_sample23.png) 