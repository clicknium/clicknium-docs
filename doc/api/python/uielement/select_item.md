# select_item
***def select_item(
        self,
        item: str,
        timeout: int = 30
    )***  

select one option for the target

**Parameters:**  
    &emsp;**item [Required]**: str   
        &emsp;&emsp; option of the dropdown control, the control support selection, such as select element in web, or combobox in desktop apllcaiton
    &emsp;**timeout**: int  
        &emsp;&emsp; Timeout for the operation. The unit of parameter is seconds. Default is set to 30 seconds.   

**Returns:**  
    &emsp;None

# TODO 
prepare the example
**Example:**
***
```python
    from clicknium import clicknium as cc, locator, ui

```