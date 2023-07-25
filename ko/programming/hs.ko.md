{
  "date" : "2021-04-21",
  "keywords": [ "what is a HS file", "tutorials on HS","HS means","HS", "HS files", "extension", "format", "HS tutorial", ".hs", "HS example","hs file extension" ,"how to open a hs file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HS - Haskell 스크립트 파일 형식",
  "description":"HS 파일 형식과 HS 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "HS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-15"
}

# HS - Java HelpSet 파일 형식

## 자바 HS 파일이란?

Java 프로그래밍 언어에서 확장자가 .hs인 파일은 응용 프로그램에서 활성화할 때 JavaHelp 시스템에서 사용하는 도움말 문서 파일입니다. 설치된 특정 응용 프로그램에 대한 도움말 집합을 정의하고 응용 프로그램에 대한 시스템 도움말의 일부로 여러 하위 집합으로 구성됩니다. Java 프로그램은 이름이 .hs 확장자로 끝나는 도움말 집합 파일을 찾을 수 있어야 합니다.

## 자바 도움말 정보

.hs 파일에는 다음 정보가 포함될 수 있습니다.

|정보|설명|
---|---|
|맵 파일|맵 파일은 토픽 ID를 하이퍼텍스트 마크업 언어 토픽 파일의 경로 이름 또는 통일 자원 로케이터와 연관시키는 데 사용됩니다.|
|정보 보기|도움말 세트 내에서 사용 중인 네비게이터를 설명하는 정보입니다. 품질 내비게이터는 목차, 색인 및 전체 텍스트 검색입니다. 추가 내비게이터에는 광택 및 즐겨찾기 내비게이터가 포함됩니다. 커스텀 내비게이터에 관한 데이터는 여기에 추가로 동봉되어 있습니다.|
<html>|도움말 제목|\<title> 도움말 세트(.hs) 파일에 설명되어 있습니다. 이 제목은 가장 높은 창과 도움말 집합 파일에 설명된 모든 보조 창에서 가장 높은 것 같습니다.| </html>
|홈 ID|ID를 표시하지 않고 지원 감시자가 호출될 때 표시되는 (기본) ID의 제목입니다.|
|프레젠테이션|지원 주제를 표시하는 창입니다. 이것은 \<presentation> .|
|Sub-helpsets|이 임의 영역은 태그를 활용하여 다른 helpsets를 정적으로 통합합니다. 이 태그로 표시되는 도움말 집합은 태그가 포함된 도움말 집합에 자연스럽게 결합됩니다. 블렌딩에 대한 더 많은 관심 사항은 Blending Helpsets에서 찾을 수 있습니다.|
|구현|이 임의의 세그먼트는 HelpSet.createHelpBroker 메서드 내에서 사용할 HelpBroker 클래스를 특성화하기 위해 키 정보 매핑을 제공하는 레지스트리를 만듭니다. 또한 레지스트리는 주어진 에뮬레이트 정렬에 대해 클라이언트에 대한 물질 뷰어를 결정합니다.|

## 자바 HS 파일 형식

Java HS 파일은 XML 파일 형식이며 W3C(World Wide Web Consortium) Extended Markiup Language 제안 권장 사항[PR-xml-971208](http://www.w3.org/TR/PR-xml- 971208). 이는 Java HS 파일이 모든 XML 판독기 응용 프로그램에서 열 수 있는 사람이 읽을 수 있는 XML 파일 형식임을 의미합니다.

### 자바 HS 파일 형식 예

다음은 [Oracle Helpset 문서](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)에 있는 helpset 파일의 예입니다.

```html
<?xml version='1.0' encoding='ISO-8859-1' ?>
<!DOCTYPE helpset
  PUBLIC "-//Sun Microsystems Inc.//DTD JavaHelp HelpSet Version 2.0//EN"
         "http://java.sun.com/products/javahelp/helpset_2_0.dtd">
<helpset version="2.0">
   <!-- title -->
   <title>Java Development Environment - Help</title>

   <!-- maps -->
   <maps>
     <homeID>top </homeID>
     <mapref location="Map.jhm" />
   </maps>

   <!-- views -->
   <view xml:lang="en" mergetype="javax.help.UniteAppendMerge">
      <name>TOC</name>
      <label>Table Of Contents</label>
      <type>javax.help.TOCView</type>
      <data>IdeHelpTOC.xml</data>
   </view>

   <view xml:lang="en" mergetype="javax.help.SortMerge">
      <name>Index</name>
      <label>Index</label>
      <type>javax.help.IndexView</type>
      <data>IdeHelpIndex.xml</data>
   </view>

   <view xml:lang="en">
      <name>Search</name>
      <label>Search</label>
      <type>javax.help.SearchView</type>
         <data engine="com.sun.java.help.search.DefaultSearchEngine">
         JavaHelpSearch
         </data>
   </view>

   <!-- A glossary navigator -->
   <view  mergetype="javax.help.SortMerge">
      <name>glossary</name>
      <label>Glossary</label>
      <type>javax.help.GlossaryView</type>
      <data>glossary.xml</data>
   </view>

   <!-- A favorites navigator -->
   <view>
      <name>favorites</name>
      <label>Favorites</label>
      <type>javax.help.FavoritesView</type>
   </view>

   <!-- presentation windows -->

   <!-- This window is the default one for the helpset.
     *  Its title bar says "Project X Help". It
     *  is a tri-paned window because displayviews, not
     *  defined, defaults to true and because a toolbar is defined.
     *  The toolbar has a back arrow, a forward arrow, and
     *  a home button that has a user-defined image.
   -->
   <presentation default=true>
       <name>main window</name>
       <size width="400" height="400" />
       <location x="200" y="200" />
       <title>Project X Help</title>
       <toolbar>
           <helpaction>javax.help.BackAction</helpaction>
           <helpaction>javax.help.ForwardAction</helpaction>
           <helpaction image="homeicon">javax.help.HomeAction</helpaction>
       </toolbar>
   </presentation>

   <!-- This window is simpler than the main window.
     *  It's intended to be used a secondary window.
     *  It has no navigation pane or toolbar.
   -->
   <presentation displayviews=false>
       <name>secondary window</name>
       <size width="200" height="200" />
       <location x="200" y="200" />
   </presentation>

   <!-- subhelpsets -->
   <subhelpset location="file:/c:/Foobar/HelpSet2.hs" />

   <!-- implementation section -->
   <impl>
      <helpsetregistry helpbrokerclass="javax.help.DefaultHelpBroker" />
      <viewerregistry viewertype="text/html"
         viewerclass="com.sun.java.help.impl.CustomKit />
      <viewerregistry viewertype="text/xml"
         viewerclass="com.sun.java.help.impl.CustomXMLKit />
   </impl>
</helpset>
```

## 참고문헌
* [오라클 자바 도움말 파일](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - Haskell 스크립트 파일 형식

## .HS 파일이란?

확장자가 .hs인 파일은 순수 기능의 고급 오픈 소스 프로그래밍 언어인 [Haskell](https://wiki.haskell.org/Haskell)로 작성된 Haskell Script 파일입니다. HS 파일로 작성된 코드는 [C](/ko/programming/c/), [C++](/ko/programming/cpp/) 등과 달리 강력하고 간결한 소프트웨어의 신속한 개발 원칙을 따르는 순전히 기능 기반입니다. Haskell은 유연한 고품질 애플리케이션을 생성하기 위해 풍부한 API, 프로파일러 및 디버거와 함께 내장된 동시성 및 병렬 처리를 제공합니다.

## HS 파일 형식

모든 프로그래밍 언어와 마찬가지로 HS 파일은 사람이 읽을 수 있는 일반 텍스트 형식으로 작성됩니다. 사용 가능한 텍스트 도구를 사용하여 생성, 편집 및 볼 수 있습니다. .hs 소스 코드 파일은 Haskell 컴파일러로 컴파일되어 실행 가능한 바이너리 파일을 생성합니다.

### HS 파일 형식 예

코드는 .hs 파일로 작성하고 [GHC](https://haskell.org/ghc)와 같은 Haskell 컴파일러를 사용하여 컴파일할 수 있습니다. 다음 코드 줄은 다음 샘플과 같이 `HelloWorld.hs`로 저장됩니다.

```
main = putStrLn "Hello, World!"
```

이것은 다음 명령을 사용하여 컴파일됩니다.

```
$ ghc -o hello hello.hs
```
결과 실행 파일은 다음과 같이 실행할 수 있습니다.

```
$ ./hello
```
"Hello, World!"가 인쇄됩니다. 출력에 대한 명령문.

## 참고문헌

* [하스켈](https://wiki.haskell.org/Haskell)
* [쉬운 5단계 하스켈](https://wiki.haskell.org/Haskell_in_5_steps)

