{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AWK 파일 형식 - AWK 스크립트 파일",
  "description":"AWK 파일 형식과 AWK 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
      "identifier" : "programming-awk",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## .AWK 파일이란?

AWK 파일은 Unix 및 Linux 운영 체제와 함께 번들로 제공되는 텍스트 처리 응용 프로그램 **AWK**용으로 생성된 스크립트 파일입니다. 여기에는 텍스트 일치, 바꾸기 및 인쇄와 같은 파일 내용이나 텍스트에 대한 작업을 수행하기 위한 논리적 지침이 포함되어 있습니다. 이렇게 하면 입력 파일에서 보고서와 서식 있는 텍스트를 생성하는 데 도움이 됩니다. awk 유틸리티는 일반적으로 대부분의 linux/unix 배포판에서 /usr/bin/awk에 있습니다.

## AWK 스크립트를 만드는 방법?

AWK 파일은 Linux/Unix OS의 모든 텍스트 편집기에서 만들거나 열 수 있습니다. 다음과 같이 새 AWK 스크립트 파일을 만들 수 있습니다.

```
$ vi script.awk
```

그러면 텍스트 편집기에서 AWK 파일이 열립니다. 다음과 같이 텍스트 편집기에 몇 가지 명령문을 입력합니다.

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
이 텍스트 내용의 첫 번째 줄은 다음과 같이 설명됩니다.

* \#! – 스크립트의 지침에 대한 인터프리터를 지정하는 'Shebang'이라고 함
* /usr/bin/awk – 인터프리터
* -f – 프로그램 파일을 읽는 데 사용되는 인터프리터 옵션

## AWK 스크립트를 실행하는 방법?

파일을 저장하고 아래 명령을 실행하여 스크립트를 실행 가능하게 만드십시오.
```
$ chmod +x script.awk
```

그런 다음 스크립트는 다음과 같이 실행할 수 있습니다.

```
$ ./script.awk
```

결과는 다음과 같습니다.

```
Writing my first Awk executable script!
```

## 참조 ##

* [Awk 프로그래밍 언어를 사용하여 스크립트 작성](https://www.tecmint.com/write-shell-scripts-in-awk-programming/)

