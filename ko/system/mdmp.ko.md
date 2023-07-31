{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MDMP 파일 - Windows 미니 덤프 파일 형식",
  "description":"MDMP 파일 형식과 MDMP 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "MDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## .MDMP 파일이란?

MDMP 파일은 Microsoft Windows에서 응용 프로그램이 비정상적으로 닫히거나 충돌할 때 생성되는 응용 프로그램의 메모리 덤프입니다. 여기에는 충돌 원인을 디버그하는 데 사용할 수 있는 정보 및 데이터 덤프가 포함되어 있습니다. MDMP 파일은 Java, C++, .NET 등과 같은 모든 플랫폼에서 만든 응용 프로그램에 적용할 수 있습니다. MDMP 외에도

MDMP 파일을 열 수 있는 응용 프로그램에는 Microsoft Visual Studio Debugger가 있습니다.

## MDMP 파일 형식

MDMP 파일은 디스크에 바이너리 파일로 저장되며 Microsoft Visual Studio 디버거로 열 수 있습니다. 충돌 원인을 식별하는 데 도움이 되는 다음 정보가 포함되어 있습니다.

* 중지 메시지, 매개변수 및 기타 데이터의 세부사항
* 로드된 드라이버 목록
* 작동을 멈춘 프로세서에 대한 프로세서 컨텍스트(PRCB)
* 중지된 프로세스에 대한 프로세스 정보 및 커널 컨텍스트(EPROCESS)
* 중지된 스레드에 대한 프로세스 정보 및 커널 컨텍스트(ETHREAD)
* 중지된 스레드에 대한 커널 모드 호출 스택

이 정보는 무슨 일이 일어났는지 알아내고, 문제를 수정하고, 재발을 방지하는 데 도움이 됩니다.

### 미니덤프 분석

Windows에서 메모리 덤프 파일을 생성하려면 부팅 볼륨에 페이징 파일이 필요합니다. 페이징 파일은 부팅 볼륨에 생성되며 크기는 2MB 이상이어야 합니다. 덤프 파일은 응용 프로그램이 충돌할 때 생성됩니다. 두 번째 문제의 경우 이전 파일이 유지되는 동안 두 번째 작은 메모리 덤프 파일이 생성됩니다. 덤프 파일의 이름은 덮어쓰기를 방지하기 위해 고유합니다.

Windows는 모든 메모리 덤프 파일 목록을 %SystemRoot%\Minidump 폴더에 보관합니다. 아래 단계에 나열된 대로 Visual Studio 디버거에서 MDMP 파일을 실행하여 분석할 수 있습니다.

## Visual Studio에서 MDMP 파일을 어떻게 열 수 있습니까?

다음 단계를 사용하여 Visual Studio에서 MDMP 파일을 열 수 있습니다.

* Visual Studio의 파일 메뉴에서 열기 | 크래시 덤프 .
* 열려는 덤프 파일로 이동합니다.
* 열기를 선택합니다.

## 참조

* [크래시 발생 시 Windows에서 생성되는 작은 메모리 덤프 파일을 읽는 방법](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump -파일)

