<div align="center">

## App\.Path Thing


</div>

### Description

Correct Reference to Files in App.Path.

For Newbies and for all who get Errors and don't know why.

If you think this deserves a Vote, then do so, if not, then don't. I just wanted to explain a common error source !
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Thomas Sturm](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/thomas-sturm.md)
**Level**          |Advanced
**User Rating**    |3.5 (56 globes from 16 users)
**Compatibility**  |VB 5\.0, VB 6\.0
**Category**       |[Files/ File Controls/ Input/ Output](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/files-file-controls-input-output__1-3.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/thomas-sturm-app-path-thing__1-23813/archive/master.zip)





### Source Code

```
After seeing so many wrong codes on this, I decided to clear things up a bit.
If you want to refer to a file located in app.path, nearly everyone writes
SomeVar$ = App.Path & "\SomeFile.txt"
What if the Program is located in the Root-Directory ? It gives a Run-Time Error because of the "\\", since App.Path returns "C:\" for example, then appends "\SomeFile.txt", which results in "C:\\SomeFile.txt".
ONE correct way would be :
Dim SourceFile As String
If Right$(App.Path, 1) = "\" Then
 SourceFile = App.Path & "SomeFile.txt"
Else
 SourceFile = App.Path & "\SomeFile.txt"
End If
This is the way I use, if there are any other, please put it in the comments.
```

