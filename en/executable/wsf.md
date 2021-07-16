{
  "date" : "2021-06-30",
  "keywords" : [ "wsf file", "wsf file format", "what is a wsf file", "file", "wsf example", "wsf file extension","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about WSF file format and APIs that can create and open WSF files.",
  "title" : "WSF - Windows Script File",
  "linktitle" : "WSF",
  "menu" : {
    "docs" : {
      "parent" : "executable"
    }
  },
  "lastmod" : "2021-06-30"
}

## What is a WSF file?
A WSF file is a script that fall under the executable category and commonly used in Microsoft Windows. The script supports the mixing of multiple languages, it means that in WSF file may include a blend of JScript, VBScript and optionally some XML elements or other scripting languages such as Python, Object REXX, Perl, Kixtart if installed by the user. The WSF files executes themselves in the absence of WScript or CScript. The WSF files can be beneficial in error isolation and exposing constants. 

## WSF file format
The WSF file format can mix the JScript and VBScript from your previous Windows Script Host projects, a .wsf file allows you to use them with Windows Script Host. A WSF script encapsulates a library of functions that can be used by various WSF files. The example below shows a .wsf file that includes a JScript file (fso.js), plus a VBScript function that calls another function. 
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
WSF format supports the following additional features:
- Include statements
- Multiple engines
- Type libraries
- Tools
- Multiple jobs in one file

## Benifits of WSF files
The WSF files can be beneficial in the following areas:

### Error isolation
 The modular nature of WSF file can prevents one script reference from interfering with another which makes the WSF useful for isolating errors. Here is an example of WSF with one module that produces an error and one that does not:
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
### Mixed language support
A WSF supports multiple languages, you can have one scripting language use code from another scripting language. Here is an example of how that works:
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
### Exposing constants
The WSF support the binding of an XML wrapper to an object reference or control so you can use that object's constants instead of having to declare them. Following is an example:
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


## References 

* [Windows Installer - by Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)

