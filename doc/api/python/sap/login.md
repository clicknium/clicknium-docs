# clicknium.sap.login

***def login(
        self,
        login_path: str,
        connection: str,
        client: str,
        user: str,
        password: str,
        timeout: int = 30
    ) -> None***  

Login to the SAP application.

**Parameters:**  
    &emsp;**login_path[Required]**: str  
        &emsp;&emsp; login path string,  login path in SAP application.
    &emsp;**connection[Required]**: str  
        &emsp;&emsp; connection string, SAP application connection.
    &emsp;**client[Required]**: str  
        &emsp;&emsp; client string, SAP application client.
    &emsp;**user[Required]**: str  
        &emsp;&emsp; user string, SAP application user.
    &emsp;**password[Required]**: str  
        &emsp;&emsp; password string, SAP application password.
    &emsp;**timeout**: int  
        &emsp;&emsp; timeout for the operation, the unit is second, and the default value is 30 seconds.

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc

# login sap application
cc.sap.login("path", "connection", "client", "username", "password")

```