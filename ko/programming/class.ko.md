{
  "date" : "2019-10-11",
  "keywords" :[ "클래스", ".class","클래스 파일이란","클래스 파일을 여는 방법", "확장자", "파일", "클래스 파일","클래스 파일 형식", ".class 확장자 ", "자바의 클래스 파일"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"클래스 - Java 클래스 파일 형식",
  "description":"클래스 파일을 만들고 열 수 있는 클래스 파일 형식 및 API에 대해 알아보세요.",
  "linktitle" : "Class",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## 클래스 파일이란?

**Class file in Java**는 실제로 JVM(Java Virtual Machine)에서 실행되는 [.java](/ko/programming/java/) 클래스의 컴파일된 출력입니다. 클래스 파일은 개별적으로 실행될 수 있을 뿐만 아니라 다른 패키지 파일과 함께 번들로 [JAR](/ko/programming/jar/) 파일의 일부가 될 수 있습니다. 이는 명령줄 인터페이스에서 **`javac`** 명령을 사용하여 만들 수 있습니다. [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/eclipse-ide-java-developers) 및 NetBeans와 같은 일부 Java IDE는 프로젝트의 Java에서 .class 출력 파일 생성을 제공합니다. 파일.

## 클래스 파일 형식

Java 클래스 파일은 JVM에서 실행되는 중간 코드인 바이트 코드로 구성됩니다. 클래스 파일은 8비트 바이트 스트림으로 구성되며 멀티바이트 데이터 항목은 항상 빅엔디안 순서로 저장됩니다.

### 클래스 파일 구조

클래스 파일 구조는 아래와 같습니다.
```
ClassFile {
    u4             magic;
    u2             minor_version;
    u2             major_version;
    u2             constant_pool_count;
    cp_info        constant_pool[constant_pool_count-1];
    u2             access_flags;
    u2             this_class;
    u2             super_class;
    u2             interfaces_count;
    u2             interfaces[interfaces_count];
    u2             fields_count;
    field_info     fields[fields_count];
    u2             methods_count;
    method_info    methods[methods_count];
    u2             attributes_count;
    attribute_info attributes[attributes_count];
}
```
어디:

* u1 = 부호 없는 1바이트 수량
* u2 = 부호 없는 2바이트 수량
* u4 = 부호 없는 4바이트 수량

.class 파일 구조에 대한 자세한 내용은 Oracle [클래스 파일 형식](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)에 설명되어 있으며 다음에서 참조할 수 있습니다. 참고로 개발자. 이러한 필드의 요약은 다음과 같습니다.

* `magic` - 매직 항목은 클래스 파일 형식을 식별하는 매직 번호를 제공합니다. 값은 0xCAFEBABE입니다.
* `minor_version`, `major_version` - minor_version 및 major_version 항목의 값은 이 클래스 파일의 부 및 주 버전 번호입니다.
* `constant_pool_count` - constant_pool_count 항목의 값은 constant_pool 테이블의 항목 수에 1을 더한 값과 같습니다. constant_pool 인덱스는 long 및 double 유형의 상수를 제외하고 0보다 크고 constant_pool_count보다 작은 경우 유효한 것으로 간주됩니다.
* `constant_pool[]` - constant_pool은 다양한 문자열 상수, 클래스 및 인터페이스 이름, 필드 이름 및 ClassFile 구조 및 해당 하위 구조 내에서 참조되는 기타 상수를 나타내는 구조 테이블(§4.4)입니다. 각 constant_pool 테이블 항목의 형식은 첫 번째 "태그" 바이트로 표시됩니다.
* `access_flags` - access_flags 항목의 값은 이 클래스 또는 인터페이스의 액세스 권한 및 속성을 나타내는 데 사용되는 플래그 마스크입니다.
* `this_class` - this_class 항목의 값은 constant_pool 테이블에 대한 유효한 인덱스여야 합니다.
* `super_class` - 클래스의 경우 super_class 항목의 값은 0이거나 constant_pool 테이블에 대한 유효한 인덱스여야 합니다.
* `interfaces_count` - interface_count 항목의 값은 이 클래스 또는 인터페이스 유형의 직접 수퍼 인터페이스 수를 제공합니다.
* `interfaces[]` - 인터페이스 배열의 각 값은 constant_pool 테이블에 대한 유효한 인덱스여야 합니다.
* `fields_count` - fields_count 항목의 값은 fields 테이블에 있는 field_info 구조의 수를 제공합니다.
* `fields[]` - fields 테이블의 각 값은 이 클래스 또는 인터페이스의 필드에 대한 완전한 설명을 제공하는 field_info 구조여야 합니다.
* `methods_count` - methods_count 항목의 값은 methods 테이블에 있는 method_info 구조의 수를 제공합니다.
* `methods[]` - 메소드 테이블의 각 값은 이 클래스 또는 인터페이스의 메소드에 대한 완전한 설명을 제공하는 method_info 구조여야 합니다. method_info 구조의 access_flags 항목에 ACC_NATIVE 및 ACC_ABSTRACT 플래그가 모두 설정되지 않은 경우 해당 메소드를 구현하는 Java Virtual Machine 명령도 제공됩니다.
* `attributes_count` - attributes_count 항목의 값은 이 클래스의 속성 테이블에 있는 속성의 수(§4.7)를 제공합니다.
* `attributes[]` - 속성 테이블의 각 값은 attribute_info 구조여야 합니다.




## 참고문헌

* [클래스 파일 형식](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)

