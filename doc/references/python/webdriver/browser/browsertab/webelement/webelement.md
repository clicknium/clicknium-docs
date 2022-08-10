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
- [set_property](./set_property.md): set the property value of the web element.  
- [execute_js](./execute_js.md): execute Javascript code for the target element.  
- [execute_js_file](./execute_js_file.md): execute Javascript file for the target element.  
- [scroll](./scroll.md)：scroll target element, if the element has scroll bar.


