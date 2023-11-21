
{
  "date" : "2023-02-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"네 번째 파일 - 네 번째 언어 파일 형식",
  "description":"4번째 파일을 생성하고 열 수 있는 예제와 API를 통해 .4번째 파일 형식이 무엇인지 알아보세요.",
  "linktitle" : "4th",
  "menu" : {
    "docs" : {
      "identifier":"programming-4th",
      "parent" : "programming"
}
},
  "lastmod" : "2023-02-09"
}

## 4번째 파일이 뭔가요?

.4번째 파일 확장자를 가진 파일은 **제4 프로그래밍 언어**용으로 작성된 프로그래밍 파일입니다. 여기에는 Forth 프로그래밍 언어로 작성된 프로그램의 소스 코드가 포함되어 있으며 프로그램이 실행될 때 출력을 생성합니다. [C](/ko/programming/c/) 및 [C++](/ko/programming/cpp/) 소스 파일과 유사한 또 다른 프로그래밍 언어 파일입니다.

## 네 번째 파일 형식 - 추가 정보


### 4번째 프로그래밍 언어 코드 예

다음은 주어진 숫자의 계승을 계산하는 Forth로 작성된 간단한 프로그램의 예입니다.

```
: factorial ( n -- n! )
   dup 0=
   if
      drop 1
      exit
   then
   1
   swap
   begin
      dup 1-
      dup 0=
      if
         drop
         exit
      then
      swap
      *
   repeat
;

```

이 예에서 계승 단어는 단일 인수 n을 사용하고 해당 계승을 반환합니다. dup 단어는 스택 상단의 값을 복제하고, drop은 스택 상단의 값을 버리고, *는 스택 상단의 두 값을 곱합니다. if 및 start/until 구문은 프로그램의 흐름을 제어합니다.

이 프로그램을 사용하려면 Forth 해석기에 정의를 입력한 다음 계승을 찾으려는 숫자로 계승 단어를 호출합니다.

```
10 factorial .
```
결과적으로 10의 계승값인 3628800이 출력됩니다.

## 참고자료

* [제4 프로그래밍 언어](https://en.wikipedia.org/wiki/Forth_(programming_언어))

