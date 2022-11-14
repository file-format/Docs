---
date: 2022-03-20
keywords: mxl, Musepack 파일 형식, .mxl 확장자
작가:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "MXL 파일 형식과 MXL 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
title: MXL 파일 형식 - 압축 MusicXML 파일
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## .MXL 파일이란?

MXL 파일은 디지털 악보 교환을 위한 개방형 표준 형식인 MusicXML 파일 형식의 압축된 형식입니다. 일반 텍스트 MusicXML 파일은 크기가 크며 이러한 파일을 시트 배포 형식으로 사용하면 파일 크기가 큰 영향을 받습니다. 이 문제는 [MusicXML](https://www.musicxml.com/) 2.0에서 원본 MIDI 파일과 유사한 파일 크기를 줄이기 위해 파일을 충분히 압축하는 MXL 파일 형식을 도입하여 처리되었습니다. MXL 파일에 권장되는 미디어 유형은 application/vnd.recordare.musicxml입니다.

## MXL 파일 형식

MXL 파일은 파일 확장자가 .mxl인 [ZIP](/ko/compression/zip/) 압축된 [XML](/ko/web/xml/) 파일로 저장됩니다. MXL 파일은 [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)에 지정된 대로 DEFLATE 알고리즘으로 압축됩니다.

### MXL 파일 구조

각 MXL 파일에는 파일의 MusicXML 버전의 시작점을 설명하는 META-INF/container.xml 파일이 있어야 하는 ZIP 기반 XML 형식이 있습니다. MXL 파일 형식에 대해 정의된 해당 .xsd 파일이 없습니다.

간단한 container.xml 파일의 내용은 다음과 같습니다. 이 예제는 MakeMusic 웹 사이트에서 사용할 수 있는 Dichterliebe01.mxl 파일에서 가져왔습니다.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
이 예에서<container> 요소는 문서 요소입니다. 그만큼<rootfiles> 요소는 하나 이상을 포함할 수 있습니다.<rootfile> 요소, 첫 번째<rootfile> MusicXML 루트를 설명하는 요소입니다. 로 사용되는 MusicXML 파일<rootfile> 할 수 있습니다<score-partwise> ,<score-timewise> , 또는<opus> 문서 요소로.

## 참고문헌

* [압축된 MXL 파일](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)
* [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)

