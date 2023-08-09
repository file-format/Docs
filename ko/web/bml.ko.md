{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BML 파일 형식 - Bean 마크업 언어 파일",
  "description":"BML 파일 형식과 BML 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "BML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-12"
}

## .BML 파일이란?

확장자가 .bml인 파일은 Java 앱을 지원하기 위한 Java 클래스를 저장하는 Bean Markup Language 파일입니다. 이를 통해 Java 개체 및 메서드에 액세스할 수 있으며 Java 클래스를 사용하여 새 기능을 만들 필요가 없습니다. 유용한 작업을 수행하기 위해 구성 요소가 서로 연결되는 방식을 지정합니다. BML은 구조 및 구성요소 관계를 설명하기 위해 IBM alphaWorks에서 개발했습니다. BML 파일은 웹 브라우저, Microsoft 메모장 및 메모장++과 같은 텍스트 편집기를 사용하여 열고 볼 수 있습니다.

## BML 파일 형식

IBM alphaworks 웹 사이트는 두 가지 BML 구현을 제공했습니다. 첫 번째 구현은 원하는 빈 계층 구조를 생성하기 위한 BML 스크립트를 '재생'하는 인터프리터입니다. 두 번째 구현은 모든 BML 스크립트를 반사 없는 Java 코드로 컴파일하는 컴파일러입니다. 이는 '일반' Java 코드로 컴파일하는 기능이 추가된 특정 목적을 위해 설계된 언어를 사용하여 애플리케이션의 구성요소 간 구조를 캡처할 수 있다는 점에서 유리합니다.

## BML 태그

다음은 BML 언어에서 사용되는 일부 태그에 대한 설명입니다.

###<bean> 꼬리표:

그만큼<bean> 요소는 새 빈을 생성하거나 이름으로 빈을 찾는 데 사용됩니다. 그만큼<bean> 태그 형식은 다음과 같습니다.
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
태그의 "id"는 JavaBean의 개체 레지스트리와 연결됩니다.

###<string> 꼬리표

문자열 태그를 사용할 수 있는 두 가지 방법이 있습니다.

1. 비어 있지 않은 문자열을 생성하려면:

```
<string [value = "value of string"]> [value of string]
</string>
```
2. 빈 문자열을 생성하려면:

```
<string/>
```
## 참고문헌

* [XML을 사용한 객체 지향 메시징](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [물리적 마크업 언어](http://web.mit.edu/mecheng/pml/standards.htm)


