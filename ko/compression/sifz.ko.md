{
  "date" : "2021-04-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SIFZ 파일 형식 - Synfig Studio 압축 프로젝트 파일",
  "description":"SIFZ 파일 형식 및 SIFZ 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "SIFZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-30"
}

## .SIFZ 파일이란?

SIFZ 파일은 오픈 소스 2D 애니메이션 제작 애플리케이션 **Synfig Studio**에서 만든 gzip 압축 SIF 파일입니다. 애니메이션을 구성하는 여러 그래픽 요소가 포함되어 있습니다. 전체 애니메이션 콘텐츠는 모양으로 채워진 캔버스, 브러시 또는 연필 스트로크 및 텍스트의 조합을 사용하여 구축됩니다. 이 모든 것은 고유한 위치, 반지름, 접선, 각도, 꼭짓점 및 너비 핸들에 정렬됩니다. SIFZ 파일은 [Synfig Studio](https://www.synfig.org/)에서 열 수 있습니다.

## SIFZ 파일 형식

SIFZ 파일은 gzip 압축 방법을 사용하여 패키지된 압축 [ZIP](/ko/compression/zip/) 파일입니다. Synfig는 벡터 및 비트맵 아트웍을 사용하여 영화 품질의 애니메이션을 만드는 데 사용됩니다. 기존의 프레임별 애니메이션 생성 방법과 달리 더 적은 리소스로 더 높은 품질의 2D 애니메이션을 생성할 수 있습니다.

압축되는 SIFZ 파일은 압축되지 않은 SIF 파일보다 작습니다. 또한 낮은 대역폭의 인터넷 연결을 통해 쉽게 전송할 수 있습니다.

## 참고문헌

* [Synfig 오픈 소스 - Github](https://github.com/synfig/synfig/)
* [Synfig 문서](https://synfig.readthedocs.io/en/latest/index.html)

