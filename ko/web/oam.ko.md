{
  "date" : "2023-01-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAM 파일 - Adobe Edge Animate 위젯 파일 형식",
  "description" :"OAM 파일이 무엇인지, 그리고 OAM 파일을 생성하고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "OAM",
  "menu" : {
    "docs" : {
      "identifier":"web-oam",
      "parent" : "web"
}
},
  "lastmod" : "2023-01-30"
}

## .OAM 파일이란?

.oam 파일은 Adobe Edge Animate Widget에서 내보낸 애니메이션 위젯 파일입니다. OAM 위젯 파일 형식으로 내보낸 애니메이션은 InDesign 문서([INDD 파일](/ko/page-description-language/indd/), Dreamweaver 및 Muse와 같은 다른 Adobe 응용 프로그램에 삽입할 수 있습니다. OAM 파일은 쉽게 사용할 수 있는 배포 패키지와 같습니다. 이를 활용하기 위해 다른 Adobe 프로젝트에 삽입합니다. OAM 파일에는 애니메이션의 자산, 동작 및 액션스크립트 코드에 대한 정보가 포함되어 있습니다. Adobe Animate 프로젝트[.AN 파일](/ko/web/an/)을 게시하여 OAM 파일을 만들 수 있습니다. .
사용자는 Edge Animate 프로젝트(.AN 파일)에서 게시하여 OAM 파일을 만들 수 있습니다.

## OAM 파일 형식

OAM 파일은 압축된 [ZIP](/ko/compression/zip/) 아카이브로 디스크에 저장됩니다. 이는 파일 확장자의 이름을 .zip으로 바꾸고 WinZIP 또는 WinRAR과 같은 압축 유틸리티를 사용하여 추출할 수 있음을 의미합니다. 파일 크기가 줄어들면 인터넷을 통해 다른 사용자와 애니메이션을 더 쉽게 전송하고 공유할 수 있습니다.

### OAM 파일 구조

.oam 파일의 내부 파일 구조는 독점적이며 Adobe에서 공개적으로 문서화하지 않습니다. 그러나 .oam 파일에는 단일 파일로 패키지된 파일 및 리소스(예: 그래픽, 오디오 및 ActionScript 코드) 모음이 포함되어 있는 것으로 알려져 있습니다. .oam 파일의 내용에는 [XML](/ko/web/xml/) 파일, SWF 파일 및 기타 리소스 파일이 포함될 수 있습니다. .oam 파일의 정확한 구조는 파일을 만드는 데 사용된 Adobe Animate의 특정 버전과 파일에 포함된 애니메이션 및 에셋의 유형에 따라 달라집니다.

OAM 파일에는 다음 정보가 포함되어 있습니다.

`자산:` 애니메이션에 사용된 그래픽, 오디오, 비디오 자산에 대한 정보입니다.

`행동:` 애니메이션에서 발생하는 동작과 상호 작용에 대한 설명입니다.

`ActionScript 코드:` 애니메이션의 동작과 상호 작용을 제어하는 데 사용되는 코드입니다.

`게시 설정:` HTML5 또는 AIR와 같이 애니메이션이 게시될 플랫폼 및 형식에 대한 정보입니다.

`메타데이터:` 애니메이션 작성자, 제작 날짜, 버전 번호 등의 추가 정보입니다.

## OAM 파일을 여는 방법?

다음 응용 프로그램을 사용하여 OAM 파일을 열 수 있습니다.

* Adobe Edge Animate CC(단종)
* 어도비 애니메이트 2023
* 어도비 인디자인 2023
* 어도비 드림위버 2021

## 참고자료

* [OAM 게시](https://helpx.adobe.com/animate/using/OAM-publishing.html)

