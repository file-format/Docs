{
  "date" : "2019-10-11",
  "keywords" :[ "JAR", ".jar","jar 파일이란","jar 파일을 여는 방법", "확장자", "파일", "jar 파일","jar 파일 형식", ".jar 확장자 " ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JAR - 자바 아카이브 파일 형식",
  "description":"JAR 파일을 만들고 열 수 있는 JAR 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "JAR",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## .JAR 파일이란?

확장자가 .jar인 파일은 다양한 애플리케이션 관련 파일을 단일 파일로 포함하는 Java 아카이브 파일입니다. 이 파일 형식은 여러 HTTP 연결을 생성하지 않도록 하여 HTTP 트랜잭션을 통해 브라우저에서 다운로드한 Java 애플릿을 로드하는 속도를 줄이기 위해 생성되었습니다. 단일 JAR 파일에는 Java 클래스 파일([.class](/ko/programming/class/)), [images](/ko/image/) 및 [sounds](/ko/audio/)가 포함될 수 있습니다. JAR 파일 내의 개별 항목은 원본을 인증하기 위해 응용 프로그램 개발자가 디지털 서명할 수 있습니다. JAR 파일은 해당 API와 관련된 특정 기능을 포함하는 기능적 API를 만드는 데 정기적으로 사용됩니다.

## JAR 파일 형식

JAR 파일은 개별 콘텐츠 파일을 단일 파일에 보관하는 인기 있는 [ZIP 파일 형식](/ko/compression/zip/)을 기반으로 합니다. JAR 파일 형식은 압축을 지원하므로 다운로드할 파일 크기가 작아지므로 다운로드 시간이 더욱 향상됩니다. Oracle의 [JAR 파일 사양](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) 기사는 JAR 파일의 내부 사양에 대한 완전한 세부 정보를 제공합니다.

### 매니페스트 파일

JAR 파일이 생성되면 JAR 파일의 내용에 대한 메타데이터 정보가 포함된 매니페스트 파일이 내부에 자동으로 생성됩니다. 이 파일은 JAR 파일 내부에 패키징된 내용을 보여줍니다. JAR 파일에 포함된 폴더와 클래스를 보여주는 일반적인 매니페스트 파일은 다음과 같습니다.

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### 매니페스트 사양

매니페스트 사양은 Oracle에서 다음과 같이 정의합니다.

`manifest-file`: 메인 섹션 줄 바꿈 \*개별 섹션

`main-section`: 버전 정보 줄 바꿈 \*main-attribute

`version-info`: 매니페스트-버전: 버전 번호

`버전 번호` : 숫자+{.숫자+}*

`main-attribute`: (모든 합법적인 기본 속성) 개행

`individual-section`: 이름: 값 개행 \*perentry-attribute

`perentry-attribute`: (적법한 perentry 속성) 개행

`줄 바꿈` : CR LF | LF | CR(LF가 뒤따르지 않음)

`digit`: {0-9}

### 실행 가능한 JAR

JAR 파일은 Microsoft Windows 운영 체제의 다른 응용 프로그램과 유사한 JVM(Java Virtual Machine)에서 실행할 수 있는 응용 프로그램으로 구성될 수도 있습니다. 이 경우 JVM은 public static void main 메소드가 있는 모든 클래스인 애플리케이션의 진입점에 대해 알아야 합니다. 매니페스트 파일은 다음 형식의 'Main-Class' 헤더로 이러한 클래스를 식별합니다.

```
Main-Class: com.example.MyClassName
```



## 참고문헌

* [JAR 파일 개요](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
* [JAR 파일 형식](https://en.wikipedia.org/wiki/JAR_(file_format)#:~:text=A%20JAR%20(Java%20ARchive)%20is,into%20one%20file%20for% 20distribution.&text=%20are%20built%20on%20the,jar%20file%20extension.)

