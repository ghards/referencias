[back](../readme.md)
# [VBA](https://docs.microsoft.com/pt-br/office/vba/api/overview/)
## Sintaxe das Macros
* **<ins>1048576</ins>**: Última linha do excel.
* **<ins>16384</ins>**: Última coluna do excel.
* **<ins>Alt + F11</ins>**: Atalho para o editor do VBA.
---
* **<ins>'</ins>**: Indica que a linha é um comentário.
---
### Operadores lógicos
```vb
  True / False
  Not 'não
  And 'e
  Or  'ou
  ==  'igual
  <>  'diferente
  >   'maior que
  >=  'maior ou igual
  <   'menor que
  <=  'menor ou igual
```
### Declaração de variáveis
```vb
  Dim variavel As Tipo: Set variavel = Nothing        'objetos
  Dim variavel As Tipo: variavel = valor              'tipos primitivos
  Const variavel As Tipo = valor                      'constantes

  With objeto
    .atributo
    .método
  End With

  Me                                                  'this
```
### Condicionais
```vb
  If condição Then
    ...
  ElseIf condição Then
    ...
  Else
    ...
  End If
```
```vb
  Select Case variavel
    Case
      ...
    Case Is                                   'comparador lógico
      ...
    Case Else                                 'default
      ...
  End Select
```
### Repetições
```vb
  For contador = inicio To final Step n       'faça de x até y de n em n
    ...
    Exit For
  Next
```
```vb
  For Each item in lista                      'para cada
    ...
  Next
```
```vb
  Do Until condição                           'faça até
    ...
    Exit Do
  Loop
```
```vb
  Do While condição                           'faça enquanto
    ...
  Loop
```
### Funções
```vb
  Private Function nome_funcao(ByVal parametro As Tipo) As Tipo
    ...
    Return
    Exit Function
  End Function
```
```vb
  Public Sub nome_funcao(Optional ByRef parametro As Tipo = valor)
    ...
    Exit Sub
  End Sub
```
### Tratamento de erros
```vb
label:
  On Error Resume Next
  On Error GoTo label
```
### Integrações
#### Word
```vb
  Dim wordApp As Word.Application: Set wordApp = CreateObject("Word.Application")
  Dim documento As Document: Set documento = wordApp.Documents.Add
```
#### PowerPoint
```vb
  Dim pptApp As PowerPoint.Application: Set pptApp = New PowerPoint.Application
  Dim documento As Presentation: Set documento = pptApp.Presentation.Add
```
#### OutLook
```vb
  Dim emailApp As OutLook.Application: Set emailApp = CreateObject("OutLook.Application")
  Dim email As MailItem: Set email = emailApp.CreateItem(0)
```