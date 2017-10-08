
**module:** selenium.webdriver.common.action_chains

---

| Method Name  | Description  | Args  |  Usage |
|---|---|---|---|
| perform  | Performs all stored actions  |   | perform() |
| Click  | Clicks an element.  | *on_element:* The element to click.  If None, clicks on current  mouse position.  | click(on_element=None) |
| click_and_hold | Holds down the left mouse button on an element. | *on_element:* The element to mouse down.  If None, clicks on current mouse position. | click_and_hold(on_element) |
| context_click(Right Click) | Performs a context-click (right click) on an element. | *on_element:* The element to context-click.  If None, clicks on current mouse position. | context_click(on_element) |
|double_click | Double-clicks an element. | *on_element:* The element to double-click.  If None, clicks on current mouse position. | double_click(on_element) |
| drag_and_drop | Holds down the left mouse button on the source element, then moves to the target element and releases the mouse button. | *source:* The element to mouse down. *target:* The element to mouse up. | drag_and_drop(source, target) |
| key_down | Sends a key press only, without releasing it.  Should only be used with modifier keys (Control, Alt and Shift). | *key:* The modifier key to send. Values are defined in Keys class. *element:* The element to send keys.  If None, sends a key to     current focused element. | key_down(key, element=None) |
| key_up | Releases a modifier key. | *key:* The modifier key to send. Values are defined in Keys class. *element:* The element to send keys.  If None, sends a key to current focused element.
 | key_up(key, element=None) |
| move_by_offset | Moving the mouse to an offset from current mouse position. | *xoffset:* X offset to move to. *yoffset:* Y offset to move to. | move_by_offset(xoffset, yoffset) |
| move_to_element | Moving the mouse to the middle of an element. | *to_element:* The element to move to. |  move_to_element(to_element) |
| move_to_element_with_offset | Move the mouse by an offset of the specificed element. Offsets are relative to the top-left corner of the element. | *to_element:* The element to move to. *xoffset:* X offset to move to. *yoffset:* Y offset to move to. | move_to_element_with_offset(to_element, xoffset, yoffset) |
| release | Releasing a held mouse button. |  *on_element:* The element to mouse up. | release(on_element) |
| Send_keys | Sends keys to current focused element. | *keys_to_send:* The keys to send. |  Send_keys(`*keys_to_send`) |
| Send_keys_to_element | Sends keys to an element. | *element:* The element to send keys. *keys_to_send:* The keys to send. |  Send_keys_to_element(self, element, `*keys_to_send`): |
