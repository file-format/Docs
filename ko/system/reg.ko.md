{
"날짜": "2023-03-07",
  "keywords": [
"reg 파일",
"reg 파일이 무엇인가요?",
"파일",
"reg 파일 확장자",
"확대"
],
  "author": {
"display_name": "샤킬 파이즈"
},
"draft": "false",
"toc": true,
"title": "REG 파일 형식 - Windows 레지스트리 파일",
  "description":"REG 파일을 생성하고 열 수 있는 REG 형식과 API에 대해 알아보세요.",
"linktitle": "REG",
  "menu": {
    "docs": {
      "identifier": "system-reg",
"parent" : "system"
}
},
"lastmod": "2023-03-07"
}

## .REG 파일이란?

REG 파일은 Windows 레지스트리 데이터를 가져오거나 내보내는 데 사용되는 파일 형식입니다. Windows 레지스트리는 Windows 운영 체제 및 설치된 응용 프로그램에 대한 구성 설정 및 옵션을 저장하는 계층적 데이터베이스입니다. 레지스트리에는 사용자 기본 설정, 응용 프로그램 설정, 하드웨어 및 소프트웨어 구성 데이터 등과 같은 정보가 포함되어 있습니다.

REG 파일은 일반적으로 ".reg" 파일 확장자를 가지며 일련의 레지스트리 항목과 특정 형식의 값을 포함하는 일반 텍스트 파일입니다. 형식은 파일을 레지스트리 파일로 식별하는 헤더 섹션과 레지스트리 항목을 나타내는 일련의 키 및 값 쌍으로 구성됩니다.

## REG 파일 형식 - 추가 정보

다음은 reg 파일 형식의 예입니다.

```
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run]
"Example"="C:\\Example.exe"

[HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced]
"Hidden"=dword:00000001
```

파일의 첫 번째 줄은 레지스트리 편집기의 버전을 지정합니다. 다음 줄에는 키 경로 뒤에 값 이름과 값 데이터가 오는 형식의 레지스트리 항목이 포함되어 있습니다. 이 예에서 reg 파일에는 두 개의 항목이 포함되어 있습니다. 하나는 Windows 시작 목록에 "Example.exe"라는 프로그램을 추가하는 항목이고, 다른 하나는 Windows 탐색기 고급 설정에서 "Hidden" 값을 "true"로 설정하는 항목입니다.

Reg 파일은 메모장과 같은 텍스트 편집기를 사용하여 생성하고 편집할 수 있습니다. 이는 백업 및 복원 목적뿐만 아니라 동일한 레지스트리 설정으로 여러 컴퓨터를 구성하는 데 자주 사용됩니다.

## Windows 레지스트리 가져오기 또는 내보내기

REG 파일은 Windows 레지스트리에서 데이터를 가져오거나 내보내는 데 사용되는 파일 유형입니다. Windows 레지스트리는 Windows 운영 체제 및 설치된 응용 프로그램에 대한 구성 설정 및 옵션을 저장하는 계층적 데이터베이스입니다. 레지스트리에는 사용자 기본 설정, 응용 프로그램 설정, 하드웨어 및 소프트웨어 구성 데이터 등과 같은 정보가 포함되어 있습니다.

Reg 파일은 레지스트리 항목을 생성하거나 수정하는 데 사용할 수 있으며 백업 및 복원 목적뿐만 아니라 동일한 레지스트리 설정으로 여러 컴퓨터를 구성하는 데에도 자주 사용됩니다. reg 파일을 사용하여 Windows 레지스트리에 새 레지스트리 항목을 추가하는 방법은 다음과 같습니다.

1. 메모장과 같은 텍스트 편집기를 사용하여 새 텍스트 파일을 만듭니다.
2. 올바른 형식으로 레지스트리 항목을 입력합니다. 형식은 파일을 레지스트리 파일로 식별하는 헤더 섹션과 레지스트리 항목을 나타내는 일련의 키 및 값 쌍으로 구성됩니다. 예는 다음과 같습니다.

```
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\Software\Example]
"Setting1"="Value1"
```

그러면 현재 사용자 레지스트리 하이브의 "Software" 키 아래에 "Example"이라는 새 키가 생성되고 "Setting1" 값이 "Value1"로 설정됩니다.

3. .reg 파일 확장자로 파일을 저장합니다.
4. .reg 파일을 두 번 클릭하여 Windows 레지스트리에 새 레지스트리 항목을 추가합니다.

레지스트리에 항목을 추가할지 확인하는 메시지가 표시됩니다. 확인하면 새 항목이 레지스트리에 추가되며 레지스트리 편집기 도구를 사용하여 확인할 수 있습니다.

## 참고자료
* [Windows 레지스트리](https://en.wikipedia.org/wiki/Windows_Registry)

