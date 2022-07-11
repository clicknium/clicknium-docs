# UiElement 
**UiElement class represents a web or window UI element with common automation operations.**  

## Properties

- `parent`: parent element, return UiElement.
- `children`: child elements, return list of UiElement.
- `next_sibling`: next sibling element.
- `previous_sibling`: previous sibling element.

## Methods
- [child](./child.md)：get child element by given index.
- [clear_text](./clear_text.md): clear text of the target element.
- [click](./click.md)：single click the target element.
- [double_click](./double_click.md)：double click the target element.
- [drag_drop](./drag_drop.md): hold down the left mouse button on the source element, then move to the target offset and release the mouse button.
- [get_position](./get_position.md): get position of the target element.
- [get_property](./get_property.md): get property value of the target element.  
- [get_size](./get_size.md): get the size(height and width) of the target element.
- [get_text](./get_text.md): get text of the target element。
- [highlight](./highlight.md): highlight the target element.
- [hover](./hover.md): hover over the element, and the mouse will move upon the element and stay for a while.
- [mouse_down](./mouse_down.md)：mouse button down on the target element.
- [mouse_up](./mouse_up.md)：mouse button up on the target element.
- [save_to_image](./save_to_image.md): save target element's screenshot to file with the specified size and offset.
- [select_item](./select_item.md): select one option for the target element when it is a dropdown type control.
- [select_items](./select_items.md): select multiple options for the target element that can support multiple selections.
- [send_hotkey](./send_hotkey.md): send hotkey to target element.
- [set_checkbox](./set_checkbox.md): set check state for a checkbox control.
- [set_focus](./set_focus.md): set the target element to focused state.
- [set_text](./set_text.md): set text for the target element.
- [wait_property](./wait_property.md): wait for the element's value of specified property to be the same as expected