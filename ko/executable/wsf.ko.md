{
  "date" : "2021-06-30",
  "keywords" :[ "wsf 파일", "wsf 파일 형식", "wsf 파일이란", "파일", "wsf 예제", "wsf 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"WSF 파일을 만들고 열 수 있는 WSF 파일 형식과 API에 대해 알아보세요.",
  "title" :"WSF - Windows 스크립트 파일",
  "linktitle" : "WSF",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## .WSF 파일이란?
WSF 파일은 실행 가능한 범주에 속하며 Microsoft Windows에서 일반적으로 사용되는 스크립트입니다. 스크립트는 여러 언어의 혼합을 지원합니다. 즉, WSF 파일에 JScript, VBScript 및 선택적으로 일부 XML 요소 또는 사용자가 설치한 경우 Python, Object REXX, Perl, Kixtart와 같은 기타 스크립팅 언어의 혼합이 포함될 수 있습니다. WSF 파일은 WScript 또는 CScript가 없을 때 자체적으로 실행됩니다. WSF 파일은 오류 격리 및 상수 노출에 유용할 수 있습니다.

## WSF 파일 형식
WSF 파일 형식은 이전 Windows 스크립트 호스트 프로젝트의 JScript와 VBScript를 혼합할 수 있으며 .wsf 파일을 사용하면 Windows 스크립트 호스트와 함께 사용할 수 있습니다. WSF 스크립트는 다양한 WSF 파일에서 사용할 수 있는 함수 라이브러리를 캡슐화합니다. 아래 예는 JScript 파일(fso.js)과 다른 함수를 호출하는 VBScript 함수를 포함하는 .wsf 파일을 보여줍니다.
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
WSF 형식은 다음과 같은 추가 기능을 지원합니다.
- 포함 문
- 다중 엔진
- 유형 라이브러리
- 도구
- 하나의 파일에 여러 작업

## WSF 파일의 이점
WSF 파일은 다음 영역에서 유용할 수 있습니다.

### 오류 격리
WSF 파일의 모듈식 특성은 하나의 스크립트 참조가 다른 스크립트 참조를 방해하는 것을 방지하여 WSF를 오류 격리에 유용하게 만듭니다. 다음은 오류를 생성하는 모듈과 그렇지 않은 모듈이 있는 WSF의 예입니다.
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
### 혼합 언어 지원
WSF는 여러 언어를 지원하므로 한 스크립팅 언어에서 다른 스크립팅 언어의 코드를 사용할 수 있습니다. 작동 방식의 예는 다음과 같습니다.
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
### 상수 노출
WSF는 XML 래퍼를 개체 참조 또는 컨트롤에 바인딩하는 것을 지원하므로 선언할 필요 없이 해당 개체의 상수를 사용할 수 있습니다. 다음은 예입니다.
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


## 참고문헌

* [Windows Installer - Wikipedia 제공](https://en.wikipedia.org/wiki/Windows_Installer)


