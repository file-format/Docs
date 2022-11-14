{
  "date" : "2019-10-11",
  "keywords": [ "mf file", "mf", "extension", "format", "mf file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MF - 자바 매니페스트 파일 형식",
  "description":"MF 파일 형식과 MF 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "MF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## .MF 파일이란?

확장자가 .mf인 파일은 개별 [JAR](/ko/programming/jar/) 파일 항목에 대한 정보를 포함하는 Java 매니페스트 파일입니다. MF 파일 자체는 JAR 파일 내부에 포함되어 있으며 모든 확장 및 패키지 관련 정의를 제공합니다. JAR 파일을 생성하여 실행 파일로 사용할 수 있습니다. 이 경우 메인페스트 파일은 **`public static void main`** 문을 포함하는 애플리케이션의 메인 클래스를 지정합니다. 매니페스트 파일의 이름은 MANIFEST.MF이며 Windows, MacOS 및 Linux 운영 체제의 모든 텍스트 편집기로 열 수 있습니다.

## 매니페스트 파일 형식 사양

[매니페스트 파일 형식 사양](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html)은 JAR 파일 형식에 대한 가이드에서 Oracle에서 사용할 수 있습니다. 매니페스트 파일은 개별 JAR 파일 항목에 대한 섹션 목록이 뒤따르는 주요 섹션으로 구성됩니다. 각 섹션은 몇 가지 규칙과 제한 사항을 따릅니다.

### 주요 섹션

주요 섹션:

* JAR 파일에 대한 보안 및 구성에 대한 정보를 포함합니다.
* JAR 파일이 속한 응용 프로그램 또는 확장에 대한 정보를 포함합니다.
* 각 개별 매니페스트 항목의 주요 속성을 정의합니다.

**참고**: 이 섹션의 속성에는 "이름"이라는 이름을 지정할 수 없습니다.

### 개별 섹션

개별 섹션은 JAR 파일의 패키지 또는 파일에 대한 다양한 속성을 정의합니다. 각 섹션은 값이 파일에 대한 상대 경로이거나 아카이브 외부의 데이터를 참조하는 절대 URL이어야 하는 "이름"이라는 속성으로 시작해야 합니다.

### 매니페스트 사양

|속성|설명|
---|---|
|매니페스트 파일|주 섹션 개행 *개별 섹션|
|주 섹션|버전 정보 줄 바꿈 *주 속성|
|버전 정보|매니페스트 버전: 버전 번호|
|버전 번호|숫자+{.숫자+}*|
|main-attribute|(모든 합법적인 기본 속성) 개행|
|individual-section|이름 : 값 개행 *perentry-attribute|
|perentry-attribute|(적법한 perentry 속성) 개행|
|newline|CR LF | LF | CR(LF가 뒤따르지 않음)|
|숫자|{0-9}|

## 참고문헌

* [오라클 - JAR 파일 형식](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html)
* [JAR 파일 형식](https://en.wikipedia.org/wiki/JAR_(file_format)#:~:text=A%20JAR%20(Java%20ARchive)%20is,into%20one%20file%20for% 20distribution.&text=%20are%20built%20on%20the,jar%20file%20extension.)

