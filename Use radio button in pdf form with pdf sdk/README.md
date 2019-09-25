## How to use radio button in pdf form with pdf sdk in VBScript and ByteScout PDF Suite

### Step-by-step tutorial on how to use radio button in pdf form with pdf sdk in VBScript

Use radio button in pdf form with pdf sdk is simple to apply in VBScript if you use these source codes below. ByteScout PDF Suite: the bundle that provides six different SDK libraries to work with PDF from generating rich PDF reports to extracting data from PDF documents and converting them to HTML. This bundle includes PDF (Generator) SDK, PDF Renderer SDK, PDF Extractor SDK, PDF to HTML SDK, PDF Viewer SDK and PDF Generator SDK for Javascript. It can use radio button in pdf form with pdf sdk in VBScript.

Want to save time? You will save a lot of time on writing and testing code as you may just take the VBScript code from ByteScout PDF Suite for use radio button in pdf form with pdf sdk below and use it in your application. Just copy and paste the code into your VBScript application’s code and follow the instructions. Check VBScript sample code samples to see if they respond to your needs and requirements for the project.

The trial version of ByteScout PDF Suite can be downloaded for free from our website. It also includes source code samples for VBScript and other programming languages.

## REQUEST FREE TECH SUPPORT

[Click here to get in touch](https://bytescout.zendesk.com/hc/en-us/requests/new?subject=ByteScout%20PDF%20Suite%20Question)

or just send email to [support@bytescout.com](mailto:support@bytescout.com?subject=ByteScout%20PDF%20Suite%20Question) 

## ON-PREMISE OFFLINE SDK 

[Get Your 60 Day Free Trial](https://bytescout.com/download/web-installer?utm_source=github-readme)
[Explore SDK Docs](https://bytescout.com/documentation/index.html?utm_source=github-readme)
[Sign Up For Online Training](https://academy.bytescout.com/)


## ON-DEMAND REST WEB API

[Get your API key](https://pdf.co/documentation/api?utm_source=github-readme)
[Explore Web API Documentation](https://pdf.co/documentation/api?utm_source=github-readme)
[Explore Web API Samples](https://github.com/bytescout/ByteScout-SDK-SourceCode/tree/master/PDF.co%20Web%20API)

## VIDEO REVIEW

[https://www.youtube.com/watch?v=NEwNs2b9YN8](https://www.youtube.com/watch?v=NEwNs2b9YN8)




<!-- code block begin -->

##### ****RadioButtons.vbs:**
    
```
' This example demonstrates how to create radio buttons.

' Create Bytescout.PDF.Document object
Set pdfDocument = CreateObject("Bytescout.PDF.Document")
pdfDocument.RegistrationName = "demo"
pdfDocument.RegistrationKey = "demo"

Set comHelpers = pdfDocument.ComHelpers

' Add page
Set page1 = comHelpers.CreatePage(comHelpers.PAPERFORMAT_A4)
pdfDocument.Pages.Add(page1)

Set timesFont = comHelpers.CreateStandardFont(comHelpers.STANDARDFONTS_TIMES, 12)
Set blackBrush = comHelpers.CreateSolidBrush(comHelpers.CreateColorGray(0))

' Add a group of radio buttons
Set radioButton1 = comHelpers.CreateRadioButton(20, 20, 15, 15, "group1", "value1")
Set radioButton2 = comHelpers.CreateRadioButton(20, 40, 15, 15, "group1", "value2")
page1.Annotations.Add(radioButton1)
page1.Annotations.Add(radioButton2)
' Add labels
page1.Canvas.DrawString "Value 1.1", (timesFont), (blackBrush), 40, 20
page1.Canvas.DrawString "Value 1.2", (timesFont), (blackBrush), 40, 40

' Add another independent group of radio buttons
Set radioButton3 = comHelpers.CreateRadioButton(120, 20, 15, 15, "group2", "value3")
Set radioButton4 = comHelpers.CreateRadioButton(120, 40, 15, 15, "group2", "value4")
page1.Annotations.Add(radioButton3)
page1.Annotations.Add(radioButton4)
' Add labels
page1.Canvas.DrawString "Value 2.1", (timesFont), (blackBrush), 140, 20
page1.Canvas.DrawString "Value 2.2", (timesFont), (blackBrush), 140, 40

' Save document to file
pdfDocument.Save("result.pdf")

' Open document in default PDF viewer app
Set shell = CreateObject("WScript.Shell")
shell.Run "result.pdf", 1, false

```

<!-- code block end -->