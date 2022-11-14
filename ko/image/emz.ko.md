{
  "date" : "2019-10-11",
  "keywords" :[ "emz 파일", "emz 파일 형식", "emz 파일이란", "파일", "emz 예제", "emz 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMZ 파일 형식 - Windows 압축 확장 메타 파일",
  "description":"EMZ 파일을 만들고 열 수 있는 EMZ 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "EMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## .EMZ 파일이란?

확장자가 .emz인 파일은 Enhanced Metafile([EMF](/ko/image/emf/) 파일)의 압축 컨테이너입니다. 이들은 UNIX 및 LINUX 운영 체제에서 일반적으로 사용되는 압축 방법인 [GZIP](/ko/compression/gz/) 압축 기술을 사용하여 압축됩니다. ZIP 링크 해제(/ko/compression/zip/), GZIP은 개별 파일을 압축하는 대신 전체 아카이브를 압축합니다. EMZ 파일은 EMF 파일에 비해 크기가 작으며 온라인 파일 공유 시 빠른 전송을 돕습니다. EMZ 파일을 열 수 있는 일부 응용 프로그램에는 Microsoft Visio 2019, Microsoft Office 2019, XnView MP 및 File Viewer Plus가 있습니다.

## EMZ 파일 형식

EMZ 파일은 [Gzip](/ko/compression/gz/) 압축되어 있으며 내부에 [EMF](/ko/image/emf/)가 들어 있습니다. Gzip은 아카이브 압축을 위해 DEFLATE 알고리즘을 사용하며 압축을 적용하는 것과 다릅니다. EMZ 파일은 GNU Zip과 같은 GZip 압축 유틸리티를 사용하여 압축을 풀 수 있습니다. 파일 형식은 다음으로 구성됩니다.

* 파일 헤더
* 선택적 헤더
* 압축 데이터
* 파일 바닥글

IETF(Internet Engineering Task Force)에서 발행한 GZIP 파일 형식[사양 버전 4.3](http://tools.ietf.org/html/rfc1952)에는 파일 형식에 대한 자세한 정보가 포함되어 있습니다.

## 참고문헌

* [RFC1952: GZIP 파일 형식 사양](http://tools.ietf.org/html/rfc1952), [IETF](https://www.ietf.org/) 작성
* [윈도우 메타파일 - 위키피디아](https://en.wikipedia.org/wiki/Windows_Metafile)

