{
  "date" : "2021-08-24", 
  "keywords" :[ "vbs", "파일", "확장자", "파일 형식", "Visual Basic 스크립트", "프로그래밍 가이드", "vbs 예제", "Microsoft Visual Basic", "VBScript" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBS - Visual Basic 스크립트 파일",
  "description":"VBS 파일 형식 및 VBS 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "VBS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-08-24"
}

## .VBS 파일이란?

VBS 또는 VBScript는 Microsoft Visual Basic의 스크립트 버전과 연결됩니다. 컴퓨팅 환경에서 사용자는 많은 측면에 액세스하고 제어할 수 있습니다. VBScript는 **Component Object Model**이라는 모델을 사용하여 환경의 요소와 도구를 사용할 수 있습니다. 이 환경은 VBScript 작업 및 실행을 위해 지정됩니다.

웹 개발 분야에서 클라이언트가 접근할 때 자바스크립트와 유사한 역할을 한다. 또한 웹 페이지 처리를 위해 서버에서 사용됩니다. [HTML](/ko/web/html/)의 응용 프로그램과 같은 일부 다른 유형의 스크립팅 파일에서 고려할 수 있습니다.


## 간략한 역사 ##

Windows 스크립트용으로 지정된 Microsoft에서 사용하는 기술의 일부로 1996년에 처음 출시되었습니다. 처음에는 웹 개발자의 도움을 위해 특별히 개발되었습니다. 같은 해 Visual Basic Script의 기능과 함께 Internet Explorer라는 Microsoft Windows 탐색기가 출시되었습니다.

기술과 웹 개발이 발전함에 따라 많은 고급 기능과 함께 많은 버전의 VBScript가 출시되었습니다. 더욱이, 내년에 이 스크립팅 언어는 새로운 기능을 갖춘 Microsoft Windows의 일부가 될 것입니다.

## 기술 사양 ##

서버 측 웹 페이지의 경우 **Active Server Pages**와 같은 도구가 VBScript와 함께 사용됩니다. 이 스크립팅 언어는 Windows의 스크립트 구성 요소에서도 사용할 수 있습니다. 이 언어의 파일은 Windows에서 .vbs 확장자로 저장됩니다.

이 언어의 코드에서 사용되는 루프와 같은 많은 제어 구조가 있습니다. 또한 명령줄이며 명명되거나 명명되지 않은 인수도 포함합니다. 이 언어의 파일은 Windows 운영 체제의 폴더나 바탕 화면에 간단히 저장할 수 있습니다. Microsoft Script Editor와 같은 VBScript 프로그램을 위한 특정 통합 개발 환경은 없지만 이 언어의 개발 기능을 제공합니다.

VBScript가 Windows의 Script 호스트에 의해 호스팅되면 스크립팅 언어에 매우 일반적이지만 Visual Basic 6.0에서는 사용할 수 없는 다양한 기능을 제공합니다. 손쉬운 또는 직접 액세스와 관련된 기능에는 네트워크 프린터, 명명되지 않은 명명된 명령줄 인수, stdout 및 stdin, 네트워크 공유, Windows Management Instrumentation, 그룹 구성원과 같은 네트워크의 사용자 정보 등이 포함됩니다.

## VBS 파일 형식 예 ##

```
<% Option Explicit %>
 <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
 <html>
 	<head>
 		<title>VBScript Example</title>
 	</head>
 	<body>
 		<div><% 
 			' Grab current time from Now() function.
 			' An '=' sign occurring after a context switch (<%) is shorthand 
 			' for a call to the Write() method of the Response object.
 			Dim timeValue : timeValue = Now %>
 			The time, in 24-hour format, is 
 			<%=Hour(timeValue)%>:<%=Minute(timeValue)%>:<%=Second(timeValue)%>.
 		</div>
 	</body>
 </html>
```

## 참조 ##

* [VBS - 위키백과 제공](https://en.wikipedia.org/wiki/VBScript)



