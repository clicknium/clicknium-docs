---
sidebar_position: 2
sidebar_label: uninstall
---

# clicknium.java.uninstall

```python 
def uninstall(self, java_install_path: str = '') -> None
```

Uninstall Java extension.

**Parameters:**  
    &emsp;**java_install_path**: str  
        &emsp;&emsp; The Java installation path, like "C:\\Program Files\\Java\\jdk-17.0.2". The system will try to find it under "Program Files && Program Files (x86)" if this parameter is not specified.

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc

# uninstall Java extension with default java installation path "Program Files && Program Files (x86)"
cc.java.extension.uninstall()

# uninstall Java extension with specified java installation path
cc.java.extension.uninstall(java_install_path = "C:\\Program Files\\Java\\jdk-17.0.2")

```