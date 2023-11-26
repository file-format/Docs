{
  "date" : "2023-05-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"NMONEY 파일 형식과 NMONEY 파일을 생성하고 열 수 있는 API에 대해 알아보세요.",
  "title" :"NMONEY 파일 - 데나로 계정 파일 형식",
  "linktitle" : "NMONEY",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-17"
}

## .NMONEY 파일이란?

NMONEY 파일은 금융 거래 내역이 포함된 금융 데이터 저장 데이터베이스 파일입니다. Nickvision이 개발했으며 개인 금융 소프트웨어 애플리케이션인 Nickvision Denaro 소프트웨어에 사용되었습니다. NOMONEY 파일에 저장된 데이터에는 계정에 대한 신용 및 차변 거래 정보가 포함됩니다.

NOMONEY 파일은 [Github](https://github.com/NickvisionApps/Denaro) 애플리케이션으로 열 수 있습니다.

## 데나로 소프트웨어 소개

Denaro는 처음에 [Nickvision](https://nickvision.org/)에서 제품으로 개발되었으며 나중에 [Github](https://github.com/NickvisionApps/Denaro)에서 호스팅되는 오픈 소스 소프트웨어 앱으로 변환되었습니다. . 그 이후로 앱은 Github에서만 수정 및 업데이트되었습니다. 앱은 Windows App SDK(현재 WinUI 3)를 사용하여 Windows UI에서 C#으로 개발됩니다.

### Denaro가 제공하는 기능

* 가장 인기 있고 친숙한 탭 인터페이스로 여러 계정을 동시에 관리
* 유형, 그룹 또는 날짜별로 거래 필터링
* 매월 발생하는 청구서 등 반복거래
* 한 계좌에서 다른 계좌로 돈을 이체하세요
* 계정의 데이터를 CSV 파일로 내보내고 CSV, OFX 또는 QIF 파일을 가져와 계정에 거래를 추가하세요.

## Denaro 파일 형식 - 추가 정보

Denaro 파일은 바이너리 파일 형식으로 디스크에 저장됩니다. 금융 데이터는 **.SQLITE3** 파일 형식의 데이터베이스 파일로 저장됩니다. SQLITE는 SQLite 소프트웨어로 생성된 경량 SQL 데이터베이스 파일입니다. 모든 기능을 갖추고 신뢰성이 높은 데이터베이스를 제공할 수 있는 독립형 데이터베이스 엔진을 제공합니다. SQLite 데이터베이스 파일을 사용하면 네트워크를 통해 이러한 파일을 간단히 교환함으로써 시스템 간에 풍부한 콘텐츠를 공유할 수 있습니다. C, [C#](/ko/programming/cs/), [C++](/ko/programming/cpp/), [Java](/ko/programming/java/), [PHP](/ko/programming/ 등의 프로그래밍 언어에 대한 SQLite 바인딩이 존재합니다. php/) 등이 있습니다.

## 참고자료

* [닉비전](https://nickvision.org/)
* [NIckVision - Github](https://github.com/NickvisionApps/Denaro)

