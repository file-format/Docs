{
  "date" : "2019-10-11",
  "keywords" :[ "dhtml","dhtml 파일", "dhtml 파일 형식", "dhtml 파일 형식", "파일", "유형", "dhtml 파일이란" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DHTML - 동적 HTML 파일 형식",
  "description":"DHTML 파일을 만들고 열 수 있는 DHTML 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "DHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## DHTML 파일이란?

.dhtml 확장자를 가진 파일은 웹 페이지의 동적 콘텐츠를 만드는 데 사용되는 동적 [HTML](/ko/web/html/) 파일입니다. DHTML에서 생성된 웹 요소는 이벤트 기반이며 페이지를 다시 로드할 필요가 없습니다. 대부분의 경우 DHTML 파일은 드롭다운 메뉴, 플로팅 레이어, 롤오버 버튼 및 기타 동적 콘텐츠와 같은 웹 페이지의 동적 콘텐츠를 만드는 데 사용됩니다. 메뉴 항목에 마우스를 가져가면 추가 하위 메뉴 옵션이 열릴 때 거의 매일 동적 html 요소를 접하게 됩니다. DHTML은 [HTML](/ko/web/html/), [Javascript](/ko/web/js/), HTML DOM, HTML 이벤트 및 [CSS](/ko/web/css/)와 같은 웹 기술을 사용하여 동적 요소의 동작.

## DHTML 파일 형식

DHTML 파일은 웹 요소의 동적 동작을 구현하는 DHTML 코드가 포함된 일반 텍스트 파일입니다.


### DHTML DOM

DHTML DOM(문서 개체 모델)은 다음 이미지와 같이 요소, 속성 및 텍스트가 있는 트리 구조인 HTML DOM을 기반으로 합니다.

{{< figure src="../dhtml.png" alt="HTML DOM" >}}

'Document' 노드는 여러 기능을 구현하기 위해 여러 기능을 호출하는 데 사용할 수 있습니다. 다음 예제에서는 DHTML에서 JavaScript의 document.write() 메서드를 사용합니다.

```
<HTML>  
<head>  
<title>  
Method of a JavaScript  
</title>  
</head>  
<body>  
<script type="text/javascript">  
document.write("Hello World");  
</script>  
</body>  
</html>  
```

이 코드는 "Hello World"라는 텍스트를 브라우저에 출력하도록 작성합니다.

### DHTML 이벤트

|S.No.|이벤트|발생|
---|---|---|
|1|onabort|사용자가 페이지 또는 미디어 파일 로드를 중단할 때 발생합니다.|
|2|onblur|사용자가 HTML 객체를 떠날 때 발생합니다.|
|3|onchange|사용자가 객체의 값을 변경하거나 업데이트할 때 발생합니다.|
|4|onclick|사용자가 HTML 요소를 클릭할 때 발생하거나 트리거됩니다.|
|5|ondblclick|사용자가 HTML 요소를 함께 두 번 클릭할 때 발생합니다.|
|6|onfocus|사용자가 HTML 요소에 초점을 맞출 때 발생합니다. 이 이벤트 핸들러는 onblur와 반대로 작동합니다.|
|7|onkeydown|사용자가 키보드 장치의 키를 누를 때 트리거됩니다. 이 이벤트 핸들러는 모든 키에 대해 작동합니다.|
|8|onkeypress|사용자가 키보드의 키를 누를 때 트리거됩니다. 이 이벤트 핸들러는 모든 키에 대해 트리거되지 않습니다.|
|9|onkeyup|사용자가 개체나 요소를 누른 후 키보드에서 키를 놓을 때 발생합니다.|
|10|onload|객체가 완전히 로드되었을 때 발생합니다.|
|11|onmousedown|사용자가 HTML 요소 위에 마우스 버튼을 눌렀을 때 발생합니다.|
|12|onmousemove|사용자가 HTML 객체에서 커서를 움직일 때 발생합니다.|
|13|onmouseover|사용자가 HTML 개체 위로 커서를 이동할 때 발생합니다.|
|14|onmouseout|마우스 포인터가 HTML 요소 밖으로 이동할 때 발생하거나 트리거됩니다.|
|15|onmouseup|HTML 요소 위에서 마우스 버튼을 놓을 때 발생하거나 트리거됩니다.|
|16|onreset|사용자가 양식을 재설정하는 데 사용됩니다.|
|17|onselect|웹 페이지에서 내용이나 텍스트를 선택한 후 발생합니다.|
|18|onsubmit|양식 제출 후 사용자가 버튼을 클릭하면 트리거됩니다.|
|19|onunload|사용자가 웹 페이지를 닫을 때 트리거됩니다.|

## 참고문헌

* [동적 HTML - Wikipedia](https://en.wikipedia.org/wiki/Dynamic_HTML)

