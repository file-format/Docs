{
  "date" : "2021-06-30",
  "keywords" :[ "wsf dosyası", "wsf dosya biçimi", "wsf dosyası nedir", "dosya", "wsf örneği", "wsf dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"WSF dosya biçimi ve WSF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"WSF - Windows Komut Dosyası",
  "linktitle" : "WSF",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Bir WSF dosyası nedir?
Bir WSF dosyası, yürütülebilir kategorisine giren ve genellikle Microsoft Windows'ta kullanılan bir komut dosyasıdır. Komut dosyası, birden çok dilin karıştırılmasını destekler; bu, WSF dosyasında JScript, VBScript ve isteğe bağlı olarak bazı XML öğelerinin bir karışımını veya kullanıcı tarafından kuruluysa Python, Object REXX, Perl, Kixtart gibi diğer komut dosyası dillerini içerebileceği anlamına gelir. WSF dosyaları, WScript veya CScript yokluğunda kendilerini yürütür. WSF dosyaları, hata izolasyonunda ve sabitleri açığa çıkarmada faydalı olabilir.

## WSF dosya biçimi
WSF dosya biçimi, önceki Windows Komut Dosyası Sistemi projelerinizdeki JScript ve VBScript'i karıştırabilir; bir .wsf dosyası, bunları Windows Komut Dosyası Sistemi ile kullanmanıza olanak tanır. Bir WSF betiği, çeşitli WSF dosyaları tarafından kullanılabilen bir işlev kitaplığını kapsar. Aşağıdaki örnekte, bir JScript dosyası (fso.js) ve başka bir işlevi çağıran bir VBScript işlevi içeren bir .wsf dosyası gösterilmektedir.
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
WSF formatı aşağıdaki ek özellikleri destekler:
- İfadeleri dahil et
- Çoklu motorlar
- Tip kitaplıkları
- Aletler
- Bir dosyada birden fazla iş

## WSF dosyalarının avantajları
WSF dosyaları aşağıdaki alanlarda faydalı olabilir:

### Hata izolasyonu
WSF dosyasının modüler yapısı, bir komut dosyası referansının diğerine müdahale etmesini önleyebilir, bu da WSF'yi hataları izole etmek için kullanışlı kılar. Burada bir modülü hata üreten ve diğeri oluşturmayan bir WSF örneği verilmiştir:
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
### Karma dil desteği
Bir WSF birden çok dili destekler, bir betik dilinin başka bir betik dilinden kod kullanmasını sağlayabilirsiniz. İşte bunun nasıl çalıştığına dair bir örnek:
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
### Sabitleri açığa çıkarmak
WSF, bir XML sarıcının bir nesne başvurusuna veya denetime bağlanmasını destekler, böylece o nesnenin sabitlerini bildirmek yerine kullanabilirsiniz. Aşağıda bir örnek verilmiştir:
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


## Referanslar

* [Windows Installer - Wikipedia'dan](https://en.wikipedia.org/wiki/Windows_Installer)


