# One Level Deep

### Wait Statements

The SeleniumType library is a custom library that provides additional functionality for working with web elements and includes some wait methods that are specific to this library.

Here are some of the wait methods that are available in the SeleniumType library:


- *WaitDisabled*: This method waits for an element to become disabled.

```
Sub waitDisplayedExample()
    Dim driver As New ChromeDriver
    driver.Get "https://the-internet.herokuapp.com/dynamic_loading/2"

    'Wait for element to be visible before clicking
    driver.FindElementByXPath("//button[text()='Start']"). WaitDisplayed

    driver.FindElementByXPath("//button[text()='Start']").Click

    Application.wait (Now + TimeValue("00:00:15"))

    driver.Quit
End Sub
```

- *WaitAttribute*: This method waits for an element to have a specific attribute value.

```
Sub waitAttributeExample()
    Dim driver As New ChromeDriver
    driver.Get "https://the-internet.herokuapp.com/dynamic_loading/2"

    driver.FindElementByXPath("//button[text()='Start']").WaitDisplayed
    driver.FindElementByXPath("//button[text()='Start']").Click

    'Wait for element attribute to change
    Set elem = driver.FindElementById("start").WaitAttribute("style", "display: none;", 10000)
    Set elem = driver.FindElementById("start").WaitNotAttribute

    Application.wait (Now + TimeValue("00:00:15"))
    driver.Quit
End Sub
```

- *WaitNotAttribute*: This method waits for an element to not have a specific attribute value.
```
Sub waitNotAttributeExample()
    Dim driver As New ChromeDriver
    driver.Get "https://the-internet.herokuapp.com/dynamic_loading/2"

    driver.FindElementByXPath("//button[text()='Start']").WaitDisplayed

    driver.FindElementByXPath("//button[text()='Start']").Click
    'Wait for element attribute value to not match
    
    Set elem = driver.FindElementById("start").WaitNotAttribute("style", "", 5000)
    
    Application.wait (Now + TimeValue("00:00:15"))
    driver.Quit
End Sub
```


- *WaitCssValue*: This method waits for an element to have a specific CSS property value.
```
Sub waitCssValueExample()
    Dim driver As New ChromeDriver
    driver.Get "https://the-internet.herokuapp.com/dynamic_loading/2"

    driver.FindElementByXPath("//button[text()='Start']").WaitDisplayed
    
    driver.FindElementByXPath("//button[text()='Start']").Click
    
    'Wait for element CSS style value to change
    Set elem = driver.FindElementById("start").WaitCssValue("display", "none", 10000)
    
    Application.wait (Now + TimeValue("00:00:10"))
    driver.Quit
End Sub
```

- *WaitForScript*: This method waits for the script to complete.

```
Sub waitForScript()
    Dim driver As New ChromeDriver
    driver.Get "https://www.google.com"
    
    driver.WaitForScript "return document.readyState === 'complete'"
    
    Application.wait (Now + TimeValue("00:00:02"))
    driver.Quit
End Sub
```

- *WaitEnabled*: This method waits for an element to become enabled.

- *WaitNotElement*: This method waits for an element to not exist on the page.

- *WaitText*: This method waits for an element to have specific text.


### Mouse over
### Popups/Alerts
### Multiple tabs
### Multiple windows
### File upload