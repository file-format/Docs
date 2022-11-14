{
  "date" : "2021-07-12",
  "keywords" :[ "cmd 파일", "cmd 파일이란", "파일", "cmd 예제", "cmd 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"CMD 파일을 만들고 열 수 있는 CMD 파일 형식과 API에 대해 알아보세요.",
  "title" :"CMD - Windows 명령 파일 형식",
  "linktitle" : "CMD",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-07-12"
}

## .CMD 파일이란?
CMD 파일은 다양한 작업을 실행하기 위해 실행되는 일반 텍스트 형태의 하나 이상의 명령을 포함하는 스크립트로 구성됩니다. [BAT](/ko/executable/bat/) 파일과 유사하며 일반적으로 실행 가능한 명령의 배치를 저장하는 데에도 사용됩니다. CMD 파일은 Microsoft Windows 운영 체제에서 널리 사용됩니다. 이 파일은 거의 90년대에 도입되었지만 여전히 최신 Windows 운영 체제에서 사용됩니다. 이러한 파일은 일반적으로 시퀀스에서 둘 이상의 명령을 실행하도록 작성됩니다.

## CMD 파일 형식
CMD는 CP/M 스타일 실행 프로그램에서 사용하는 파일 형식입니다. 일반적으로 CP/M-80의 [COM](/ko/executable/com/) 및 DOS의 [EXE](/ko/executable/exe/)와 비슷합니다. CMD 파일에는 1~8개의 코드 또는 데이터 그룹과 128바이트 헤더가 포함됩니다. 각 그룹의 크기는 최대 1MB입니다. CMD 파일에는 재배치 정보와 이후 버전의 RSX(Resident System Extensions)도 포함될 수 있습니다. CMD는 [BAT](/ko/executable/bat/) 파일과 비교하여 새로운 기능입니다. MS-DOS에서 Windows가 출시되기 전에 MS-DOS에 사용되었습니다. 오늘날에도 .bat 확장자로 파일을 저장할 수 있지만 많은 사람들이 .cmd 확장자를 사용하여 실행 스크립트를 저장합니다.

### CMD 형식 사양

헤더의 시작 부분에는 해당 유형과 함께 파일에 있는 그룹 목록이 포함됩니다. 각 유형은 최대 한 번만 사용할 수 있습니다. 이러한 유형은 다음과 같습니다.

- 코드
- 데이터
- 추가의
- 스택
- 사용자 1
- 사용자 2
- 사용자 3
- 사용자 4
- 공유 코드

마찬가지로 DOS의 프로그램 세그먼트 접두사에서 데이터 그룹의 처음 256바이트는 0입니다. CP/M-86에 의해 0페이지로 채워집니다. 데이터 그룹이 없으면 코드 그룹의 처음 256바이트가 대신 사용됩니다.
## CMD 파일 예
다음은 시스템 정보를 표시하는 CMD 스크립트의 예입니다.
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## 참고문헌

* [CMD 스크립트 작성 방법](https://smallbusiness.chron.com/write-cmd-script-53226.html)
* [CMD 파일(CP/M) - 위키피디아 제공](https://en.wikipedia.org/wiki/CMD_file_(CP/M))

