# install

***def install(self, java_install_path: str = '') -> None*** 

Install Java extension.

>**Remarks:**  
>- Make sure you have installed Java or JRE.

**Parameters:**  
    &emsp;**java_install_path**: str  
        &emsp;&emsp; The Java installation path, like "C:\\Program Files\\Java\\jdk-17.0.2\\bin". The system will try to find it under "Program Files && Program Files (x86)" if this parameter is not specified.

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc

# install java extension with default java installation path "Program Files && Program Files (x86)"
cc.java.extension.install()

# install java extension with customized java installation path
cc.java.extension.install(java_install_path = "C:\\Program Files\\Java\\jdk-17.0.2\\bin")

```