{
  "date" : "2021-03-10",
  "keywords" :[ "ACSM", "Adobe Content Server Message", "extension", "format", "eBook", "file", "Adobe Digital Editions" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Adobe의 ACSM 파일 형식과 ACSM 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"ACSM - Adobe Content Server 메시지 파일 형식",
  "linktitle" : "ACSM",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-05-28"
}

## .ACSM 파일이란?

확장자가 .acsm인 파일을 Adobe Content Server 메시지 파일이라고 합니다. 이러한 파일은 **Adobe Digital Editions**에서 Adobe DRM 보호 콘텐츠를 활성화하고 다운로드하는 데 사용됩니다. 실제로 ACSM 파일은 eBook 파일이 아닙니다. 다른 eBook(예: PDF)처럼 열고 읽을 수 없습니다. eBook을 활성화하고 다운로드하기 위한 데이터만 포함되어 있습니다. 즉, ACSM 파일은 Adobe 서버와 통신하는 정보로만 구성됩니다. Digital Editions 사용자는 eBook을 다운로드할 경우 ACSM 파일을 볼 수 있지만 어떤 이유로든 다운로드가 중지되었을 것입니다. 사용자는 .acsm 파일을 두 번 클릭하여 다운로드를 재개할 수 있습니다.

## ACSM 파일은 어떻게 작동합니까?

Adobe Content Server는 eBook 및 기타 디지털 자료를 보호할 책임이 있기 때문입니다. 구매 후 콘텐츠는 구매자의 Adobe ID에 자동으로 연결됩니다. 아이디는 비공개이며 타인에게 양도할 수 없습니다. 사용자는 Adobe 복사 방지 기능이 있는 문서를 구입하기 전에 설정해야 합니다. 고객은 Adobe ID를 백그라운드에서 실행되는 Adobe 서버 응용 프로그램에 전달하지 않고는 복사 방지된 문서에 액세스할 수 없습니다.

고객이 구매할 때 ACSM은 처음에 다운로드할 수 있는 유일한 파일입니다. ACSM 파일을 열려면 고객이 시스템에 Adobe Digital Editions 소프트웨어를 설치하고 Adobe ID에 연결해야 합니다. Adobe Digital Editions는 ACSM 파일을 변환하기 위한 권한 부여의 ID를 확인합니다. 인증되면 사용자는 [EPUB](/ko/ebook/epub/) 또는 [PDF](/ko/pdf/) 형식의 eBook을 다운로드할 수 있습니다. Adobe Digital Editions는 또한 ACSM 파일을 사용하여 다운로드 디렉토리를 인식합니다.

## 참고문헌

* [Adobe Content Server - Wikipedia 제공](https://en.wikipedia.org/wiki/Adobe_Content_Server)


