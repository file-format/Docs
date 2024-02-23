{
   "date" : "2023-12-14",
   "keywords" : [
"ws",
"ws 파일",
"ws 윈도우 스크립트 파일",
"WS 파일을 여는 방법",
"파일",
"WS 파일 확장자",
"확대",
"파일"
],
   "author" : {
      "display_name" : "Shakeel Faiz"
},
   "draft" : "false",
   "toc" : true,
   "title" : "WS 파일 - Windows 스크립트 - .ws 파일이란 무엇이며 어떻게 여나요?",
   "description" : "WS 파일을 만들고 열 수 있는 WS Windows 스크립트 파일 형식과 API에 대해 알아보세요.",
   "linktitle" : "WS",
   "menu" : {
      "docs" : {
         "identifier" : "executable-ws-ko",
         "parent" : "executable"
}
},
   "lastmod" : "2023-12-14"
}

## .WS 파일이란?

Windows의 **.WS 파일**에는 일반적으로 **Windows 스크립트 호스트**를 통해 실행되도록 설계된 실행 가능한 스크립트가 들어 있습니다. 이 스크립트는 XML 요소뿐만 아니라 JScript 및 VBScript 루틴과 같은 다양한 요소와 루틴을 포함할 수 있습니다. .ws 파일을 두 번 클릭하면 Windows 스크립트 호스트가 파일에 포함된 스크립트의 실행을 시작합니다.

## Windows 호스트 스크립트 정보

WSH(Windows 스크립트 호스트)는 사용자가 VBScript(Visual Basic Scripting Edition) 및 JScript(Microsoft의 JavaScript 버전)와 같은 스크립팅 언어로 작성된 스크립트를 실행할 수 있도록 Microsoft에서 개발한 스크립팅 호스트입니다. Windows 운영 체제에서 스크립팅을 위한 프레임워크를 제공하여 다양한 작업 및 시스템 관리를 자동화할 수 있습니다.

Windows 스크립트 호스트에 대한 몇 가지 주요 사항은 다음과 같습니다.

1.  **스크립팅 언어:** WSH는 VBScript와 JScript가 가장 일반적으로 사용되는 여러 스크립트 언어를 지원합니다. 작업을 자동화하고 운영 체제와 상호 작용하거나 데이터를 조작하기 위해 이러한 언어 중 하나로 스크립트를 작성할 수 있습니다.
    
2.  **스크립트 실행:** WSH 스크립트는 일반적으로 VBScript의 경우 .vbs, JScript의 경우 .js와 같은 확장자를 가진 파일에 저장됩니다. 스크립트를 실행하면 WSH가 코드를 해석하고 실행합니다.
    
3.  **자동화:** WSH는 반복 작업 자동화, 시스템 설정 관리, 관리 기능 수행과 같은 자동화 목적으로 자주 사용됩니다. 시스템 관리자와 고급 사용자에게 특히 유용합니다.
    
4.  **콘솔 및 GUI 스크립트:** WSH 스크립트는 콘솔 기반이거나 GUI 기반일 수 있습니다. 콘솔 스크립트는 명령줄 창에서 실행되는 반면 GUI 스크립트는 보다 대화형 애플리케이션을 위한 그래픽 사용자 인터페이스를 생성할 수 있습니다.
    
5.  **Security:** WSH has security features to help prevent malicious scripts from causing harm; users are typically prompted before executing scripts and scripts are subject to certain restrictions to prevent unauthorized access and actions.
    
6.  **Windows 스크립트 호스트 개체 모델:** WSH는 스크립트가 Windows 운영 체제와 상호 작용할 수 있도록 하는 개체 모델을 제공합니다. 여기에는 파일 시스템, 레지스트리 설정, 네트워크 리소스 및 기타 시스템 구성 요소에 대한 액세스가 포함됩니다.
    
7.  **명령줄에서 스크립트 실행:** 콘솔 또는 GUI 환경에서 스크립트를 실행할지 여부에 따라 `cscript.exe` 또는 `wscript.exe` 실행 파일을 사용하여 명령줄에서 WSH 스크립트를 실행할 수 있습니다. .

## WS 파일 여는 방법?

WS 파일은 일반 텍스트 파일이므로 열거나 편집하려면 다음과 같은 텍스트 편집기를 사용할 수 있습니다.

- **메모장**
- **메모장++**
- **애플 텍스트편집**
- **Visual Studio 코드**

WS 파일 내에서 스크립트를 실행하려면 해당 스크립트를 두 번 클릭하거나 명령줄에서 'wscript' 명령을 사용하면 됩니다.

## 참고자료
* [윈도우 스크립트 호스트](https://en.wikipedia.org/wiki/Windows_Script_Host)


