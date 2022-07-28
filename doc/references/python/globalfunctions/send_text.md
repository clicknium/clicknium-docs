---
sidebar_position: 8
---
# clicknium.send_text
***def send_text(
        self,
        text: str
    ) -> None***  

Send text to the cursor's current position.

>**Remarks:**  
This method is to send text to the system. If you need to send the text to a specific UI element, you need to set the UI element to focused state before calling this method. Or you may use [set_text](./../uielement/set_text.md) which is bound to a UI element.


**Parameters:**  
    &emsp;**text[Requried]**: str  
        &emsp;&emsp; text string to be sent.  

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium

clicknium.find_element(locator.chrome.bing.search_sb_form_q).set_focus()

clicknium.send_text("clicknium")
```