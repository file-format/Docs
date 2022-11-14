{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MXF - 재료 교환 형식",
  "keywords" :[ "MXF", "matroska 비디오", "mkv 형식", "MXF 파일 재생 방법", "SMPTE", "멀티미디어", "비디오" ],
  "description":"MXF 파일을 만들고 열 수 있는 MXF 파일 형식 및 API에 대해 알아보세요.",
  "linktitle" : "MXF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-01"
}

## MXF 파일이란?

확장자가 .mxf인 파일은 파일에 대한 메타데이터 정보와 함께 디지털 비디오 및 오디오 미디어를 포함하는 멀티미디어 컨테이너 형식입니다. 미디어 및 엔터테인먼트 산업에서 일하는 엔지니어링, 기술 및 경영진의 전문가들의 글로벌 협회인 SMPTE(영화 및 텔레비전 엔지니어 협회) 표준을 따릅니다. MXF 파일은 [AVI](/ko/video/avi/) 또는 [MOV](/ko/video/mov/)와 같은 다른 파일 형식으로 변환할 수 있습니다.

## MXF 파일 형식

MXF 파일은 사실 정해진 형식의 바이트 시퀀스로 구성된 이진 파일입니다. 디코딩 응용 프로그램은 이 형식을 이해하고 정보를 추출하기 위해 이 형식을 준수해야 합니다. 이 형식을 사용하면 아래에 설명된 KLV 코딩을 사용하여 이전 버전과의 호환성을 손상시키지 않고 새 항목을 추가할 수 있습니다.

* 키 – 요소의 식별자, SMPTE UL(Universal Label)
* Length – 이 항목에 필요한 공간을 줄이기 위해 사용되는 가변 길이 인코딩인 데이터의 길이
* 값 – 요소의 실제 값.

### SMPTE 형식 사양

MXF 파일 형식은 다음 SMPTE 사양에 의해 정의되었습니다.

