---
sidebar_position: 1
sidebar_label: install
---

# clicknium.java.install

```python
def install(self, java_install_path: str = '') -> None
```

Install Java extension.

>**Remarks:**  
>- Make sure you have installed JRE or JDK.

**Parameters:**  
    &emsp;**java_install_path**: str  
        &emsp;&emsp; The Java installation path, like "C:\\Program Files\\Java\\jdk-17.0.2". The system will try to find it under "Program Files && Program Files (x86)" if this parameter is not specified.

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc

# install Java extension with default Java installation path "Program Files && Program Files (x86)"
cc.java.extension.install()

# install Java extension with customized Java installation path
cc.java.extension.install(java_install_path = "C:\\Program Files\\Java\\jdk-17.0.2")

```