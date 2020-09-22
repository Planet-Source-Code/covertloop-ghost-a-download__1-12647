<div align="center">

## Ghost A Download


</div>

### Description

This code downloads anything off the internet without popping up a dialog box of any sort. Very simple to use. Vote if ya wanna.
 
### More Info
 
Don't forget about the declarations.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[CovertLoop](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/covertloop.md)
**Level**          |Beginner
**User Rating**    |5.0 (15 globes from 3 users)
**Compatibility**  |VB 4\.0 \(16\-bit\), VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0
**Category**       |[Coding Standards](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/coding-standards__1-43.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/covertloop-ghost-a-download__1-12647/archive/master.zip)

### API Declarations

```
Private Declare Function URLDownloadToFile Lib "urlmon" Alias _
  "URLDownloadToFileA" (ByVal pCaller As Long, _
  ByVal szURL As String, _
  ByVal szFileName As String, _
  ByVal dwReserved As Long, _
  ByVal lpfnCB As Long) As Long
Public Function DownloadFile(URL As String, _
  LocalFilename As String) As Boolean
  Dim lngRetVal As Long
  lngRetVal = URLDownloadToFile(0, URL, LocalFilename, 0, 0)
  If lngRetVal = 0 Then DownloadFile = True
End Function
```


### Source Code

G = DownloadFile("UrlOfTheFileToDownload", "c:\windows\desktop\FileName.htm")

