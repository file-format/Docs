{
  "date" : "2022-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M4S 파일 - M4S 파일이란 무엇입니까?",
  "description":"M4S 파일을 만들고 열 수 있는 M4S 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "M4S",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-18"
}

## .M4S 파일이란?

M4S 파일은 **MPEG-DASH** 스트리밍 기술을 사용하여 인터넷을 통해 스트리밍되는 동영상의 작은 부분입니다. 바이너리 데이터 형태의 비디오 세그먼트를 포함합니다. 수신 애플리케이션(일반적으로 웹 브라우저 또는 미디어 플레이어)은 수신된 순서대로 이러한 세그먼트를 재생합니다. 첫 번째 M4S 세그먼트는 포함된 초기화 데이터로 식별됩니다. **요약**에서 M4S 파일은 전체 파일의 작은 개별 미디어 세그먼트입니다.

## M4S 파일 형식

M4S 파일은 [ISO Base Media File(ISOBMFF) 형식](https://www.w3.org/TR/mse-byte-stream-format-isobmff/)을 기반으로 합니다. 큰 파일의 이러한 작은 세그먼트는 HTTP를 통해 독립적으로 다운로드할 수 있습니다. 따라서 대용량 [MP4](/ko/video/mp4/) 동영상 파일이 있는 경우 M4S 세그먼트 파일로 분할하여 MPEG-DASH(Dynamic Adaptive Streaming over HTTP) 기술을 사용하여 스트리밍할 수 있습니다. 이 대용량 동영상 파일을 M4S로 디스크에 다운로드하면 여러 M4S 파일이 다운로드됩니다. 이러한 모든 .m4s 세그먼트가 연결되면 완전한 재생 가능한 파일이 생성됩니다. 미디어 플레이어는 파일과 함께 첫 번째 초기화 세그먼트도 사용할 수 없는 경우 파일을 재생할 수 없습니다.

## MPEG-DASH 스트리밍 정보

MPEG-DASH는 인터넷을 통해 고품질 미디어 콘텐츠를 스트리밍할 수 있는 적응형 비트 전송률 스트리밍 기술을 사용합니다. 이는 콘텐츠를 HTTP를 통해 스트리밍되는 일련의 작은 세그먼트로 분할하여 수행됩니다. 영화, 팟캐스트 또는 스포츠 경기 생중계와 같은 대용량 미디어 파일을 이러한 방식으로 스트리밍할 수 있습니다. 이러한 세그먼트는 다른 비트 전송률로 인코딩됩니다. MPEG-DASH 지원 미디어 플레이어는 비트 전송률 적응 알고리즘을 사용하여 비트 전송률이 가장 높은 세그먼트를 자동으로 선택합니다. 이렇게 하면 재생에서 이벤트가 지연되거나 다시 버퍼링되는 것을 방지할 수 있습니다.

### M4S 파일용 오픈 소스 API

M4S 파일을 읽고 변환하는 데 사용할 수 있는 오픈 소스 API가 있습니다.

* [libdash](https://github.com/bitmovin/libdash) - M4S 파일용 .NET API
* [dash.js](https://github.com/Dash-Industry-Forum/dash.js) - M4S 파일용 자바스크립트 클라이언트
* [대시 파일 생성을 위한 Go 라이브러리](https://github.com/zencoder/go-dash)

### M4S를 MP4로 변환하는 오픈 소스 API

* [MFourStoMp4](https://github.com/muri11o/mfourstomp4)

## 참조 ###

* [ISO 기본 미디어 파일(ISOBMFF) 형식](https://www.w3.org/TR/mse-byte-stream-format-isobmff/)
* [HTTP를 통한 동적 적응 스트리밍 - MPEG-DASH](https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP)

