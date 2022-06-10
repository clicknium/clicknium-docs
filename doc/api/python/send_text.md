# clicknium.send_text
***def send_text(
        self,
        text: str
    ) -> None***  

Send text to current cursor's position.

**Parameters:**  
    &emsp;**text[Requried]**: str  
        &emsp;&emsp; text string is to be input  

**Returns:**  
    &emsp;None

**Example:**
***
```python
    from clicknium import clicknium

    clicknium.send_text("clicknium")
```