* SMPTE ST 377-1:2011. 텔레비전 — MXF(Material Exchange Format) — 파일 형식 사양
* SMPTE ST 377-2(2012년 1월 현재 작업 진행 중). MXF용 KLV 인코딩 확장 구문.
* SMPTE ST 378:2004(2010년 보관). 텔레비전 — 재료 교환 형식(MXF) — 작동 패턴 1a(단일 품목, 단일 패키지)
* SMPTE ST 379-1:2009. MXF(Material Exchange Format) — MXF 일반 컨테이너
* SMPTE ST 379-2:2010. MXF(Material Exchange Format) -- MXF 제약이 있는 일반 컨테이너
* SMPTE ST 380:2004. 텔레비전 — 재료 교환 형식(MXF) — 서술적 메타데이터 체계-1(표준, 동적)
* SMPTE ST 381-1:2005. 텔레비전 — MXF(Material Exchange Format) — MPEG 스트림을 MXF 일반 컨테이너(동적)에 매핑
* SMPTE ST 381-2:2011. MXF(Material Exchange Format) — MPEG 스트림을 MXF 제약이 있는 일반 컨테이너에 매핑
* SMPTE ST 382:2007. MXF(Material Exchange Format) — AES3 스트림 및 브로드캐스트 웨이브 오디오를 MXF 일반 컨테이너에 매핑
* SMPTE ST 383:2008. 텔레비전 — MXF(Material Exchange Format) — DV-DIF 데이터를 MXF 일반 컨테이너에 매핑
* SMPTE ST 384:2005. 텔레비전 — MXF(Material Exchange Format) — MXF 일반 컨테이너에 압축되지 않은 그림 매핑
* SMPTE ST 385:2004. 텔레비전 — MXF(Material Exchange Format) — SDTI-CP 에센스 및 메타데이터를 MXF 일반 컨테이너에 매핑
* SMPTE ST 386:2004(2010년 보관). 텔레비전 — MXF(Material Exchange Format) — 유형 D-10 에센스 데이터를 MXF 일반 컨테이너에 매핑
* SMPTE ST 387:2004(2010년 보관). 텔레비전 — MXF(Material Exchange Format) — 유형 D-11 에센스 데이터를 MXF 일반 컨테이너에 매핑
* SMPTE ST 388:2004(2010년 보관). 텔레비전 — MXF(Material Exchange Format) — A-law 코딩 오디오를 MXF 일반 컨테이너에 매핑
* SMPTE ST 389:2005. 텔레비전 — MXF(Material Exchange Format) — MXF 일반 컨테이너 역재생 시스템 요소
* SMPTE ST 390:2011. 텔레비전 — 재료 교환 형식(MXF) — 특수 작동 패턴 "Atom"(단일 항목의 단순화된 표현)
* SMPTE ST 391:2004(2010년 보관). 텔레비전 — 재료 교환 형식(MXF) — 작동 패턴 1b(단일 품목, 묶음 패키지)
* SMPTE ST 392:2004. 텔레비전 — 재료 교환 형식(MXF) — 작동 패턴 2a(재생 목록 항목, 단일 패키지)
* SMPTE ST 393:2004. 텔레비전 — 재료 교환 형식(MXF) — 작동 패턴 2b(재생 목록 항목, 묶음 패키지)
* SMPTE ST 394:2006. 텔레비전 — MXF(Material Exchange Format) — MXF 일반 컨테이너에 대한 시스템 계획 1
* SMPTE ST 405:2006. 텔레비전 — MXF(Material Exchange Format) — MXF 일반 컨테이너 시스템 계획 1을 위한 요소 및 개별 데이터 항목
* SMPTE ST 407:2006. 텔레비전 — MXF — 작동 패턴 3a 및 3b
* SMPTE ST 408:2006. 텔레비전 — MXF — 작동 패턴 1c, 2c 및 3c
* SMPTE ST 410: 2008. 자료 교환 형식 - 일반 스트림 파티션.
* SMPTE ST 422:2006. 재료 교환 형식 — JPEG2000 코드스트림을 MXF 일반 컨테이너에 매핑
* SMPTE ST 429.4:2006. D-Cinema 패키징 — MXF JPEG 2000 애플리케이션
* SMPTE ST 429.5:2006. D-Cinema Packaging — Timed Text Track 파일
* SMPTE ST 429.6:2006. D-Cinema 패키징 — MXF 트랙 파일 에센스 암호화
* SMPTE ST 434:2006. 자료 교환 형식 — 메타데이터 및 파일 구조 정보를 위한 XML 인코딩
* SMPTE ST 436:2006. 텔레비전 — VBI 라인 및 보조 데이터 패킷을 위한 MXF 매핑
* SMPTE ST 2019-4:2009. MXF 일반 컨테이너에 VC-3 코딩 단위 매핑
* SMPTE ST 2037:2009. MXF 일반 컨테이너에 VC-1 매핑
* SMPTE RP 2008:2008. 재료 교환 형식 — AVC 스트림을 MXF 일반 컨테이너에 매핑
* SMPTE RP 2057:2011. MXF의 텍스트 기반 메타데이터 캐리지
* SMPTE EG 41:2004. MXF(Material Exchange Format) — 엔지니어링 지침. 참고: 이 문서는 2012년 1월에 참조했을 때 SMPTE 웹 사이트에 더 이상 나열되지 않았습니다.
* SMPTE EG 42:2004. MXF(Material Exchange Format) — MXF 설명 메타데이터
* SMPTE RDD 3:2008. e-VTR MXF 상호 운용성 사양
* SMPTE RDD 9-2009. Sony MPEG Long GOP 제품의 MXF 상호 운용성 사양
* SMPTE 메타데이터 레지스트리 스프레드시트 메뉴.

### MXF 구조적 메타데이터

구조적 메타데이터는 파일 내용에 대한 유용한 정보를 포함하므로 MXF 파일의 기본입니다. MXF 메타데이터에는 프레임 속도, 프레임 크기, 파일 생성 날짜 및 사용자 지정 수정 날짜와 같은 정보가 포함되어 있습니다. 구조적 메타데이터는 다양한 필수 구성요소를 기술적으로 설명하고 출력 타임라인이 구성되는 방식을 전달하는 것을 포함하는 MXF 파일의 구조와 기능을 설명합니다.

## 참고문헌

* [MXF - Wikipedia](https://en.wikipedia.org/wiki/Material_Exchange_Format)
* [MXF - 진행 보고서](http://tech.ebu.ch/docs/techreview/trev_2010-Q3_MXF-1.pdf)
* [MXF용 오픈소스 C++ 라이브러리](http://www.freemxf.org/)

