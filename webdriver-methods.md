Remote WebDriver
~~~~~~~~~~~~~~~~

**module:** selenium.webdriver.remote.webdriver

Controls a browser by sending commands to a remote server.  This
server is expected to be running the WebDriver wire protocol as
defined here: http://code.google.com/p/selenium/wiki/JsonWireProtocol

- class WebDriver(command_executor='http://127.0.0.1:4444/wd/hub',
        desired_capabilities=None, browser_profile=None)
    


  Create a new driver that will issue commands using the wire protocol.
        

  *command_executor:* Either a command.CommandExecutor object or a
  string that specifies the URL of a remote server to send commands
  to.

  *desired_capabilities:* Dictionary holding predefined values for
  starting a browser

  *browser_profile:* A
  selenium.webdriver.firefox.firefox_profile.FirefoxProfile object.
  Only used if Firefox is requested.

  Other Attributes:

  *error_handler:* errorhandler.ErrorHandler object used to verify
  that the server did not return an error.

  *session_id:* The session ID to send with every command.

  *capabilities:* A dictionary of capabilities of the underlying
  browser for this instance's session (This is set by passing
  `desired_capabilities` argument)

  
  - name

    Returns the name of the underlying browser for this instance.
        

  - start_client():

    Called before starting a new session. This method may be
    overridden to define custom startup behavior.


  - stop_client()

    Called after executing a quit command. This method may be
    overridden to define custom shutdown behavior.

