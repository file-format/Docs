{
  "date" : "2022-06-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SY_ 파일 형식 - 압축된 SYS 파일",
  "description":"SY_ 파일 형식과 SY_ 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "SY_",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-24"
}

## SY_ 파일이란?

SY_ 파일은 소프트웨어 설치 프로그램이 설치 프로그램 내부에 패키지된 설치 파일의 크기를 줄이기 위해 사용하는 압축된 .sys 파일입니다. 이렇게 하면 설치 프로그램의 전체 크기가 줄어듭니다. SY_ 파일은 하나 이상의 압축 파일을 확장하는 Microsoft Expand 명령줄 유틸리티를 사용하여 확장할 수 있습니다.

## SY_ 파일 형식 - 추가 정보

SY_ 파일은 압축된 바이너리 파일로 디스크에 저장됩니다. 그러나 내부 파일 형식은 공개적으로 사용할 수 없습니다. Microsoft Expand 명령줄 유틸리티는 다음 명령줄 중 하나를 사용하여 SY_ 파일을 확장할 수 있습니다.

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
확장하면 SY_ 파일이 [SYS](https://docs.fileformat.com/system/sys/) 파일로 변환됩니다.

SY_ 파일은 EX_ 및 DL_ 파일과 유사합니다.

## 참고문헌

* [StuffIt - 위키피디아 작성](https://en.wikipedia.org/wiki/StuffIt)
* [마이크로소프트 익스팬드](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/expand)

