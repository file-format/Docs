{
  "date" : "2023-05-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPIO 파일 - Unix CPIO 아카이브 파일 형식",
  "description":"CPIO 파일이 무엇인지, 그리고 CPIO 파일을 생성하고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "CPIO",
  "menu" : {
    "docs" : {
      "identifier" : "compression-cpio",
      "parent" : "compression"
}
},
  "lastmod" : "2023-05-10"
}

## .CPIO 파일이란?

CPIO 파일은 Unix의 CPIO(Copy In Copy Out) 형식으로 생성된 아카이브 파일입니다. 압축되지 않았다는 점을 제외하면 TAR 파일 형식과 유사합니다. CPIO 파일은 장치 파일, 심볼릭 링크 및 확장 파일 속성을 저장할 수 있습니다.

## CPIO 파일 형식

CPIO 아카이브는 사람이 읽을 수 없는 바이너리 파일로 생성됩니다. 파일 및 디렉토리 모음을 저장합니다. CPIO 아카이브의 콘텐츠는 파일 이름, 권한, 소유권, 타임스탬프 등의 메타데이터 정보로 식별됩니다. 이 메타데이터 정보는 시스템의 측면 액세스를 위해 아카이브 파일에도 저장됩니다.

## CPIO 아카이브 형식

CPIO 파일은 하나 이상의 연결된 멤버 파일로 구성됩니다. 아카이브의 각 파일은 헤더에 언급된 파일 내용이 선택적으로 뒤따르는 헤더로 구성됩니다. 아카이브의 끝에는 TRAILER!!라는 빈 파일로 설명되는 또 다른 헤더가 포함되어 있습니다.

### CPIO 아카이브 유형

CPIO 아카이브에는 두 가지 유형이 있습니다. 헤더 스타일만 다릅니다.

* ASCII 아카이브 - 이 CPIO 아카이브에는 아카이브 자체가 ASCII 파일로 구성된 경우 CPIO 아카이브의 일부가 되는 인쇄 가능한 헤더가 있습니다.
* 바이너리 아카이브 - 이 CPIO 아카이브에는 바이너리 헤더가 있습니다.

## CPIO 아카이브 작업

### CPIO 아카이브를 만드는 방법은 무엇입니까?

**cpio** 명령을 사용하여 Unix 계열 시스템에서 CPIO를 생성할 수 있습니다. 다음 명령은 현재 디렉터리와 해당 하위 디렉터리에 있는 모든 파일과 디렉터리를 찾습니다. 그런 다음 이 출력은 archive.cpio라는 새 CPIO 아카이브를 생성하는 cpio 명령으로 파이프됩니다.

```
find . -depth -print | cpio -ov > archive_cpio.cpio
```
### CPIO 아카이브에서 파일을 추출하는 방법은 무엇입니까?

다음 명령은 기존 아카이브에서 파일을 추출합니다.

```
cpio -id < archive_cpio.cpio
```
표준 입력에서 archive.cpio 파일을 읽고 파일을 현재 디렉터리에 추출합니다.


## 참고자료

* [CPIO - 위키피디아 작성](https://en.wikipedia.org/wiki/Cpio)
* [CPIO 파일 형식](https://www.ibm.com/docs/en/zos/2.2.0?topic=formats-cpio-format-cpio-archives)