::

  - start_session(desired_capabilities, browser_profile=None)

    Creates a new session with the desired capabilities.

    Args:

         - browser_name: The name of the browser to request.
         - version: Which browser version to request.
         - platform: Which platform to request the browser on.
         - javascript_enabled: Whether the new session should support JavaScript.
         - browser_profile:
           A selenium.webdriver.firefox.firefox_profile.FirefoxProfile
           object.  Only used if Firefox is requested.

            
  - create_web_element(element_id)

    Creates a web element with the specified element_id.

  - execute(driver_command, params=None)

    Sends a command to be executed by a command.CommandExecutor.

    Args:
         - driver_command: The name of the command to execute as a string.
         - params: A dictionary of named parameters to send with the command.
        
        :Returns:
          The command's JSON response loaded into a dictionary object.


  - get(url)

    Loads a web page in the current browser session.


  - title

    Returns the title of the current page.

    Usage:
            driver.title

    
  - find_element_by_id(id_)

    Finds an element by id.

    Args:
         - id\_: The id of the element to be found.
        
        :Usage:
            driver.find_element_by_id('foo')

    
  - find_elements_by_id(id_)

    Finds multiple elements by id.

    Args:
         - id\_: The id of the elements to be found.
        
        :Usage:
            driver.find_element_by_id('foo')

    
  - find_element_by_xpath(xpath)

    Finds an element by xpath.

    Args:
         - xpath: The xpath locator of the element to find.
        
        :Usage:
            driver.find_element_by_xpath('//div/td[1]')

    
  - find_elements_by_xpath(xpath)

    Finds multiple elements by xpath.

    Args:
         - xpath: The xpath locator of the elements to be found.
        
        :Usage:
            driver.find_elements_by_xpath("//div[contains(@class, 'foo')]")

    
  - find_element_by_link_text(link_text)

    Finds an element by link text.

    Args:
         - link_text: The text of the element to be found.
        
        :Usage:
            driver.find_element_by_link_text('Sign In')

    
  - find_elements_by_link_text(text)

    Finds elements by link text.

    Args:
         - link_text: The text of the elements to be found.
        
        :age:
         driver.find_elements_by_link_text('Sign In')

    
  - find_element_by_partial_link_text(link_text)

    Finds an element by a partial match of its link text.

    Args:
         - link_text: The text of the element to partially match on.
        
        :Usage:
            driver.find_element_by_partial_link_text('Sign')

    
  - find_elements_by_partial_link_text(link_text)

    Finds elements by a partial match of their link text.

    Args:
         - link_text: The text of the element to partial match on.
        
        :Usage:
            driver.find_element_by_partial_link_text('Sign')

    
  - find_element_by_name(name)

    Finds an element by name.

    Args:
         - name: The name of the element to find.
        
        :Usage:
            driver.find_element_by_name('foo')

    
  - find_elements_by_name(name)

    Finds elements by name.

    Args:
         - name: The name of the elements to find.
        
        :Usage:
            driver.find_elements_by_name('foo')

    
  - find_element_by_tag_name(name)

    Finds an element by tag name.

    Args:
         - name: The tag name of the element to find.
        
        :Usage:
            driver.find_element_by_tag_name('foo')

    
  - find_elements_by_tag_name(name)

    Finds elements by tag name.

    Args:
         - name: The tag name the use when finding elements.
        
        :Usage:
            driver.find_elements_by_tag_name('foo')

    
  - find_element_by_class_name(name)

    Finds an element by class name.

    Args:
         - name: The class name of the element to find.
        
        :Usage:
            driver.find_element_by_class_name('foo')

    
  - find_elements_by_class_name(name)

    Finds elements by class name.

    Args:
         - name: The class name of the elements to find.
        
        :Usage:
            driver.find_elements_by_class_name('foo')

    
  - find_element_by_css_selector(css_selector)

    Finds an element by css selector.

    Args:
         - css_selector: The css selector to use when finding elements.
        
        :Usage:
            driver.find_element_by_css_selector('#foo')

    
  - find_elements_by_css_selector(css_selector)

    Finds elements by css selector.

    Args:
         - css_selector: The css selector to use when finding elements.
        
        :Usage:
            driver.find_element_by_css_selector('#foo')

    
  - execute_script(script, *args)

    Synchronously Executes JavaScript in the current window/frame.
        
        :Args:
         - script: The JavaScript to execute.
         - \*args: Any applicable arguments for your JavaScript.
        
        :Usage:
            driver.execute_script('document.title')

    
  - execute_async_script(script, *args)

    Asynchronously Executes JavaScript in the current window/frame.
        
        :Args:
         - script: The JavaScript to execute.
         - \*args: Any applicable arguments for your JavaScript.
        
        :Usage:
            driver.execute_async_script('document.title')

    
  - current_url

        :Usage:
            driver.current_url


  - page_source

        :Usage:
            driver.page_source


  - close()

        Closes the current window.
        
        :Usage:
            driver.close()

    
  - quit()

        Quits the driver and closes every associated window.
        
        :Usage:
            driver.quit()


  - current_window_handle

        :Usage:
            driver.current_window_handle

    
  - window_handles

        Returns the handles of all windows within the current session.
        :Usage:
            driver.window_handles


    #Target Locators
  - switch_to_active_element()

        Returns the element with focus, or BODY if nothing has focus.
        
        :Usage:
            driver.switch_to_active_element()

    
  - switch_to_window(window_name)

        Switches focus to the specified window.
        
        :Args:
         - window_name: The name of the window to switch to.
        
        :Usage:
            driver.switch_to_window('main')

    
  - switch_to_frame(index_or_name)

        Switches focus to the specified frame, by index or name.
        
        :Args:
         - index_or_name: The name of the window to switch to, or 
           an integer representing the index to switch to.
        
        :Usage:
         - driver.switch_to_frame('frame_name')
         - driver.switch_to_frame(1)

    
  - switch_to_default_content()

        Switch focus to the default frame.
        
        :Usage:
            driver.switch_to_default_content()

    
  - switch_to_alert()

        Switches focus to an alert on the page.
        
        :Usage:
            driver.switch_to_alert()

    
    #Navigation 
  - back()

        Goes one step backward in the browser history.
        
        :Usage:
            driver.back()

    
  - forward()

        Goes one step forward in the browser history.
        
        :Usage:
            driver.forward()

    
  - refresh()

        Refreshes the current page.
        
        :Usage:
            driver.refresh()

    
    # Options
  - get_cookies()

        Returns a set of dictionaries, corresponding to cookies visible in the 
        current session.
        
        :Usage:
            driver.get_cookies()


    
  - get_cookie(name)

        Get a single cookie by name. Returns the cookie if found, None if not.
        
        :Usage:
            driver.get_cookie('my_cookie')

    
  - delete_cookie(name)

        Usage:
            driver.delete_cookie('my_cookie')

    
  - delete_all_cookies()

        Delete all cookies in the scope of the session.
        Usage:
            driver.delete_all_cookies()

    
  - add_cookie(cookie_dict)

        Adds a cookie to your current session.
        Args:
            cookie_dict: A dictionary object, with the desired cookie name as the key, and
            the value being the desired contents.
        Usage:
            driver.add_cookie({'foo': 'bar',})


    
    # Timeouts
  - implicitly_wait(time_to_wait)

        Sets a sticky timeout to implicitly wait for an element to be found, 
        or a command to complete. This method only needs to be called one time per session.
        Args:
            time_to_wait: Amount of time to wait
        Usage:
            driver.implicitly_wait(30)

    
  - set_script_timeout(time_to_wait)

        Set the amount of time that the script should wait before throwing an
           error.
        Args:
            time_to_wait: The amount of time to wait
        Usage:
            driver.set_script_timeout(30)

    
  - find_element(by=By.ID, value=None)

        'Private' method used by the find_element_by_* methods.
        Usage:
            Use the corresponding find_element_by_* instead of this.

    
  - find_elements(by=By.ID, value=None)

        'Private' method used by the find_elements_by_* methods.
        Usage:
            Use the corresponding find_elements_by_* instead of this.


  - desired_capabilities

         returns the drivers current desired capabilities being used

    
  - get_screenshot_as_file(filename)

        Gets the screenshot of the current window. Returns False if there is 
        any IOError, else returns True. Use full paths in your filename.
        Args:
            filename: The full path you wish to save your screenshot to.
        Usage:
            driver.get_screenshot_as_file('/Screenshots/foo.png')

    
  - get_screenshot_as_base64()

    Gets the screenshot of the current window as a base64 encoded
    string which is useful in embedded images in HTML.
        
        :Usage:
            driver.get_screenshot_as_base64()
