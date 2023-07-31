{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDMP 파일 - Windows 힙 덤프 파일 형식",
  "description":"HDMP 파일을 만들고 열 수 있는 HDMP 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "HDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## .HDMP 파일이란?

HDMP 파일은 오류로 인해 응용 프로그램이나 프로그램이 충돌할 때 압축되지 않은 메모리 덤프입니다. 그것은 Windows XP/Vista에 의해서만 생성되며 충돌했을 때 응용 프로그램 상태의 덤프를 포함합니다. 압축되지 않은 HDMP 파일은 보고 목적으로 압축된 Minidump [MDMP](/ko/system/mdmp/) 파일에 비해 디스크에서 더 많은 공간을 차지합니다.

HDMP 파일 **열기** 또는 분석에 사용할 수 있는 응용 프로그램에는 Windows용 디버깅 도구가 포함된 Microsoft Visual Studio가 있습니다.

## HDMP 파일 형식

HDMP 파일은 이진 파일로 디스크에 저장되며 적절한 응용 프로그램 없이 열면 아무런 이점이 없습니다. 여기에는 오류가 발생했을 때 기록된 관련 시스템 데이터가 포함됩니다.

### HDMP와 MDMP 파일 형식의 차이점

HDMP는 압축되지 않은 메모리 덤프 파일입니다. 대조적으로 MDMP는 파일 크기를 줄이기 위해 압축되어 문제를 보고하기 위해 Microsoft에 보내는 미니 덤프 파일입니다.

## 참조 ##

* [DMP - 마이크로소프트](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

