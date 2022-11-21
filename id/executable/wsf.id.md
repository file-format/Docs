{
  "date" : "2021-06-30",
  "keywords" :[ "file wsf", "format file wsf", "apa itu file wsf", "file", "contoh wsf", "ekstensi file wsf", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file WSF dan API yang dapat membuat dan membuka file WSF.",
  "title" :"WSF - File Skrip Windows",
  "linktitle" : "WSF",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Apa itu file WSF?
File WSF adalah skrip yang termasuk dalam kategori yang dapat dieksekusi dan biasanya digunakan di Microsoft Windows. Skrip mendukung pencampuran beberapa bahasa, artinya dalam file WSF dapat menyertakan campuran JScript, VBScript dan secara opsional beberapa elemen XML atau bahasa skrip lain seperti Python, Object REXX, Perl, Kixtart jika diinstal oleh pengguna. File WSF mengeksekusi sendiri tanpa adanya WScript atau CScript. File WSF dapat bermanfaat dalam isolasi kesalahan dan mengekspos konstanta.

## Format file WSF
Format file WSF dapat mencampur JScript dan VBScript dari proyek Windows Script Host Anda sebelumnya, file .wsf memungkinkan Anda untuk menggunakannya dengan Windows Script Host. Skrip WSF merangkum pustaka fungsi yang dapat digunakan oleh berbagai file WSF. Contoh di bawah menunjukkan file .wsf yang menyertakan file JScript (fso.js), ditambah fungsi VBScript yang memanggil fungsi lain.
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
Format WSF mendukung fitur tambahan berikut:
- Sertakan pernyataan
- Beberapa mesin
- Ketik perpustakaan
- Peralatan
- Beberapa pekerjaan dalam satu file

## Manfaat file WSF
File WSF dapat bermanfaat di bidang berikut:

### Isolasi kesalahan
Sifat modular file WSF dapat mencegah satu referensi skrip mengganggu yang lain yang membuat WSF berguna untuk mengisolasi kesalahan. Berikut adalah contoh WSF dengan satu modul yang menghasilkan kesalahan dan yang tidak:
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
### Dukungan bahasa campuran
WSF mendukung banyak bahasa, Anda dapat membuat satu bahasa skrip menggunakan kode dari bahasa skrip lain. Berikut adalah contoh cara kerjanya:
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
### Mengekspos konstanta
WSF mendukung pengikatan pembungkus XML ke referensi atau kontrol objek sehingga Anda dapat menggunakan konstanta objek tersebut alih-alih harus mendeklarasikannya. Berikut ini adalah contohnya:
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


## Referensi

* [Penginstal Windows - oleh Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)


