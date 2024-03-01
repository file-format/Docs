{
  "date": "2021-06-30",
  "keywords": [
"wsf-tiedosto",
"wsf-tiedostomuoto",
"mikä on wsf-tiedosto",
"tiedosto",
"wsf esimerkki",
"wsf tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi WSF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata WSF-tiedostoja.",
  "title": "WSF - Windowsin komentosarjatiedosto",
  "linktitle": "WSF",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ws-fif"
}
},
  "lastmod": "2021-06-30"
}

## Mikä on WSF-tiedosto?
WSF-tiedosto on komentosarja, joka kuuluu suoritettavaan kategoriaan ja jota käytetään yleisesti Microsoft Windowsissa. Skripti tukee useiden kielten sekoittamista, mikä tarkoittaa, että WSF-tiedostossa voi olla sekoitus JScriptiä, VBScriptiä ja valinnaisesti joitain XML-elementtejä tai muita komentosarjakieliä, kuten Python, Object REXX, Perl, Kixtart, jos käyttäjä on asentanut ne. WSF-tiedostot suorittavat itsensä ilman WScriptiä tai CScriptiä. WSF-tiedostot voivat olla hyödyllisiä virheiden eristämisessä ja vakioiden paljastamisessa.

## WSF tiedostomuoto
WSF-tiedostomuoto voi sekoittaa aiempien Windows Script Host -projektiesi JScriptin ja VBScriptin, .wsf-tiedoston avulla voit käyttää niitä Windows Script Hostin kanssa. WSF-skripti sisältää kirjaston funktioita, joita useat WSF-tiedostot voivat käyttää. Alla olevassa esimerkissä näkyy .wsf-tiedosto, joka sisältää JScript-tiedoston (fso.js) sekä VBScript-funktion, joka kutsuu toista funktiota.
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
WSF-muoto tukee seuraavia lisäominaisuuksia:
- Sisällytä lausunnot
- Useita moottoreita
- Tyyppikirjastot
- Työkalut
- Useita töitä yhdessä tiedostossa

## WSF-tiedostojen edut
WSF-tiedostot voivat olla hyödyllisiä seuraavilla alueilla:

### Virheeristys
WSF-tiedoston modulaarinen luonne voi estää yhtä komentosarjaviittausta häiritsemästä toista, mikä tekee WSF:stä hyödyllisen virheiden eristämisessä. Tässä on esimerkki WSF:stä, jossa on yksi moduuli, joka tuottaa virheen ja toinen ei:
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
### Sekakielinen tuki
WSF tukee useita kieliä, voit käyttää yhtä skriptikielen koodia toisesta skriptikielestä. Tässä on esimerkki siitä, miten se toimii:
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
### Vakioiden paljastaminen
WSF tukee XML-kääreen sitomista objektiviittaukseen tai ohjausobjektiin, jotta voit käyttää objektin vakioita niiden ilmoittamisen sijaan. Seuraavassa on esimerkki:
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


## Viitteet 

* [Windows Installer - Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)



