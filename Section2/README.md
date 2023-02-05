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

**VBA Complete Course** [Excel VBA(macros) Step by Step](https://www.youtube.com/watch?v=hPrfOYBDGs8&list=PL1R_HJw0CDYIXDfzAR_fVUPfiB35okm93)

To learn **ONLY** about functions and subprocedures, [watch this tutorial](PL1R_HJw0CDYIXDfzAR_fVUPfiB35okm93).

### Variables and Objects

##### Variables

In any programming language, a variable is a value that can change, depending on conditions or on information passed to the program. It also provide a way of labeling data.

In VBA, Variables can be declared as one of the following data types: Boolean, Byte, Integer, Long, Currency, Single, Double, Date, String (for variable-length strings), String \* length (for fixed-length strings), Object, or Variant. If you don't specify a data type, the **Variant** data type is assigned by default

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

You may also [watch this tutorial.](https://www.youtube.com/watch?v=cPcNs5dlGPs&list=PL1R_HJw0CDYKYzExtZfhKZRddhwv5i-rg&index=3)

### Conditional statements

In VBA we have 2 conditional statements:

- If .. Else .. End If
- Select Case

Both of these evaluate one or more conditions and, depending on the result, execute specific sections of code.

##### If ... Then Statement

The If ... Then statement tests a condition and if it evaluates to True, executes a specific section of code. If the condition evaluates to False, a different section of code is executed.

```
If Condition1 Then
    ' Execute something
ElseIf Condition2 Then
    ' Execute something else
.
.
.
Else
    ' Execute something if above conditions are not true
End If
```

For example:

```
If ActiveCell.Value < 40 Then
    ActiveCell.offset(0,1).value="Fail"
ElseIf ActiveCell.Value < 80 Then
    ActiveCell.offset(0,1).value="Pass"
Else
    ActiveCell.offset(0,1).value="OUSTANDING"
End If
```

[Watch Tutorial](https://www.youtube.com/watch?v=QNosohYSNzE&list=PL1R_HJw0CDYIXDfzAR_fVUPfiB35okm93&index=5)

If you want to see some examples using these conditional statements then these are good to start.

[Largest of 2 numbers](https://www.youtube.com/watch?v=eFTOTMP0rYQ&list=PL1R_HJw0CDYIXDfzAR_fVUPfiB35okm93&index=6)

[Largest of 3 numbers](https://www.youtube.com/watch?v=Mj2eOqTyhS8&list=PL1R_HJw0CDYIXDfzAR_fVUPfiB35okm93&index=7)

##### Select Case Statement

The Select Case statement is similar to the If ... Then statement, in that it tests an expression, and executes different sections of code, depending on the value of the expression.

```
Sub test()
dayIndex = Weekday(Date)

Select Case dayIndex
    Case 1
        MsgBox "Sunday"
    Case 2
        MsgBox "Monday"
    Case 3
        MsgBox "Tuesday"
    Case 4
        MsgBox "Wednesday"
    Case 5
        MsgBox "Thursday"
    Case 6
        MsgBox "Friday"
    Case 7
        MsgBox "Saturday"
    Case Else
        MsgBox "Invalid"
End Select

End Sub
```
[Watch Complete Tutorial](https://www.youtube.com/watch?v=SS5Wdd_ER2U&list=PL1R_HJw0CDYIXDfzAR_fVUPfiB35okm93&index=8)



### Loop statements

Loops are one of the most powerful programming tools in VBA, and they allow users to repeat the same code block multiple times until a specific point is attained or a given condition is met. 

[Watch Loop Statements Complete Tutorial](https://www.youtube.com/watch?v=-D5KJiqIcjc&list=PL1R_HJw0CDYIXDfzAR_fVUPfiB35okm93&index=16)

[Watch - Loops in 1d](https://www.youtube.com/watch?v=nvlz7MyblQU&list=PL1R_HJw0CDYIXDfzAR_fVUPfiB35okm93&index=17)

[Watch - Loops in 2d](https://www.youtube.com/watch?v=TJXDkBmjSmE&list=PL1R_HJw0CDYIXDfzAR_fVUPfiB35okm93&index=18)

[Watch - While..Wend Loop Tutorial](https://www.youtube.com/watch?v=ctPlFpjgluw&list=PL1R_HJw0CDYIXDfzAR_fVUPfiB35okm93&index=20)

[Watch - Do... While Loop Tutorial](https://www.youtube.com/watch?v=4OhDQXiyD1w&list=PL1R_HJw0CDYIXDfzAR_fVUPfiB35okm93&index=21)

[Watch - Do...Until loop Tutorial](https://www.youtube.com/watch?v=mXY5P2c8KU0&list=PL1R_HJw0CDYIXDfzAR_fVUPfiB35okm93&index=23)


### String Operations

Irrespective of what data scraping technique we are using, we always need some pre and post processing of data to get it in clean format(the way we are expecting). String operations therefore play a key role in data scraping.

To learn string functions, [watch this tutorial.](https://youtu.be/TqQZHAlb5BE)

You may [watch various String manipulation functions and techniques here.](https://www.youtube.com/watch?v=fM0dRsPSjf4&list=PL1R_HJw0CDYKYzExtZfhKZRddhwv5i-rg&index=6)


<a href="https://www.youtube.com/c/xtremeexcel?sub_confirmation=1"><img src="https://github.com/kamalgirdher/WebScraping_using_Excel/blob/main/images/subscribe.png"></a>
