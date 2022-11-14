{
  "date" : "2021-06-29",
  "keywords" :[ "com 파일", "com 파일이란", "파일", "com 예제", "com 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"COM 파일을 만들고 열 수 있는 COM 파일 형식과 API에 대해 알아보세요.",
  "title" :"COM - DOS 명령 파일 형식",
  "linktitle" : "COM",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-29"
}

## .COM 파일이란?
COM 파일은 단순히 일련의 명령이나 명령을 실행하는 데 사용됩니다. COM 파일은 Windows 또는 MS-DOS에서 실행할 수 있는 실행 프로그램으로 구성됩니다. EXE 파일과 마찬가지로 COM 파일도 바이너리 형식으로 저장되지만 헤더나 메타데이터가 없고 최대 크기가 약 64KB라는 점에서 EXE 파일과 다릅니다. COM 파일이 32비트 시스템에서 처음 실행되면 NTVDM(NT Virtual DOS Machine) 구성 요소를 설치하라는 메시지가 나타납니다. COM 파일은 MS-DOS 환경을 지원하는 가상 머신이 있는 64비트 버전의 Microsoft Windows에서 실행할 수 있습니다.

## COM 파일 형식
COM 파일 형식은 Microsoft Windows 또는 MS-DOS에서 사용되는 바이너리 실행 형식입니다. 그 구조는 일련의 지침으로 구성됩니다. 헤더가 없고 표준 메타데이터가 포함되어 있지 않습니다. 모든 데이터와 코드를 하나의 세그먼트에만 저장하고 바이너리의 최대 크기는 64KB입니다. 이 파일 형식은 재실행을 시도할 때 자체 재배치되지 않습니다. 따라서 운영 체제는 미리 설정된 주소에서 로드합니다. 또한 COM 파일을 **fat 바이너리** 형식으로 두 운영 체제에서 모두 실행할 수 있습니다. 명령 수준에서는 실제 호환성이 없습니다. 진입점의 명령어는 기능면에서 동일하지만 두 운영 체제에서 다르도록 선택되며 프로그램을 실행하고 사용 중인 운영 체제 섹션으로 점프합니다. 기본적으로 사용할 파일을 선택하는 코드가 선행되는 단일 파일에 동일한 절차를 가진 두 개의 다른 프로그램입니다.
### COM 파일 예
COM 파일을 실행할 때 명령은 첫 번째 바이트에서 읽고 마지막 명령을 찾을 때까지 연속적으로 따릅니다. 다음은 ASM 코드 예입니다.

```
[BITS 16]		;Set code generation to 16 bit mode
[ORG 0x0100]		;Set code start address to 0100h


[SEGMENT .text]		;Main code segment
    mov ah, 9 ; DOS print string function
    mov dx, hello
    int 21h
    ;Exit to DOS
    mov ah, 4ch
    int 21h
[SEGMENT .data]		;Initialised data segment
hello:   db   'Hello, .COM programmer!',13,10,'$'
```

## 참고문헌

* [COM 파일 - Wikipewdia 제공](https://en.wikipedia.org/wiki/COM_file)

