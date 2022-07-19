# WebElement

- extends: [UiElement](./../../../../../python/uielement/uielement.md) 

**WebElement class inherits from UiElement, representing the web UI element with web specific operations.**  

## Properties

- `parent`: parent element, return WebElement.  

- `children`: child elements, return list of WebElement.  

- `next_sibling`: next sibling element, return WebElement.

- `previous_sibling`: previous sibling element, return WebElement.

## Methods
- [child](./child.md)：get child element by given index.
- [set_property](./set_property.md): set web element's property value.  
- [execute_js](./execute_js.md): execute javascript code for the target element.  
- [execute_js_file](./execute_js_file.md): execute javascript file for the target element.  


