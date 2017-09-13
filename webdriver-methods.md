WebDriver Method Summary
---

| Method Name  | Description  | Args  |  Usage |
|---|---|---|---|
| name  | Returns the name of the underlying browser for this instance  |   |   |
| start_client()  |  Called before starting a new session. This method may be overridden to define custom startup behavior |   | driver.start_client()  |
| stop_client  | Called after executing a quit command. This method may be overridden to define custom shutdown behavior. |   | driver.stop_client()  |
| start_session | Creates a new session with the desired capabilities. | a. browser_name: The name of the browser to request b. version: Which browser version to request c. platform: Which platform to request the browser on. d.javascript_enabled: Whether the new session should support JavaScript e. browser_profile:A selenium.webdriver.firefox.firefox_profile.FirefoxProfile  object.  Only used if Firefox is requested. | driver.start_session(desired_capabilities, browser_profile=None)  |
| create_web_element  | Creates a web element with the specified element_id.  |   | create_web_element(element_id)  |
| execute  |  Sends a command to be executed by a command.CommandExecutor. | a. driver_command: The name of the command to execute as a string. b. params: A dictionary of named parameters to send with the command. | execute(driver_command, params=None)   # Returns command's JSON response loaded into a dictionary object|
| get  | Loads a web page in the current browser session.  |   | driver.get(url)  |
| title  | Returns the title of the current page.  |   | driver.title  |
| find_element_by_id  | Finds an element by id.  | id\_: The id of the element to be found.  | driver.find_element_by_id('foo')  |
| find_elements_by_id  | Finds all element by id.  | id\_: The element with similar id's to be found.  | driver.find_elements_by_id('foo')  |
| find_element_by_xpath  | Finds an element by xapth.  | xpath: The xpath locator of the element to find.  | driver.find_element_by_xpath('//div/td[1]')  |
| find_elements_by_xpath  | Finds all elements by xapth.  | xpath: The xpath locator of the element to find.  | driver.find_elements_by_xpath('//div/td[1]')  |
| find_element_by_link_text  | Finds an element by link text.  | link_text: The text of the element to be found.  | driver.find_element_by_link_text('Sign In')  |
| find_elements_by_link_text  | Finds all elements by link text.  | link_text: The text of the element to be found.  | driver.find_elements_by_link_text('Sign In')  |
| find_element_by_partial_link_text  | Finds an element by a partial match of its link text  | link_text: The text of the element to be found.  | driver.find_element_by_partial_link_text(Sign)  |
| find_elements_by_partial_link_text  | Finds all elements by a partial match of its link text  | link_text: The text of the element to be found.  | driver.find_elements_by_partial_link_text(Sign)  |
| find_element_by_name  | finds an element by name.  | name: The name of the element to find  | driver.find_element_by_name('foo')  |
| find_elements_by_name  | finds all elements by name.  | name: The name of the element to find | driver.find_elements_by_name('foo')  |
| find_element_by_tag_name  | Finds an element by tag name. | name: The name of the element to find | driver.find_element_by_tag_name(name)  |
| find_elements_by_tag_name  | Finds all elements by tag name. | name: The name of the element to find | driver.find_elements_by_tag_name(name)  |
| find_element_by_class_name  |  Finds an element by class name. | name: The class name of the element to find | driver.find_element_by_class_name(name)  |
| find_elements_by_class_name  |  Finds an element by class name. | name: The class name of the element to find | driver.find_elements_by_class_name(name)  |
| find_element_by_css_selector  |  Finds an element by css selector. | css_selector: The css selector to use when finding elements. | driver.find_element_by_css_selector(css_selector)  |
| find_elements_by_css_selector  |  Finds all elements by css selector. | css_selector: The css selector to use when finding elements. | driver.find_elements_by_css_selector('#foo')  |
| execute_script  |  Synchronously Executes JavaScript in the current window/frame. | script: The JavaScript to execute,args: Any applicable arguments for your JavaScript . | driver.execute_script('document.title') |
| execute_async_script  |  Asynchronously Executes JavaScript in the current window/frame. | script: The JavaScript to execute,args: Any applicable arguments for your JavaScript . | driver.execute_async_script('document.title') |
| current_url  |  Displays the HTML title of window |  | driver.current_url |
| page_source  |  Displays the HTML source of window |  | driver.page_source |
| close  |  Closes the current window. |  | driver.close() |
| quit  |  Quits the driver and closes every associated window. |  | driver.quit() |
| current_window_handle  |   |  | driver.current_window_handle |
| window_handles  | Returns the handles of all windows within the current session.  |  | driver.window_handles |
| find_element  | 'Private' method used by the find_element_by_* methods.  |  | find_element(by=By.ID, value=None) |
| find_elements  | 'Private' method used by the find_elements_by_* methods.  |  | find_element(by=By.ID, value=None) |

