{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"파일 만들기 - Xcode Makefile 스크립트 파일",
  "description":"MakeFile 파일을 만들고 열 수 있는 XCode MakeFile 형식 및 API에 대해 알아보세요.",
  "linktitle" : "MAKE",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}


## .MAKE 파일이란?

MAKE 파일은 코드 컴파일을 구성하는 XCode 스크립트 파일입니다. 여러 소스 코드 파일에서 프로그램을 컴파일하고 링크하는 데 사용됩니다. 이 도움말은 응용 프로그램을 업데이트해야 할 때 다시 컴파일해야 하는 대규모 응용 프로그램의 부분을 결정합니다. Make 파일은 변경된 파일에 따라 일련의 지침을 사용하여 실행합니다.

## MAKE 파일 형식 예

다음 내용은 Make 유틸리티를 사용하여 실행되며 출력은 다음과 같습니다.

```
hello:
	echo "hello world"
```
**출력하기**

```
$ make
echo "hello world"
hello world
```

## 참고문헌
* [XCode 및 Make - Apple 포럼](https://developer.apple.com/forums/thread/657458)
* [Object-C 가이드](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

