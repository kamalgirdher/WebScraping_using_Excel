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
You can try rest of these yourself. Feel free to ask questions on Youtube if something doesn't work for you!

- *WaitEnabled*: This method waits for an element to become enabled.

- *WaitNotElement*: This method waits for an element to not exist on the page.

- *WaitText*: This method waits for an element to have specific text.

### Alerts
In Selenium Type Library for VBA, you can handle alerts using the SwitchToAlert method, which returns an Alert object representing the currently active alert dialog. Once you have the Alert object, you can use methods like Accept, Dismiss, and SendKeys to interact with the alert. For example:

```
Sub InfoAlert()
    Dim driver As New ChromeDriver
    driver.Get "https://the-internet.herokuapp.com/javascript_alerts"

    ' Click on a link that opens a popup
    driver.FindElementByXPath("//button[contains(text(),'Click for JS Alert')]").Click
    
    ' Switch to the alert and accept or dismiss it
    Set Alert = driver.SwitchToAlert
    
    Alert.Accept ' Clicks "OK"
    
    Application.wait (Now + TimeValue("00:00:05"))

    driver.Quit
End Sub


Sub ConfirmAlert()
    Dim driver As New ChromeDriver
    driver.Get "https://the-internet.herokuapp.com/javascript_alerts"

    ' Click on a link that opens a popup
    driver.FindElementByXPath("//button[contains(text(),'Click for JS Confirm')]").Click
    
    ' Switch to the alert and accept or dismiss it
    Set Alert = driver.SwitchToAlert
    
    Alert.Accept ' Clicks "OK"
    'Alert.Dismiss ' Clicks "Cancel
    
    Application.wait (Now + TimeValue("00:00:05"))

    driver.Quit
End Sub



Sub PromptAlert()
    Dim driver As New ChromeDriver
    driver.Get "https://the-internet.herokuapp.com/javascript_alerts"

    ' Click on a link that opens a popup
    driver.FindElementByXPath("//button[contains(text(),'Click for JS Prompt')]").Click
    
    ' Switch to the alert and accept or dismiss it
    Set Alert = driver.SwitchToAlert
    Alert.SendKeys "XtremeExcel"
    
    Application.wait (Now + TimeValue("00:00:03"))
    
    'To accept the alert
    Alert.Accept
    
    Application.wait (Now + TimeValue("00:00:05"))

    driver.Quit
End Sub

```


### Multiple windows and tabs

In Selenium Type Library for VBA, you can handle multiple windows using the SwitchToWindow method. This method allows you to switch between windows by specifying either the window handle or the window title. Once you switch to a window, you can perform any actions you need to on that window, and then switch back to the original window when you're done.

```
Sub newWindow()
Dim driver As New ChromeDriver

driver.Get "https://nxtgenaiacademy.com/multiplewindows/"

driver.FindElementByName("newbrowserwindow123").Click

'Switch to new window
driver.SwitchToNextWindow

'Print New window top bar text on console
Debug.Print driver.FindElementByCss("ul.top_bar_info>li").Text

'Close opened window
driver.Close

Application.wait (Now + TimeValue("00:00:03"))

'Switch to main window
driver.SwitchToPreviousWindow

Application.wait (Now + TimeValue("00:00:05"))

driver.Quit
End Sub



Sub newTab()
Dim driver As New ChromeDriver

driver.Get "https://nxtgenaiacademy.com/multiplewindows/"

driver.FindElementByName("145newbrowsertab234").Click

'Switch to new window
driver.SwitchToNextWindow

'Print New window top bar text on console
Debug.Print driver.FindElementByCss("ul.top_bar_info>li").Text

'Close opened window
driver.Close

Application.wait (Now + TimeValue("00:00:03"))

'Switch to main window
driver.SwitchToPreviousWindow

Application.wait (Now + TimeValue("00:00:05"))

driver.Quit
End Sub

```

### Frames

In Selenium Type Library for VBA, you can handle frames using the SwitchToFrame method. This method allows you to switch to a particular frame on a webpage by specifying either the frame element or the frame index. Once you switch to a frame, you can interact with the elements inside the frame as if they were part of the main webpage. To switch back to the default content (i.e., the main webpage), you can use SwitchTo.DefaultContent.

```
Sub HandlingFrame()
    Dim driver As New ChromeDriver

    driver.Get "https://the-internet.herokuapp.com/iframe"

    'Switch to frame
    driver.SwitchToFrame ("mce_0_ifr")

    'Print text from element inside frame
    MsgBox driver.FindElementByCss("body p").Text

    Application.wait (Now + TimeValue("00:00:05"))

    driver.Quit
End Sub
```