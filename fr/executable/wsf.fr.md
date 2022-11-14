{
  "date" : "2021-06-30",
  "keywords" :[ "fichier wsf", "format de fichier wsf", "qu'est-ce qu'un fichier wsf", "fichier", "exemple wsf", "extension de fichier wsf","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier WSF et les API qui peuvent créer et ouvrir des fichiers WSF.",
  "title" :"WSF - Fichier de script Windows",
  "linktitle" : "WSF",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Qu'est-ce qu'un fichier WSF ?
Un fichier WSF est un script appartenant à la catégorie des exécutables et couramment utilisé dans Microsoft Windows. Le script prend en charge le mélange de plusieurs langues, cela signifie que le fichier WSF peut inclure un mélange de JScript, VBScript et éventuellement certains éléments XML ou d'autres langages de script tels que Python, Object REXX, Perl, Kixtart s'ils sont installés par l'utilisateur. Les fichiers WSF s'exécutent en l'absence de WScript ou CScript. Les fichiers WSF peuvent être utiles pour isoler les erreurs et exposer les constantes.

## Format de fichier WSF
Le format de fichier WSF peut mélanger le JScript et le VBScript de vos précédents projets Windows Script Host, un fichier .wsf vous permet de les utiliser avec Windows Script Host. Un script WSF encapsule une bibliothèque de fonctions qui peuvent être utilisées par divers fichiers WSF. L'exemple ci-dessous montre un fichier .wsf qui inclut un fichier JScript (fso.js), plus une fonction VBScript qui appelle une autre fonction.
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
Le format WSF prend en charge les fonctionnalités supplémentaires suivantes :
- Inclure des déclarations
- Plusieurs moteurs
- Bibliothèques de types
- Outils
- Plusieurs travaux dans un seul fichier

## Avantages des fichiers WSF
Les fichiers WSF peuvent être utiles dans les domaines suivants :

### Isolement des erreurs
La nature modulaire du fichier WSF peut empêcher une référence de script d'interférer avec une autre, ce qui rend le WSF utile pour isoler les erreurs. Voici un exemple de WSF avec un module qui produit une erreur et un qui n'en produit pas :
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
### Prise en charge de plusieurs langues
Un WSF prend en charge plusieurs langages, vous pouvez avoir un langage de script utilisant le code d'un autre langage de script. Voici un exemple de comment cela fonctionne :
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
### Exposition des constantes
Le WSF prend en charge la liaison d'un wrapper XML à une référence d'objet ou à un contrôle afin que vous puissiez utiliser les constantes de cet objet au lieu d'avoir à les déclarer. Voici un exemple :
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


## Références

* [Windows Installer - par Wikipédia](https://en.wikipedia.org/wiki/Windows_Installer)