---

# Target Locators

| Method Name  | Description  | Args  |  Usage |
|---|---|---|---|
| switch_to_active_element  | Returns the element with focus, or BODY if nothing has focus.  |   | driver.switch_to_active_element()  |
| switch_to_window  | Switches focus to the specified window  |window_name: The name of the window to switch to.  | driver.switch_to_window(main) |
| switch_to_frame  | Switches focus to the specified frame, by index or name.  |index_or_name: The name of the window to switch to, or an integer representing the index to switch to.  | driver.switch_to_frame(1) or driver.switch_to_frame('frame_name') |
| switch_to_default_content  | Switch focus to the default frame.  |  | driver.switch_to_default_content() |
| switch_to_alert  |  Switches focus to an alert on the page.  |  | driver.switch_to_alert() |

---


# Navigation

| Method Name  | Description  | Args  |  Usage |
|---|---|---|---|
| back  | Goes one step backward in the browser history.  |   | driver.back()  |
| forward  | Goes one step forward in the browser history.  |   | driver.forward()  |
| refresh  | Refreshes the current page.  |   | driver.refresh()  |
| refresh  | Refreshes the current page.  |   | driver.refresh()  |

---

# Options

| Method Name  | Description  | Args  |  Usage |
|---|---|---|---|
| get_cookies  | Returns a set of dictionaries, corresponding to cookies visible in the current session.  |   | driver.get_cookies() |
| get_cookie  | Get a single cookie by name. Returns the cookie if found, None if not.  |   | driver.get_cookie('my_cookie') |
| delete_cookie  | Deletes the cookie by name  |   | driver.delete_cookie('my_cookie') |
| delete_all_cookies  | Delete all cookies in the scope of the session. |   | driver.delete_all_cookies() |
| add_cookie  | Adds a cookie to your current session.. | cookie_dict: A dictionary object, with the desired cookie name as the key, and the value being the desired contents.   | driver.add_cookie({'foo': 'bar',}) |

---

# Timeouts
| Method Name  | Description  | Args  |  Usage |
|---|---|---|---|
| implicitly_wait  | Sets a sticky timeout to implicitly wait for an element to be found,or a command to complete. This method only needs to be called one time per session. | time_to_wait: Amount of time to wait  | driver.implicitly_wait(30) |
| implicitly_wait  | Sets a sticky timeout to implicitly wait for an element to be found,or a command to complete. This method only needs to be called one time per session. | time_to_wait: Amount of time to wait  | driver.implicitly_wait(30) |
| set_script_timeout  | Set the amount of time that the script should wait before throwing an error | time_to_wait: Amount of time to wait  | driver.set_script_timeout(30) |
| desired_capabilities  | returns the drivers current desired capabilities being used |   | driver.desired_capabilities |
| get_screenshot_as_file  | Gets the screenshot of the current window. Returns False if there is any IOError, else returns True. Use full paths in your filename | filename: The full path you wish to save your screenshot to.  | driver.get_screenshot_as_file('/Screenshots/foo.png') |
| get_screenshot_as_base64  | Gets the screenshot of the current window as a base64 encoded string which is useful in embedded images in HTML. |   | driver.get_screenshot_as_base64() |

---
