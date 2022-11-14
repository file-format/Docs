{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AGI 파일 - 별표 게이트웨이 인터페이스 파일 형식",
  "description":"AGI 파일을 만들고 열 수 있는 예제와 API를 통해 AGI 파일 형식이 무엇인지 알아보세요.",
  "linktitle" : "AGI",
  "menu" : {
    "docs" : {
      "identifier": "programming-agi",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## .AGI 파일이란?

AGI 파일은 오픈 소스 전화 통신 시스템인 Asterisk에서 사용하는 스크립트 파일입니다. 여기에는 프로세스 및 별표 다이얼 플랜을 자동화하는 데 사용할 수 있는 정보가 포함되어 있습니다. AGI 스크립트 파일을 사용하여 PostgreSQL 또는 MySQL과 같은 관계형 데이터베이스와 연결할 수 있습니다. 또한 AGI 스크립트를 사용하여 다른 외부 리소스에도 액세스할 수 있습니다. AGI 스크립트는 다이얼 플랜의 제어를 외부 AGI 스크립트로 넘겨서 Asterisk가 복잡한 작업을 수행할 수 있도록 합니다.

## AGI 파일 형식 - 추가 정보

AGI 스크립트 파일은 텍스트 파일로 저장되며 변경을 위해 모든 텍스트 편집기에서 열 수 있습니다.

### AGI 통신의 표준 패턴

AGI 스크립트는 Asterisk에서 보낸 변수와 해당 값을 로드합니다. 이러한 변수의 일반적인 모습은 다음과 같습니다.

```
agi_request: test.py
agi_channel: Zap/1-1
agi_language: en
agi_callerid:
agi_context: default
agi_extension: 123
agi_priority: 2
```

이 변수 뒤에는 AGI 스크립트가 이제 다이얼 플랜을 제어할 수 있음을 나타내는 Asterisk에서 보낸 빈 줄이 있습니다.

### AGI 스크립트 파일용 프로그래밍 언어

AGI 스크립트는 일반적으로 Perl, [PHP](/ko/programming/php/), [C](/ko/programming/c/), Pascal 또는 Bourne Shell로 작성할 수 있습니다.

## 참고문헌

* [별표 AGI 스크립트](https://www.oreilly.com/library/view/asterisk-the-future/9780596510480/ch09.html)

