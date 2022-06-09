# login

***def login(
        self,
        login_path: str,
        connection: str,
        client: str,
        user: str,
        password: str,
        timeout: int = 30
    ) -> None***  

Login in sap application.

**Parameters:**  
    &emsp;**login_path[Required]**: str  
        &emsp;&emsp; login path string,  login path in sap application
    &emsp;**connection[Required]**: str  
        &emsp;&emsp; connection string, sap application connection  
    &emsp;**client[Required]**: str  
        &emsp;&emsp; client string, sap application client  
    &emsp;**user[Required]**: str  
        &emsp;&emsp; user string, sap application user  
    &emsp;**password[Required]**: str  
        &emsp;&emsp; password string, sap application password  
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, Unit is second, and default value is 30 seconds. 

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc

# get sap driver
sap_driver = cc.sap

# login sap application
sap_driver.login("path", "connection", "client", "username", "password")

```