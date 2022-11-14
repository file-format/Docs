{
  "date" : "2021-07-25",
  "keywords":["man","file", "extension", "type", "format", "Unix Manual"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAN - 유닉스 매뉴얼",
  "description":"MAN 파일을 만들고 열 수 있는 FODT 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "MAN",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-25"
}

## .MAN 파일이란?

.man 확장자를 가진 파일은 소프트웨어 문서 형식의 Unix 프로그래밍 사용자 매뉴얼인 매뉴얼 페이지를 나타냅니다. 설명서를 보는 데 사용되는 Unix에 포함된 'Man' 유틸리티에서 사용합니다. 소프트웨어 설명서에는 명령을 실행하여 명령 터미널에서 Man 유틸리티를 사용하여 검색할 수 있는 섹션 및 페이지의 정보가 포함되어 있습니다. 컴퓨터에서 문서의 소프트 카피로 사용할 수 있으므로 액세스하기 위해 인쇄된 사본이나 인터넷 연결이 필요하지 않습니다.

## Unix 매뉴얼 Man 파일 형식 - 추가 정보

매뉴얼 페이지는 일반 텍스트 형식으로 저장되며 보거나 편집하기 위해 모든 텍스트 편집기에서 만들고 열 수 있습니다. UNIX에서는 매뉴얼의 섹션 및 페이지 번호에 대한 참조를 포함하는 터미널에서 명령을 실행하여 매뉴얼 페이지의 정보를 검색합니다.

### 섹션 및 페이지

Unix man은 명령에 대한 각 페이지 인수가 프로그램, 유틸리티 또는 기능의 이름을 참조하는 시스템 설명서입니다. 명령이 섹션 정보와 함께 제공된 경우 해당 특정 섹션에서 페이지를 검색합니다. 그러나 기본 동작은 모든 섹션에서 페이지를 검색하고 여러 섹션에 있는지 여부에 관계없이 첫 번째 페이지를 표시하는 것입니다.

### 섹션 번호

다음은 매뉴얼의 섹션 번호와 포함된 페이지 유형에 대한 정보입니다.

|섹션 번호|페이지 유형|
---|---|
|1|실행 프로그램 또는 쉘 명령|
|2|시스템 호출(커널에서 제공하는 기능)|
|3|라이브러리 호출(프로그램 라이브러리 내의 함수)|
|4|특수 파일(보통 /dev에 있음)|
|5|파일 형식 및 규칙, 예: /etc/passwd|
|6|게임|
|7|기타(매크로 패키지 및 규칙 포함), 예: man(7), groff(7)|
|8|시스템 관리 명령(일반적으로 루트에만 해당)|
|9|커널 루틴 [비표준]|

## 예 - MAN 페이지를 읽는 방법?

다음은 Man 명령을 사용하여 MkDir 명령에 대한 정보를 검색하는 방법의 예입니다.

```
% man mkdir

MKDIR(1)    USER COMMANDS       MKDIR(1)

NAME
   mkdir - make a directory

SYNOPSIS
   mkdir [ -p ] dirname...

DESCRIPTION
   mkdir creates directories. Standard entries,`.',for the
   directory itself, and `..' for its parent, are made automat-
   ically.

   The -p flag allows missing parent directories
   to be created as needed.

   With the exception of the set-gid bit, the
   current umask(2V) setting determines the mode in which
   directories are created. The new directory inherits the set-gid
   bit of the parent directory. Modes may be modified after
   creation by using chmod(1V).

   mkdir requires write permission in the parent directory.

SEE ALSO
   chmod(1V), rm(1), mkdir(2v), umask(2V)
```

## 참고문헌

* [OpenDocument 기술 사양 - Wikipedia 작성](https://en.wikipedia.org/wiki/OpenDocument_technical_specification)
* [man(1) — 리눅스 매뉴얼 페이지](https://man7.org/linux/man-pages/man1/man.1.html)

