# uninstall

***def uninstall(self, java_install_path: str = '') -> None*** 

Uninstall java extension.

**Parameters:**  
    &emsp;**java_install_path**: str  
        &emsp;&emsp; The java installation path, like "C:\\Program Files\\Java\\jdk-17.0.2\\bin". The system will try to find it under "Program Files && Program Files (x86)" if this parameter is not specified.

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc

# uninstall java extension with default java installation path "Program Files && Program Files (x86)"
cc.java.extension.uninstall()

# uninstall java extension with specified java installation path
cc.java.extension.uninstall(java_install_path = "C:\\Program Files\\Java\\jdk-17.0.2\\bin")

```