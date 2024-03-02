{
  "date": "2021-06-30",
  "keywords": [
"comhad wsf",
"Formáid comhaid wsf",
"cad is comhad wsf ann",
"comhad",
"sampla wsf",
"síneadh comhad wsf",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid WSF agus APIs is féidir comhaid WSF a chruthú agus a oscailt.",
  "title": "WSF - Comhad Script Windows",
  "linktitle": "WSF",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ws-gaf"
}
},
  "lastmod": "2021-06-30"
}

## Cad is comhad WSF ann?
Is script é comhad WSF a thagann faoin gcatagóir inrite agus a úsáidtear go coitianta i Microsoft Windows. Tacaíonn an script le meascadh teangacha iolracha, ciallaíonn sé go bhféadfadh cumasc de JScript, VBScript agus go roghnach roinnt eilimintí XML nó teangacha scriptithe eile cosúil le Python, Object REXX, Perl, Kixtart a bheith i gcomhad WSF má tá sé suiteáilte ag an úsáideoir. Déanann na comhaid WSF iad féin a fhorghníomhú in éagmais WScript nó CScript. Féadfaidh na comhaid WSF a bheith tairbheach maidir le haonrú earráide agus le tairisigh a nochtadh.

## Formáid comhaid WSF
Is féidir le formáid comhaid WSF an JScript agus VBScript a mheascadh ó do thionscadail roimhe seo Windows Script Host, ceadaíonn comhad .wsf duit iad a úsáid le Windows Script Host. Cuimsíonn script WSF leabharlann feidhmeanna ar féidir le comhaid WSF éagsúla a úsáid. Taispeánann an sampla thíos comhad .wsf a chuimsíonn comhad JScript (fso.js), chomh maith le feidhm VBScript a ghlaonn feidhm eile air.
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
Tacaíonn formáid WSF leis na gnéithe breise seo a leanas:
- Cuir ráitis san áireamh
- Innill Il
- Cineál leabharlanna
- Uirlisí
- Poist iolracha i gcomhad amháin

## Buntáistí comhaid WSF
Féadfaidh na comhaid WSF a bheith tairbheach sna réimsí seo a leanas:

### Earráid leithlisiú
Is féidir le nádúr modúlach comhad WSF cosc a chur ar thagairt scripte amháin cur isteach ar cheann eile, rud a fhágann go bhfuil an WSF úsáideach chun earráidí a aonrú. Seo sampla de WSF le modúl amháin a chruthaíonn earráid agus modúl nach ndéanann:
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
### Tacaíocht teanga mheasctha
Tacaíonn WSF le teangacha iolracha, is féidir cód úsáide teanga scriptithe amháin a bheith agat ó theanga scriptithe eile. Seo sampla de conas a oibríonn sé sin:
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
### Tairisigh nochtaithe
Tacaíonn an WSF le cumhdach XML a cheangal le tagairt nó le rialú oibiachta ionas gur féidir leat tairisigh an réada sin a úsáid seachas a bheith ort iad a dhearbhú. Seo a leanas sampla:
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


## Tagairtí 

* [Suiteálaí Windows - le Vicipéid](https://en.wikipedia.org/wiki/Windows_Installer)



