---
sidebar_position: 9
---
# clicknium.scrape_data  

***def scrape_data(
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        next_page_button_locator: Union[_Locator, str] = None,
        next_page_button_locator_variables: dict = {},
        next_page_button_by: Union[Literal["default", "mouse-emulation", "control-invocation"], MouseActionBy] = MouseActionBy.Default,
        wait_page_load_time: int = 5,
        max_count: int = -1,
        timeout: int = 30
    ) -> object***  


 Scrape data from applications.

**Parameters:**  
    &emsp;**locator[Required]**: Union[_Locator, str]   
        &emsp;&emsp; The visit path of locator for target UI element, eg: 'locator.chrome.bing.table'.  
    &emsp;**locator_variables**: dict = {}     
        &emsp;&emsp; Set to initialize parameters in locator, eg: { "row": 1,  "column": 1}, more about variable, please refer to https://www.clicknium.com/documents/concepts/locator#parametric-locator    
    &emsp;**next_page_button_locator**: Union[_Locator, str] = None       
        &emsp;&emsp; The visit path of locator for goto next page UI element. If it's None, means just extract the current page data.      
    &emsp;**next_page_button_locator_variables**: dict = {}  
        &emsp;&emsp; Set to initialize parameters in next_page_button_locator.  
    &emsp;**next_page_button_by**:  Union[Literal["default", "mouse-emulation", "control-invocation"], MouseActionBy] = MouseActionBy.Default  
        &emsp;&emsp; Defines the method to click the UI element.  
        &emsp;&emsp;&emsp;&emsp; mouse-emulation: click the target UI element by simulating mouse.  
        &emsp;&emsp;&emsp;&emsp; control-invocation: click the target UI element by invoking its UI method. It may not be supported if it is a Windows desktop element.  
        &emsp;&emsp;&emsp;&emsp; default: automatically choose method per element type. For Web element, use `control-invocation`; for Window element, use `mouse-emulation`.  
    &emsp;**wait_page_load_time**: int = 5   
        &emsp;&emsp; Time to wait for the next page to load, the unit is second. If the value less than 0, use 0.  
    &emsp;**max_count**: Uint = -1   
        &emsp;&emsp; Maximum number of extracte data items. default value is -1. If the value less than 0, means extract all data until the last page.   
    &emsp;**timeout**: int = 30  
        &emsp;&emsp; Timeout for the operation to find the 'locator' UI element, the unit is second, and default value is 30 seconds. 

**Returns:**  
    &emsp;The Json object of extracted data

**Example:**
***
```python
from clicknium import clicknium as cc
import pandas as pd

rowdata = cc.scrape_data(locator.sample)
df = pd.json_normalize(rowdata)
print(df)

```