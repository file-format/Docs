{
  "date" : "2021-08-10",
  "keywords" :[ ".ovf 파일", "파일 형식", ".ovf 파일이란", "파일", "파일 확장자"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :".ovf 파일 형식이 무엇이며 OVF 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"OVF 파일 형식 - 가상화 파일 열기",
  "linktitle" : "OVF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## .OVF 파일이란?

OVF 파일은 가상 머신에서 실행되는 소프트웨어의 패키징 및 배포에 대한 정보가 포함된 텍스트 파일입니다. 가상 머신에서 애플리케이션을 실행하기 위한 모든 요구 사항(예: 보안, 이식성, 효율성 및 확장성)을 설명하는 [Open Virtualization Standard Specifications](https://www.dmtf.org/standards/ovf)에 따라 형식이 지정됩니다. 국제 표준화 기구(ISO)는 OVF를 ISO 17203 표준으로 채택했습니다.

## OVF 파일 형식의 간략한 역사

OVF 파일 형식은 개방형 관리 용이성 표준을 만드는 DMTF(Distributed Management Task Force)에서 도입했습니다. 특정 하이퍼바이저 또는 명령어 세트 아키텍처와 무관합니다. OVF 패키지에는 각각 가상 머신에 배포할 수 있는 하나 이상의 가상 시스템이 포함되어 있습니다.

## OVF 파일 형식 - 추가 정보

OVF 패키지는 단일 디렉토리에 있는 여러 파일로 구성됩니다. 이 중 [XML](/ko/web/xml/) 파일 형식으로 저장된 정확히 하나의 OVF 설명자(확장자 .ovf) 파일을 포함합니다. 다음과 같은 OVF 패키지에 대한 패키지된 가상 머신 정보 및 메타데이터 정보를 설명합니다.

* 이름
* 하드웨어 요구 사항
* OVF 패키지의 다른 파일에 대한 참조 및
* 사람이 읽을 수 있는 설명

OVF 패키지에서 찾을 수 있는 다른 파일에는 하나 이상의 디스크 이미지와 선택적으로 인증서 파일 및 기타 보조 파일이 포함됩니다.

## 참고문헌

* [오픈 가상화 형식 - DMTF](https://www.dmtf.org/standards/ovf)
* [OVF 파일 형식 사양](https://www.dmtf.org/sites/default/files/standards/documents/DSP0243_1.1.0.pdf)

