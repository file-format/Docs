{
"날짜":"2023-07-20",
   "keywords":[
"큰 상자",
"BIN 파일",
"파일",
"BIN 파일 확장자",
"확대",
"파일"
],
   "author":{
"display_name":"샤킬 파이즈"
},
"draft":"false",
"toc":true,
"title":"BIN 파일 형식 - Unix 실행 파일",
   "description":"BIN 파일을 생성하고 열 수 있는 BIN 형식과 API에 대해 알아보세요.",
"linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"executable-bin",
"parent":"실행 가능"
}
},
"lastmod":"2023-07-20"
}

## .BIN 파일이란?

BIN 파일은 Linux 또는 FreeBSD와 같은 Unix 기반 운영 체제에서 실행 가능한 파일입니다. 소스 코드에서 파생된 바이너리 코드로 구성된 컴파일된 프로그램을 보유하므로 기본 시스템 아키텍처와 호환됩니다. Unix Executable BIN 파일은 실행 파일 형식으로서의 역할 측면에서 Windows .EXE 파일 및 macOS .APP 파일과 비교할 수 있습니다.

Unix 시스템용 소프트웨어 개발 영역에서 BIN 파일은 개발자가 프로그램을 패키지하고 배포하기 위해 일반적으로 사용됩니다. 이는 사용자에게 소프트웨어를 제공하는 편리한 수단을 제공하므로 쉽게 설치하고 실행할 수 있습니다. BIN 파일 외에도 [.ELF](/ko/executable/elf/), .X86, [.RUN](/ko/executable/run/) 및 .X86_64를 포함하여 각각 특정 하드웨어 또는 시스템 요구 사항.

BIN 파일의 내부 구조는 Unix 운영 체제가 포함된 프로그램을 식별하고 읽고 실행하는 데 사용하는 인코딩된 데이터로 구성됩니다. 시스템은 특정 파일 서명이나 헤더를 사용하여 BIN 파일을 실행 파일로 인식한 후 그 안에 포함된 바이너리 명령을 해석하고 실행합니다.

BIN 파일은 종종 프로그램을 올바르게 설치하고 설정하는 방법에 대한 자세한 지침을 제공하는 **INSTALL.TXT** 파일과 함께 번들로 제공됩니다. 이 문서를 통해 사용자는 설치 과정을 성공적으로 탐색하고 문제 없이 소프트웨어를 사용할 수 있습니다.

## BIN 파일 여는 방법?

BIN 파일은 직접 열고 볼 수 있도록 설계되지 않았습니다. 그러나 프로그램을 실행하거나 프로그램에 포함된 데이터를 추출할 수 있습니다. BIN 파일의 내용에 액세스하려면 BIN 파일 이름이 "sample.bin"이라고 가정하고 명령줄에서 다음 단계를 수행하십시오.

1. **실행 권한 확인:**

BIN 파일을 실행하기 전에 실행 파일로 실행하는 데 필요한 권한이 있는지 확인하세요. 다음 명령을 사용하십시오.

```
$ chmod +x sample.bin
```

이 명령은 파일 실행 권한을 부여합니다.

2. **BIN 파일을 실행합니다:**

실행 권한을 설정한 후 다음 명령을 입력하여 BIN 파일을 실행할 수 있습니다.

```
$ ./sample.bin
```

**경고**

_다운로드하거나 이메일로 보낸 BIN 파일을 처리할 때는 사이버 범죄자가 악성 코드를 배포하는 데 사용할 수 있으므로 주의하십시오. 악의적인 실행 가능 공격의 위험을 완화하려면 신뢰할 수 있는 소스의 BIN 파일만 실행하세요._

## 기타 BIN 파일

**.bin** 파일 확장자를 사용하는 다른 파일 형식은 다음과 같습니다.

- [BIN - MacBinary 인코딩 파일](/ko/compression/bin/)
- [BIN - 바이너리 디스크 이미지 파일](/ko/disc-and-media/bin/)
- [BIN - BlackBerry IT 정책 파일](/ko/settings/bin/)
- [BIN - Sega Genesis 게임 ROM](/ko/game/bin/)
- [BIN - PSX PlayStation BIOS 이미지](/ko/game/bin-pcsx/)

## 참고자료

* [리눅스에서 바이너리 파일을 실행하는 방법](https://linuxhint.com/execute-binary-files-in-linux/)


