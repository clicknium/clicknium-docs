# UiElement <!-- {docsify-ignore-all} -->
**UiElement class provides common operations for web and window's UiElement.**  

## properties

- `parent`   
    parent element, return UiElement

- `children`  
    children elements, return list of UiElement

- `next_sibling`  
    next sibling element

- `previous_sibling`  
    previous sibling element

## methods
- [child](/doc/api/python/uielement/child.md)：get child element with index
- [click](/doc/api/python/uielement/click.md)：single click the target element
- [double_click](/doc/api/python/uielement/double_click.md)：double click the target element
- [mouse_up](/doc/api/python/uielement/mouse_up.md)：mouse up on the element
- [mouse_down](/doc/api/python/uielement/mouse_down.md)：mouse down on the element
- [drag_drop](/doc/api/python/uielement/drag_drop.md): hold down the left mouse button on the source element, then move to the target offset and release the mouse button
- [get_position](/doc/api/python/uielement/get_position.md): get the position of the element
- [get_property](/doc/api/python/uielement/get_property.md): get property value of the element
- [wait_property](./doc/api/python/uielement/wait_property.md): wait for the element's value of specified property to be the same as expected
- [get_size](/doc/api/python/uielement/get_size.md): get the size(height and width) of the element
- [set_text](/doc/api/python/uielement/set_text.md): set text for the target element
- [get_text](/doc/api/python/uielement/get_text.md): get text of the element
- [clear_text](/doc/api/python/uielement/clear_text.md): clear text of the element
- [highlight](/doc/api/python/uielement/highlight.md): highlight the element with specified color
- [hover](/doc/api/python/uielement/hover.md): hover over the element, and the mouse will move upon the element for a while
- [save_to_image](/doc/api/python/uielement/save_to_image.md): save target element's screenshot to file with the specified size and offset
- [select_item](/doc/api/python/uielement/select_item.md): select one option for the target element
- [select_items](/doc/api/python/uielement/select_items.md): select multiple options for the target element
- [send_hotkey](/doc/api/python/uielement/send_hotkey.md): send hotkey based on target element
- [set_checkbox](/doc/api/python/uielement/set_checkbox.md): check operation on the target element
- [set_focus](/doc/api/python/uielement/set_focus.md): set focus for the target element
