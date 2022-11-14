{
  "date" : "2021-07-23",
  "keywords" :[ "PL", "파일", "확장자", "형식", "펄", "펄 언어", "PL 파일", "프로그래밍"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description":"PL 파일을 만들고 열 수 있는 PL 파일 형식과 API에 대해 알아보세요.",
  "title" :"PL 파일 - Perl 스크립트 파일 형식",
  "linktitle" : "PL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-07-23"
}

## .PL 파일이란?

확장자가 .pl인 파일은 스크립팅 언어인 Perl 스크립트 파일입니다. 이들은 Perl Interpreter 소프트웨어를 사용하여 컴파일되고 실행됩니다. PL 스크립트 파일에는 코드 줄, 변수 및 주석이 포함됩니다. 스크립팅 언어는 상대적으로 어렵습니다.
[PHP](/ko/programming/php/)와 같은 다른 프로그래밍 파일 형식을 이해합니다. PL 파일을 생성할 수 있으며 Windows, macOS 및 Linux와 호환됩니다.

## Perl 스크립팅 언어의 간략한 역사

이 언어는 1987년에 처음 사용되었으므로 이 파일은 그 해에 기원을 얻었습니다. 1989년에 Perl 2가 출시되었습니다. 이후 5.35 버전까지 업데이트 및 수정이 완료되었으며, 차기 버전은 내년 출시를 목표로 하고 있습니다.

모든 업데이트에는 기능, 성능, 언어 및 파일 모양에 대한 도구가 추가되었습니다. 이 년 동안 버전에 대한 많은 수정이 있었습니다. 원래 기본 스크립팅 언어였으나 지금은 다른 많은 모듈도 포함합니다. 원래는 매우 단순한 언어였으나 이 언어의 문자는 촘촘해서 이해하기가 상당히 어려웠습니다.

## Perl 파일 형식 확장자 사양

이러한 프로그래밍 파일에는 몇 가지 속성 또는 사양이 있으며 그 중 일부는 다음과 같습니다.

* 이 파일에 포함된 코드는 일반 텍스트 형식이며 스크립트 개발에 사용됩니다.
* 서버 스크립팅, 텍스트 구문 분석 및 서버 관리는 이 언어의 스크립트가 다루는 주요 측면입니다.
* 이 언어와 관련된 많은 인기 있는 프로그램은 활성 상태 Active Perl 및 Bare Bones BBEdit(Mac OS와 호환)입니다.
* 이 언어는 고급 언어로 간주됩니다.
* Win32의 경우 사용자는 언어의 기본 바이너리 배포판을 설치해야 할 수 있습니다.
* 다양한 Windows 리소스 키트에서 실행하려면 일부 스크립팅 도구가 필요합니다.
* Visual Studio .NET은 프로그래밍 언어 개발을 위한 유명한 프레임워크입니다. Visual Perl로 알려진 Active State 도구는 Perl을 Visual Studio에 추가하는 데 사용됩니다.
* 파일에서 소스 코드의 첫 번째 줄은 사용 중인 인터프리터의 정보를 설명합니다. PL 파일은 일반적으로 컴퓨터에 설치된 Perl 인터프리터를 사용하여 이 스크립트를 실행하도록 컴퓨터에 지시하는 **#!/usr/bin/perl** 행으로 시작합니다.


## PL 스크립트 예제

```
#!/usr/bin/perl
print "Hello, world\n";
```

인쇄됩니다

```
Hello, World
```

### 한 줄 주석 ###

```
#!/usr/bin/perl
# This is a single line comment
print "Hello Perl\n";
```

### 여러 줄 주석 ###

```
#!/usr/bin/perl
=begin comment
This is a multiline comment.
Line 1
Line 2
=cut
print "Hello Perl\n";
```

### 변수 할당 ###

```
#!/usr/bin/perl
$a = 10;
print "Variable a = $a\n";
```

### 스칼라 변수 할당 ###

```
#!/usr/bin/perl
$age = 35; # Assigning an integer
$name = "Tony Stark"; # Assigning a string
$pi = 3.14; # Assigning a floating point
```

### 단순 스칼라 연산 ###

```
#!/usr/bin/perl
$constr = "hi" . "perl";# Concatenates two or more strings.
$add = 40 + 10; # addition of two numbers.
$prod = 4 * 51;# multiplication of two numbers.
$connumstr = $constr . $add;# concatenation of string and number.
```

## 참조 ##

- [Python(프로그래밍 언어) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

