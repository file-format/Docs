{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CDF - 채널 정의 형식",
  "description" :"CDF 파일이 무엇이며 CDF 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "CDF",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-18"
}

## .CDF 파일이란?

확장자가 .cdf인 파일은 자주 업데이트되는 "채널"을 게시하는 데 사용되는 XLM 기반 정보 배포 파일 형식입니다. 정보는 모든 웹 서버에서 게시되며 웹 브라우저와 같은 호환되는 수신 프로그램이 있는 컴퓨터에 자동으로 전달됩니다. 사용자는 활성 채널을 구독하고 데스크톱으로 업데이트를 예약합니다.
CDF 파일은 이전에 Microsoft의 Active Channel, Active Desktop 및 Smart Offline Favorites 기술과 함께 사용되었습니다.

## CDF 파일 형식

CDF 파일은 정보 교환을 위한 일반 웹 파일 형식인 XML 파일로 저장됩니다. CDF 파일 형식은 현재 오래된 형식이며 널리 채택되지 않았습니다. 이에 비하면 넷스케이프의 RSS가 더 유명하고 널리 쓰였다.

### CDF 파일 형식 예

다음은 CDF 파일 형식의 일반적인 예입니다.

```
<?xml version="1.0" encoding="UTF-8"?>
<CHANNEL HREF="http://domain/folder/pageOne.extension"
BASE="http://도메인/폴더/"
LASTMOD="1998-11-05T22:12"
PRECACHE="예"
레벨="0">
<TITLE>채널 제목</TITLE>
<ABSTRACT>채널 콘텐츠 개요.</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY="14"/>
</SCHEDULE>
<LOGO HREF="wideChannelLogo.gif" STYLE="IMAGE-WIDE"/>
<LOGO HREF="imageChannelLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="iconChannelLogo.gif" STYLE="ICON"/>
<ITEM HREF="pageTwo.extension"
    LASTMOD="1998-11-05T22:12"
    PRECACHE="예"
레벨="1">
<TITLE>2페이지 제목</TITLE>
<ABSTRACT>2페이지 내용 개요.</ABSTRACT>
<LOGO HREF="pageTwoLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="pageTwoLogo.gif" STYLE="ICON"/>
</ITEM>
</CHANNEL>
```

## 참고문헌

* [채널 정의 형식 - Wikipedia 기준](https://en.wikipedia.org/wiki/Channel_Definition_Format)

