{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"KIT 파일을 만들고 열 수 있는 KIT 파일 형식과 API에 대해 알아보세요.",
  "title" :"KIT 파일 형식 - CodeKit 파일",
  "linktitle" : "KIT",
  "menu" : {
    "docs" : {
      "identifier":"web-kit",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## .KIT 파일이란?

.kit 확장자를 가진 파일은 [CodeKit](https://codekitapp.com/) 프로그래밍 언어 응용 프로그램으로 생성된 HTML 파일입니다. 기존의 [HTML](/ko/web/html/) 파일 외에 '가져오기'와 '변수'가 포함되어 있어 정적인 사이트에 적합합니다. CodeKit은 KIT 파일을 정적 웹사이트 파일로 쉽게 사용할 수 있는 HTML로 컴파일합니다.

## 키트 파일 형식

KIT 파일은 가져오기 및 변수를 추가로 포함하는 HTML 파일입니다. 이들은 일반 텍스트 파일로 저장되며 모든 텍스트 편집기 또는 웹 파일 편집기로 열 수 있습니다.

### 키트 파일 가져오기

거의 모든 유형의 파일을 Kit 파일로 가져올 수 있습니다. 다음은 파일을 .kit 파일로 가져오는 데 사용되는 가져오기 구문입니다.

```
<!-- @import "someFile.kit" -->
<!-- @import "file.html" -->
```

가져오기를 KIT 파일에 추가하여 저장하면 가져오는 파일의 텍스트로 대체됩니다. @import 대신 @include를 사용할 수도 있습니다.

### KIT 파일의 다중 가져오기

쉼표로 구분된 목록을 사용하여 한 번에 둘 이상의 파일을 가져올 수도 있습니다.

```
<!-- @import someFile, otherFile.html, ../thirdFile.kit -->
```

## 참고문헌

* [키트란?](https://codekitapp.com/help/kit/)

