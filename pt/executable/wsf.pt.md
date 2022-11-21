{
  "date" : "2021-06-30",
  "keywords" :[ "arquivo wsf", "formato de arquivo wsf", "o que é um arquivo wsf", "arquivo", "exemplo wsf", "extensão de arquivo wsf", "extensão", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo WSF e APIs que podem criar e abrir arquivos WSF.",
  "title" :"WSF - Arquivo de script do Windows",
  "linktitle" : "WSF",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## O que é um arquivo WSF?
Um arquivo WSF é um script que se enquadra na categoria executável e comumente usado no Microsoft Windows. O script suporta a mistura de várias linguagens, isso significa que no arquivo WSF pode incluir uma mistura de JScript, VBScript e opcionalmente alguns elementos XML ou outras linguagens de script como Python, Object REXX, Perl, Kixtart se instalado pelo usuário. Os arquivos WSF são executados sozinhos na ausência de WScript ou CScript. Os arquivos WSF podem ser benéficos no isolamento de erros e na exposição de constantes.

## Formato de arquivo WSF
O formato de arquivo WSF pode misturar o JScript e o VBScript de seus projetos anteriores do Windows Script Host, um arquivo .wsf permite que você os use com o Windows Script Host. Um script WSF encapsula uma biblioteca de funções que podem ser usadas por vários arquivos WSF. O exemplo abaixo mostra um arquivo .wsf que inclui um arquivo JScript (fso.js), além de uma função VBScript que chama outra função.
```
<job id="IncludeExample">
   <script language="JScript" src="FSO.JS"/>
   <script language="VBScript">
      ' Get the free space for drive C.
      s = GetFreeSpace("c:")
      WScript.Echo s
   <script>
</job>
```
O formato WSF suporta os seguintes recursos adicionais:
- Incluir declarações
- Vários motores
- Bibliotecas de tipos
- Ferramentas
- Vários trabalhos em um arquivo

## Benefícios dos arquivos WSF
Os arquivos WSF podem ser benéficos nas seguintes áreas:

### Isolamento de erros
A natureza modular do arquivo WSF pode impedir que uma referência de script interfira em outra, o que torna o WSF útil para isolar erros. Aqui está um exemplo de WSF com um módulo que produz um erro e outro que não:
```
<?xml version="1.0" ?>
 <job id="Partially works">
   <!-- This will not work -->
   <script language="VBScript">
'    <![CDATA[
         WScript.echo 4/0 ' Oh, boy! You cannot divide by zero...
     ]]>
   </script>
   <!-- This will work... definitely... -->
   <script language="VBScript">
     <![CDATA[
         WScript.echo "Hello, Scripters!" & vbNewline & _
                      "Fantastic! It worked!"
'    ]]>
   </script>
 </job>
```
### Suporte a idiomas mistos
Um WSF suporta vários idiomas, você pode ter um código de uso de linguagem de script de outra linguagem de script. Aqui está um exemplo de como isso funciona:
```
<?xml version="1.0" ?>
<!-- Mixing JScript and VBScript -->
 <job id="SORT-VBScriptWithJScript">
   <script language="JScript">
     function SortVBArray(arrVBArray) {return arrVBArray.toArray().sort();}
   </script>
   <script language="VBScript">
'    <![CDATA[
     '** Fastest sort: call the Jscript sort from VBScript
     myData = "a,b,c,1,2,3,X,Y,Z,p,d,q"
     wscript.echo "Original List of values: " & vbTab & myData
     starttime = timer()
     sortedArray = SortVBArray(split(myData,","))
     endtime=timer()
     jscriptTime = round(endtime-starttime,2)
     wscript.echo "JScript sorted in " & jscriptTime & " seconds: "  & vbTab & sortedArray
'    ]]>
   </script>
 </job>
```
### Expondo constantes
O WSF suporta a vinculação de um wrapper XML a uma referência ou controle de objeto para que você possa usar as constantes desse objeto em vez de declará-las. Segue um exemplo:
```
<?xml version="1.0" ?>
<!-- WSF Example with Object Reference
Notes for this very formal example:
 CDATA is used to help the XML parser ignore 
 special characters in the content of the script.  
 The CDATA open and close must be masked 
 from VBScript by making them comments.
-->
<package>
 <job id="EnumerateConstantsADO">
  <reference object="ADODB.Recordset" />
  <script language="VBScript">
'  <![CDATA[
    dim title, str, i
    ctecArray = Array("adOpenUnspecified","adOpenForwardOnly", _
                      "adOpenKeyset","adOpenDynamic","adOpenStatic")
    title = "ADO Recordset Values for Constants"
    str = title & vbNewLine & vbNewLine
    str = str & "*CursorTypeEnum Constants*" & vbNewLine
    For i = 0 to ubound(ctecArray)
      str = str & Eval(ctecArray(i)) & vbTab & ctecArray(i) & vbNewLine
    Next
    str = str & vbNewLine
    str = str & "*LockTypeEnum Constants*" & vbNewLine
    ltecArray = Array("adLockUnspecified","adLockReadOnly", _
                      "adLockPessimistic","adLockOptimistic", _
                      "adLockBatchOptimistic")
    For i = 0 to ubound(ltecArray)
      str = str & Eval(ltecArray(i)) & vbTab & ltecArray(i) & vbNewLine
    Next
    MsgBox str, vbInformation, Title
'  ]]>
  </script>
 </job>
</package>
```


## Referências

* [Windows Installer - pela Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)


