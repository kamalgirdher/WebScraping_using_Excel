# VBA Refresher

### SubProcedures & Functions

**What is Sub-procedure?**
A sub-procedure is set of statements that perform action(s) but do not return a value. A function on the other hand does the same thing, but returns a value.

A sub-procedure is always enclosed between **Sub** and **End Sub**.

```
Sub test()
' set of statements
End Sub
```

And a function starts with **Function** and ends with **End Function**

```
Function test(*arguments*)
' set of statements
test=*<return value>*
End Sub
```

If you are just starting with VBA, I would suggest to watch & follow my youtube channel to learn VBA basics before moving ahead with this course.

<a href="https://www.youtube.com/c/xtremeexcel?sub_confirmation=1"><img src="https://github.com/kamalgirdher/WebScraping_using_Excel/blob/main/images/subscribe.png"></a>

**Playlist:** [Excel VBA(macros) Step by Step](https://www.youtube.com/watch?v=hPrfOYBDGs8&list=PL1R_HJw0CDYIXDfzAR_fVUPfiB35okm93)

To learn **ONLY** about functions and subprocedures, [watch this tutorial](PL1R_HJw0CDYIXDfzAR_fVUPfiB35okm93).



### Variables and Objects


##### Variables

In any programming language, a variable is a value that can change, depending on conditions or on information passed to the program. It also provide a way of labeling data.

In VBA, Variables can be declared as one of the following data types: Boolean, Byte, Integer, Long, Currency, Single, Double, Date, String (for variable-length strings), String * length (for fixed-length strings), Object, or Variant. If you don't specify a data type, the **Variant** data type is assigned by default


```
Dim a As Integer
Dim b As String
Dim c

a=10
b="Kamal"
c=100
```
A variable name in vba need to follow these rules,

- It must be less than 255 characters
- No spacing is allowed
- It must not begin with a number
- Period is not permitted

To learn more about variable, [watch this video](https://www.youtube.com/watch?v=33JmyY83IpA&list=PL1R_HJw0CDYIXDfzAR_fVUPfiB35okm93&index=3).


##### Objects

In VBA, an object represents instance of an application, such as a worksheet, a cell, a chart, a form, or a report. In Visual Basic code, you must identify an object before you can apply one of the object's methods or change the value of one of its properties.

A collection is an object that contains several other objects, usually, but not always, of the same type. In Microsoft Excel, for example, the Workbooks object contains all the open Workbook objects. In Visual Basic, the Forms collection contains all the Form objects in an application.

```
Sub test()

'Declaration goes like this
Dim wb as Workbook
'Initialization goes like this
Set wb = ActiveWorkbook


Dim olapp as Outlook.application
Set olapp = new Outlook.Application

Dim wdApp as Word.Application
Set wdApp = new Word.Application

Dim ie as InternetExplorer
Set ie = new InternetExplorer

' If we do not know the object type initially, we can keep it as variant.
Dim x

End Sub
```

If this is unclear, do not worry. We will be creating objects of selenium webdriver and see the usage in detail.


### Conditional statements