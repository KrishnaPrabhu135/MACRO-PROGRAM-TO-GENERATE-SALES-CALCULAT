# MACRO-PROGRAM-TO-GENERATE-SALES-CALCULAT
Sub CalculateTotalSales()
Dim employee As String, total As Double, sheet As Worksheet, i AsInteger
total = 0
employee = InputBox("Enter the employee name (case sensitive)")
For Each sheet In Worksheets
For i = 2 To 13 If sheet.Cells(i, 2).Value = employee Then
total = total + sheet.Cells(i, 3).Value
End If
Next i
Next sheet
MsgBox "Total sales of " & employee &
