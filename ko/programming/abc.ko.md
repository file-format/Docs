
{
  "date" : "2021-12-14",
  "keywords": [ ".abc file", "extension", "format","ActionScript Byte Code File", "how to open .abc file","abc file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABC - ActionScript 바이트 코드 파일",
  "description":"ABC 파일을 만들고 열 수 있는 예제와 API를 통해 ABC 파일 형식이 무엇인지 알아보세요.",
  "linktitle" : "ABC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-14"
}

## .ABC 파일이란?

확장자가 .abc인 파일은 Flash 컴파일러에서 ActionScript 스크립트 파일을 컴파일한 결과 생성된 ActionScript 바이트 코드 파일입니다. ABC 파일에 포함된 바이트 코드는 ActionScript 가상 머신(AVM 및 AVM2)에 의해 실행됩니다. 바이트 코드는 상수 데이터, AVM2 명령어 세트의 명령어 및 다양한 종류의 메타데이터로 구성됩니다. ABC 파일이 AVM 또는 AVM2에 로드되면 검증을 거칩니다. AVM2 개요를 준수하지 않으면 거부됩니다. ABC 파일은 오래 전에 중단된 Adobe Flash Player에서 열 수 있습니다.

## ABC 파일 형식 - 추가 정보

ABC 파일은 AVM 또는 AVM2 가상 머신에서 읽을 수 있는 바이너리 파일 형식으로 디스크에 저장됩니다. 내부 파일 구조는 모든 상수 데이터, 유형 설명자, 코드 및 메타데이터가 포함된 실행 코드 블록을 나타냅니다.

## ABC 파일 구조

ABC 파일 구조는 아래와 같습니다.

```
abcFile  
{
           u16        minor_version                
           u16        major_version                
           cpool_info        constant_pool                
           u30        method_count                
           method_info        method[method_count]                
           u30        metadata_count                
           metadata_info        metadata[metadata_count]                
           u30        class_count                
           instance_info        instance[class_count]                
           class_info        class[class_count]                
           u30        script_count                
           script_info        script[script_count]               
           u30        method_body_count                
           method_body_info        method_body[method_body_count]        
}
```

### ABC 파일 필드

|필드 이름|설명|
---|---|
|minor_version, major_version|major_version 및 minor_version의 값은 abcFile 형식의 주 및 부 버전 번호입니다.|
|constant_pool|constant_pool은 정수, double, 문자열, 네임스페이스, 네임스페이스 세트 및 다중 이름으로 구성된 가변 길이 구조입니다.|
|method_count, method|method_count의 값은 메소드 배열의 항목 수입니다. 메소드 배열의 각 항목은 가변 길이 method_info 구조입니다.|
|metadata_count, metadata|metadata_count의 값은 메타데이터 배열의 항목 수입니다. 각 메타데이터 항목은 이름을 문자열 값 집합에 매핑하는 metadata_infostructure입니다. |
|class_count, instance, class|class_count의 값은 인스턴스 및 클래스 배열의 항목 수입니다. |
|script_count, script|script_count의 값은 스크립트 배열의 항목 수입니다. 각 스크립트 항목은 이 파일에 있는 단일 스크립트의 특성을 정의하는 script_info 구조입니다. |
|method_body_count, method_body|method_body_count의 값은 method_body 배열의 항목 수입니다. 각 method_bodyentry는 개별 메소드 또는 함수에 대한 지침을 포함하는 가변 길이 method_body_info 구조로 구성됩니다.|

## 참고문헌

* [강력한 ABC(ActionScript 바이트코드) [Dis-]어셈블러 - Github](https://github.com/CyberShadow/RABCDAsm)

