{
  "date" : "2021-06-30",
  "keywords" :["wsfファイル","wsfファイル形式","wsfファイルとは","ファイル","wsf例","wsfファイル拡張子","拡張子","形式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"WSF ファイル形式と,WSF ファイルを作成して開くことができる API について学びます。",
  "title" :"WSF - Windows スクリプト ファイル",
  "linktitle" : "WSF",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## .WSF ファイルとは何ですか?
WSF ファイルは、実行可能なカテゴリに分類され、Microsoft Windows で一般的に使用されるスクリプトです。スクリプトは複数の言語の混合をサポートします。つまり、WSF ファイルには、JScript、VBScript、およびオプションでいくつかの XML 要素の混合、またはユーザーがインストールした場合は Python、Object REXX、Perl、Kixtart などの他のスクリプト言語を含めることができます。 WSF ファイルは、WScript または CScript がなくても実行されます。 WSF ファイルは、エラーの分離と定数の公開に役立ちます。

## WSF ファイル形式
WSF ファイル形式では、以前の Windows Script Host プロジェクトの JScript と VBScript を混在させることができます。.wsf ファイルを使用すると、それらを Windows Script Host で使用できます。 WSF スクリプトは、さまざまな WSF ファイルで使用できる関数のライブラリをカプセル化します。次の例は、JScript ファイル (fso.js) と、別の関数を呼び出す VBScript 関数を含む .wsf ファイルを示しています。
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
WSF 形式は、次の追加機能をサポートしています。
- ステートメントを含める
- 複数のエンジン
- タイプ ライブラリ
- ツール
- 1 つのファイルに複数のジョブ

## WSF ファイルの利点
WSF ファイルは、次の分野で役立ちます。

### エラー分離
WSF ファイルのモジュール性により、あるスクリプト参照が別のスクリプト参照に干渉するのを防ぐことができるため、WSF はエラーの分離に役立ちます。エラーを生成するモジュールと生成しないモジュールを含む WSF の例を次に示します。
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
### 混合言語のサポート
WSF は複数の言語をサポートします。1 つのスクリプト言語で別のスクリプト言語のコードを使用できます。これがどのように機能するかの例を次に示します。
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
### 定数の公開
WSF は、XML ラッパーのオブジェクト参照またはコントロールへのバインドをサポートしているため、オブジェクトの定数を宣言する代わりに使用できます。次に例を示します。
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


## 参考文献

* [Windows インストーラ - ウィキペディアによる](https://en.wikipedia.org/wiki/Windows_Installer)


