{
  "date" : "2019-10-11",
  "keywords" :[ ".mel", "Maya 임베디드 언어","파일", "확장자", "파일 형식", "Maya 3D", "프로그래밍 가이드"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MEL - Maya 임베디드 언어 파일 형식",
  "description":"MEL 파일을 만들고 열 수 있는 MEL 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "MEL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-03-08"
}

## .MEL 파일이란?

.mel(Maya Embedded Language) 확장자를 가진 파일은 Autodesk Maya에서 그래픽 인터페이스를 만드는 데 사용하는 스크립팅 언어입니다. Maya의 그래픽 인터페이스 외에 실행 가능한 스크립트를 사용하여 그래픽 요소 생성을 자동화할 수 있습니다. MEL을 사용하면 프로그래밍을 배우지 않고도 그래픽 인터페이스를 만들 수 있습니다. 이는 반복 작업의 속도를 높이는 매크로 및 사용자 지정 작업을 생성하여 달성됩니다. 이러한 절차와 스크립트를 사용하여 사용자 지정 모델링, 애니메이션, 역학 및 작업 렌더링을 만들 수 있습니다. Autodesk Maya 2020을 사용하여 EML 파일의 내용을 열고 볼 수 있습니다.

## MEL 파일 형식 - 추가 정보

프로그래머의 [참조 매뉴얼](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)은 Maya의 문서 섹션에서 개발자를 위해 제공됩니다. MEL은 UINX와 유사한 쉘 스크립팅 명령을 기반으로 하여 작업을 수행합니다. 스크립팅 기반 명령은 기존의 객체 지향 프로그래밍(OOP)과 관련이 없으므로 데이터 구조를 사용하지 않거나 함수를 호출하거나 다른 언어에서처럼 OOP를 사용하지 않습니다.

MEL에 대한 몇 가지 핵심 사항은 다음과 같습니다.

`Comments` - MEL의 모든 문장은 블록의 끝에서도 세미콜론(;)으로 끝나야 합니다.

`Returning Values` - 값을 반환하는 표현식을 지정하면 MEL에서 값이 자동으로 인쇄되지 않습니다. 대신 오류가 발생합니다.
```
3 + 5;
// Error: 3 + 5; //
// Error: Syntax error //
print(3+5);
8
```
`생성, 편집 및 삭제 명령` - 동일한 명령을 사용하여 사물을 만들거나 편집하거나 기존 사물에 대한 정보를 쿼리합니다. 그러나 플래그는 명령이 수행하는 작업(생성, 편집 또는 쿼리)을 제어합니다.

```
// Create a sphere named "mySphere" with radius 5
sphere -radius 5 -name "mySphere";
// Edit the radius of mySphere
sphere -edit -radius "mySphere";
// Print the radius of mySphere
sphere -query -radius

```
`함수에서 값 반환` - 함수 구문은 자동으로 값을 반환합니다. 명령 구문을 사용하여 반환 값을 얻으려면 명령을 역따옴표로 묶어야 합니다.

```
$a = getAttr("mySphere.translateX"); // Function syntax
$b = `getAttr mySphere.translateY`; // Command syntax
```

## 참고문헌

* [MEL](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)

