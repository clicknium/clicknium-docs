---
sidebar_position: 6
sidebar_label: scroll
---

# clicknium.mouse.scroll

```python
def scroll(
        self,
        times = 1,
        modifier_key: Literal["nonekey", "alt", "ctrl", "shift","win"]  = ModifierKey.NoneKey
    ) -> None
```  

Do the mouse scroll wheel.

**Parameters:**  
    &emsp;**times**: int  
        &emsp;&emsp; an integer number of times to scroll, and default is 1. When the value is greater than zero means scroll up, others means scroll down.    
    &emsp;**modifier_key**: ModifierKey  
        &emsp;&emsp; the modifier key("alt", "ctrl", "shift", "win") to be pressed along with click, and default is none.    

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc

# Do the mouse scroll wheel with up direction and scroll 2 times and press along with modifier key "ctrl"
cc.mouse.scroll(2,'ctrl')

```