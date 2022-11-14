{
  "date" : "2021-06-30",
  "keywords" :[ "archivo wsf", "formato de archivo wsf", "qué es un archivo wsf", "archivo", "ejemplo de wsf", "extensión de archivo wsf","extensión", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo WSF y las API que pueden crear y abrir archivos WSF",
  "title" :"FSM - Archivo de script de Windows",
  "linktitle" : "WSF",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## ¿Qué es un archivo WSF?
Un archivo WSF es un script que se incluye en la categoría de ejecutable y se usa comúnmente en Microsoft Windows. La secuencia de comandos admite la combinación de varios idiomas, lo que significa que el archivo WSF puede incluir una combinación de JScript, VBScript y, opcionalmente, algunos elementos XML u otros lenguajes de secuencias de comandos como Python, Object REXX, Perl, Kixtart si el usuario los instala. Los archivos WSF se ejecutan solos en ausencia de WScript o CScript. Los archivos WSF pueden ser beneficiosos para el aislamiento de errores y la exposición de constantes.

## formato de archivo FSM
El formato de archivo WSF puede combinar JScript y VBScript de sus proyectos anteriores de Windows Script Host, un archivo .wsf le permite usarlos con Windows Script Host. Un script WSF encapsula una biblioteca de funciones que pueden usar varios archivos WSF. El siguiente ejemplo muestra un archivo .wsf que incluye un archivo JScript (fso.js), además de una función VBScript que llama a otra función.
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
El formato WSF admite las siguientes funciones adicionales:
- Incluir declaraciones
- Múltiples motores
- Bibliotecas de tipos
- Instrumentos
- Múltiples trabajos en un archivo

## Beneficios de los archivos WSF
Los archivos WSF pueden ser beneficiosos en las siguientes áreas:

### Aislamiento de errores
La naturaleza modular del archivo WSF puede evitar que una referencia de secuencia de comandos interfiera con otra, lo que hace que el WSF sea útil para aislar errores. Aquí hay un ejemplo de WSF con un módulo que produce un error y otro que no:
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
### Compatibilidad con idiomas mixtos
Un WSF admite varios idiomas, puede tener un código de uso de lenguaje de secuencias de comandos de otro lenguaje de secuencias de comandos. Aquí hay un ejemplo de cómo funciona:
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
### Exponiendo constantes
El WSF admite el enlace de un contenedor XML a una referencia o control de objeto para que pueda usar las constantes de ese objeto en lugar de tener que declararlas. El siguiente es un ejemplo:
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


## Referencias

* [Instalador de Windows - por Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)


