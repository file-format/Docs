{
  "date" : "2022-04-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"AHK 파일 형식과 AHK 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"AHK 파일 형식 - AutoHotkey 스크립트 파일",
  "linktitle" : "AHK",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-04-25"
}

## .AHK 파일이란?

AHK 파일은 Microsoft Windows에서 작업 자동화에 사용되는 AutoHotkey 소프트웨어 응용 프로그램으로 생성된 스크립트 파일입니다. 여기에는 즉각적인 작업을 수행하는 데 사용할 수 있는 바로 가기 키를 사용하여 작업을 자동화하기 위한 지침이 포함되어 있습니다. 파일은 AutoHotkey에 의해 실행되며 모든 작업은 순차적으로 수행됩니다. AHK 파일은 단축키를 사용하여 정의된 단축키를 사용하여 복잡한 작업을 수행하기에 충분히 강력합니다. AHK 파일은 Microsoft 메모장 및 메모장++과 같은 텍스트 편집기로 열 수 있습니다.

## AHK 파일 형식

AHK 파일은 디스크에 일반 텍스트 파일로 저장되며 AutoHotkey로 실행할 수 있는 코드 라인을 포함합니다. AutoHotkey는 무료 오픈 소스 스크립팅 언어이며 사용자가 양식 채우기, 자동 클릭, 매크로 실행 등과 같은 작업을 수행하기 위해 간단한 스크립트에서 복잡한 스크립트를 만들 수 있습니다. AHK 파일은 최소한 단일 작업을 수행한 다음 종료할 수 있습니다. .

AHK를 [Exe](/ko/executable/exe/) 파일로 변환하는 데 사용할 수 있는 도구가 있습니다.

### AHK 예

다음 예제에서는 Win+Z 키를 사용하여 Microsoft 메모장을 실행하거나 이미 실행 중인 경우 맨 앞으로 가져옵니다.

```
#z::Run https://www.autohotkey.com  ; Win+Z

^!n::  ; Ctrl+Alt+N
if WinExist("Untitled - Notepad")
    WinActivate
else
    Run Notepad
return
```

## AHK 파일을 어떻게 생성합니까?

다음 단계를 사용하여 AHK 파일을 만들 수 있습니다. 이들은 AutoHotkey가 이미 머신에 설치되어 있다고 가정합니다.

* 바탕 화면에서 마우스 오른쪽 버튼을 클릭합니다.
* 메뉴에서 "신규"를 찾으십시오.
* "새로 만들기" 메뉴에서 "AutoHotkey Script"를 클릭합니다.
* 스크립트에 새 이름을 지정합니다.
* 바탕 화면에서 새로 생성된 파일을 찾아 마우스 오른쪽 버튼으로 클릭합니다.
* "스크립트 편집"을 클릭합니다.
* 메모장 같은 창이 떴어야 합니다.
* 파일을 저장합니다.

## 참고문헌

* [오토핫키](https://www.autohotkey.com/)
* [배치 파일 - Wikipewdia 제공](https://en.wikipedia.org/wiki/Batch_file)

