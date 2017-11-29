 ##### 所有sheet
* 自动滚动选择A1单元格
* sheet缩放到100%
* 自动保存/关闭

```  
Sub ResetCursorAndZoom()
    Dim s As Object
    Dim defaultSheet As Object
    Set defaultSheet = ActiveSheet
    For Each s In ActiveWorkbook.Sheets
        s.Activate
        ActiveSheet.Range("A1").Select
        ActiveWindow.Zoom = 100
    Next s
    defaultSheet.Activate
    ActiveWorkbook.Save
    ActiveWorkbook.Close
End Sub
```  

---
