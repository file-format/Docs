{
  "date" : "2022-06-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TPSR 파일 형식 - TeamViewer 파일럿 세션 보고서 파일",
  "description":"TPSR 파일을 만들고 열 수 있는 TPSR 파일 형식 및 API에 대해 알아보세요.",
  "linktitle" : "TPSR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-06"
}

## .TPSR 파일이란?

TPSR은 TeamViewer Assist AR(이전의 TeamViewer Pilot)에서 사용하는 연결 프로토콜 파일입니다. TPSR 파일에 저장된 정보는 압축된 [ZIP](/ko/compression/zip/) 파일 형식으로 저장됩니다. TPSR에는 문제 해결 및 검토 목적을 위해 전문가와 기술자 간의 TeamViewer 연결에 대한 자세한 기록이 포함되어 있습니다. TPSR 파일에 포함된 정보에는 장치 유형, 이름, Assist AR ID, 전문가 ID, 날짜 및 시간, 연결 기간이 포함됩니다. 이 데이터는 압축된 TPSR 아카이브 내의 [JSON](/ko/web/json/) 파일에 저장됩니다.

## TPSR 파일 형식

TPSR 파일은 콘텐츠가 JSON 파일 내에 저장되는 ZIP 아카이브 파일 형식으로 디스크에 저장됩니다. TeamViewer에서 연결 보고 옵션이 활성화된 경우 Assist AR 연결이 완료된 후 자동으로 생성됩니다.

TeamViewer Assist AR을 사용하면 전문가가 기술자와 연결하여 모바일 카메라를 통해 원격 엔드의 라이브 피드를 얻을 수 있습니다. 그들은 전화로 문제를 해결하기 위해 기술자를 도울 수 있습니다.

## TPSR 파일 열기

TeamViewer 소프트웨어의 데스크톱 버전을 사용하여 TPSR 파일을 열 수 있습니다. 컴퓨터에 설치된 경우 TPSR 파일을 두 번 클릭하면 TeamViewer 소프트웨어에서 열립니다. TPSR 파일은 [PDF](/ko/pdf/) 파일로도 내보낼 수 있으며 프로토콜 파일의 인쇄 사본을 갖도록 인쇄할 수도 있습니다.

## 참조 ##

* [TPSR](https://community.teamviewer.com/English/kb/articles/46456-using-teamviewer-assist-ar)

