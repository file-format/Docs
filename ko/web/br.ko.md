{
  "date" : "2022-08-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BR 파일 - Brotli 압축 파일 형식",
  "description":"BR 파일을 만들고 열 수 있는 BR 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "BR",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-20"
}

## .BR 파일이란?

BR 파일은 오픈 소스 데이터 압축 알고리즘 **Brotli**를 적용하여 생성된 압축 웹 파일입니다. 스타일시트([CSS](/ko/web/css/)), 이미지([SVG](/ko/image/svg/)), [XML](/ko/web/xml/) 및 스크립팅과 같은 웹페이지 자산을 저장하는 데 사용됩니다. 파일([JS](/ko/web/js/)). Chrome 및 Firefox와 같은 최신 웹 사이트는 BR 파일을 사용하여 페이지 로딩 시간을 줄여 사용자 경험을 개선합니다.

## BR 파일 형식

BR 파일은 Brotli 압축 알고리즘을 사용하여 생성된 압축 웹 파일입니다. Brotli 압축은 무손실 데이터 압축 알고리즘이며 Google에서 Zopfli 압축 알고리즘으로 개발했습니다. LZ77 무손실 압축 알고리즘과 허프만 코딩의 조합을 기반으로 합니다.

BR 파일은 크기가 작기 때문에 웹 서버 및 CDN(콘텐츠 전달 네트워크)에서 사용됩니다. 이러한 서버에 대한 요청으로 인해 HTTP 콘텐츠가 압축되어 웹 사이트가 더 빨리 로드됩니다. Brotli는 더 대중화되었으며 gzip보다 더 나은 압축을 제공합니다.

## 참고문헌

* [브로틀리 - 위키피디아](https://en.wikipedia.org/wiki/Brotli)

