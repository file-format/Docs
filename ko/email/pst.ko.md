{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PST - Outlook 개인 정보 저장소 파일 형식",
  "description":"PST 파일 형식과 PST 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "PST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## .PST 파일이란?

확장자가 .pst인 파일은 다양한 사용자 정보를 저장하는 Outlook 개인 저장소 파일(개인 저장소 테이블이라고도 함)을 나타냅니다. 사용자 정보는 이메일, 일정 항목, 메모, 연락처 및 기타 여러 파일 형식을 포함하는 다양한 유형의 폴더에 저장됩니다. PST 파일은 나중에 다양한 응용 프로그램에서 로드하고 볼 수 있는 이메일 데이터를 오프라인으로 보관하는 데 사용됩니다.

## PST 파일 형식 사양

PST 파일 형식[사양](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)은 Open Specification Promise를 통해 취소 불가능한 무료 특허 라이선스로 Microsoft에서 제공됩니다. .

### PST 형식 유형

PST 파일 형식은 파일 형식의 인코딩에 따라 두 가지 형식으로 분류됩니다. ANSI로 인코딩된 PST 파일은 이전 파일 형식이며 Outlook 2002 및 이전 버전에서만 지원됩니다. 이러한 파일의 최대 크기 제한은 2GB(2^^31^^ 바이트)이며 유니코드를 지원하지 않습니다. 유니코드 인코딩을 기반으로 하는 보다 현대적인 파일 형식 유형은 파일 크기 제한을 제거하고 최대 데이터 크기 50GB에 도달할 수 있습니다.

### PST 파일 형식의 논리적 구성

PST 파일 형식의 기반에는 데이터를 정렬된 상태로 유지하고 로그 시간에 검색, 순차 액세스, 삽입, 삭제 등을 허용하는 B-Tree가 있습니다. PST 파일의 전체 구조는 3개의 레이어로 구성됩니다.

![Logical layers of a PST file](/ko/email/PST-1.png "Logical layers of a PST file")

'노드 데이터베이스(NDB) 레이어' - 노드 데이터베이스 레이어는 PST 파일의 하위 수준에 있으며 노드 데이터베이스를 포함합니다. 이러한 노드는 실제로 PST 파일 형식의 하위 수준 저장 기능을 나타냅니다. NDB 계층은 스토리지 관점에서 헤더, 파일 할당 정보, 블록 및 BTree(Node BTree 및 블록 BTree)로 구성됩니다. NDB Layer의 Node와 Block은 Node reference의 4가지 속성인 NID(Node ID), Parent NID, Data BID(Block BID), SubNode BID 중 하나인 Data BID를 통해 연결됩니다.

`목록, 테이블 및 속성 계층 -` LTP 계층은 NDB 위에 있는 상위 수준 개념에 대한 논리적 이해를 제공합니다. 다른 요소 외에도 LTP 계층은 주로 PC(Property Context)와 TC(Table Context)로 구성됩니다. PC는 속성 모음이고 TC는 속성 모음 대 이러한 속성의 존재에 대한 2차원 매트릭스를 나타냅니다. PC 및 TC의 효율적인 구현인 LTP 계층은 NDB 노드 상단에서 다음 두 가지 유형의 데이터 구조를 사용합니다.

* HN(Heap On Node) - 노드의 데이터 스트림을 작은 가변 크기 조각으로 하위 할당할 수 있습니다.
* BTH(BTree on Heap) - BTH는 위에서 설명한 PC를 BTH로 구현하여 데이터를 검색하는 편리하고 실용적인 방법을 제공하므로 HN 구조 내부에 구축하여 구현합니다.

`Messaging Layer -` PST 파일 작업을 위한 더 높은 수준의 규칙과 비즈니스 로직이 이 레이어에서 구현됩니다. 이 계층의 논리적 출력은 LTP 및 NDB 계층을 결합하여 가능한 폴더 개체, 메시지 개체, 첨부 파일 개체 및 속성으로 나타납니다. PST 콘텐츠를 수정할 때 따라야 하는 규칙 및 요구 사항도 이 계층에서 정의됩니다.

### PST 파일 형식의 물리적 구성

PST 파일의 높은 수준의 파일 구성은 아래 그림과 같습니다. 이것은 PST 파일의 논리적 요소와 다른 개념에 대한 개요입니다.

![Physical organization of the PST file format](/ko/email/PST-2.png "Physical organization of the PST file format")


#### PST 헤더 정보

PST 파일의 HEADER 구조는 오프셋 0인 파일의 맨 처음에 위치합니다. PST 파일에 대한 메타데이터 정보와 위에서 설명한 NDB Layer 데이터 구조에 액세스하기 위한 ROOT 정보를 포함합니다. HEADER 구조는 유니코드 및 ANSI 버전의 PST 파일 형식에 따라 다릅니다.

헤더는 바이트(0x21, 0x42, 0x44, 0x4E)로 표시되는 4바이트 매직 워드 **!BDN**으로 시작합니다. 또 다른 2바이트 매직 넘버 **SM**(0x53, 0x4D)는 파일 시작에서 오프셋 8에 있습니다. 버전 정보(ANSI 또는 유니코드)는 파일 시작에서 오프셋 10에 있습니다. 16진수 값(0x17)은 유니코드 PST 파일을 지정하고 0x0E 또는 0x0F는 ANSI 파일 형식을 나타냅니다.

|필드|설명
---|---|
|dwMagic(4바이트)|"{ 0x21, 0x42, 0x44, 0x4E }("!BDN")"이어야 합니다.
|dwCRCPartial(4바이트)|wMagicClient(0ffset 0x0008)에서 시작하는 471바이트 데이터의 32비트 CRC 값
|wMagicClient(2바이트)|"{ 0x53, 0x4D }"여야 합니다.
|wVer(2바이트)|파일 형식 버전. 파일이 ANSI PST 파일인 경우 이 값은 14 또는 15여야 하고 파일이 유니코드 PST 파일인 경우 23이어야 합니다.
|wVerClient(2바이트)|클라이언트 파일 형식 버전. 이 문서에 설명된 형식에 해당하는 버전은 19입니다. 이 문서를 기반으로 하는 새 PST 파일의 작성자는 이 값을 19로 초기화해야 합니다(SHOULD).
|bPlatformCreate(1바이트)|이 값은 0x01로 설정되어야 합니다.
|bPlatformAccess(1바이트)|이 값은 0x01로 설정되어야 합니다.
|dw예약됨(8바이트)|
|bidUnused(8바이트 유니코드 전용)|유니코드 PST 파일 형식이 생성될 때 추가된 미사용 패딩.
|bidNextP(유니코드: 8바이트, ANSI: 4바이트)|다음 페이지 BID. 페이지에는 bidIndex 값을 할당하기 위한 특수 카운터가 있습니다. 페이지의 BID에 대한 bidIndex 값은 이 카운터에서 할당됩니다.
|bidNextB(4바이트 ANSI 전용): |다음 BID. 이 값은 다음 할당 블록에 할당될 BID를 나타내는 단조 카운터입니다. BID 값은 4씩 증가합니다. 자세한 내용은 섹션 2.2.2.2를 참조하십시오.
|dwUnique(4바이트)|PST 파일의 HEADER 구조가 수정될 때마다 수정되는 단조 증가 값입니다. 이 값의 기능은 고유한 값을 제공하고 각 헤더 수정 후에 HEADER CRC가 다른지 확인하는 것입니다.
|rgnid[]   (128바이트)|각각 32개의 가능한 NID_TYPE(NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE, NID_TYPE_ASSOC_MESSAGE) 중 하나에 해당하는 32개의 NID 고정 배열
|qwUnused(8바이트)|사용되지 않은 공간; 0으로 설정해야 합니다. 유니코드 PST 파일 형식 전용.
|루트(유니코드: 72바이트, ANSI: 40바이트)|ROOT 구조(섹션 2.2.2.5).
|dwAlign (4 바이트)|사용하지 않는 정렬 바이트; 0으로 설정해야 합니다. 유니코드 PST 파일 형식 전용.
|rgbFM(128바이트)|사용되지 않는 FMap. 이것은 더 이상 사용되지 않으며 0xFF로 채워져야 합니다. 리더는 이 바이트 값을 무시해야 합니다(SHOULD).
|rgbFP(128바이트)|사용되지 않는 FPMap. 이것은 더 이상 사용되지 않으며 0xFF로 채워져야 합니다. 리더는 이 바이트 값을 무시해야 합니다(SHOULD).
|bSentinel(1바이트)|0x80으로 설정해야 합니다.
|bCryptMethod(1바이트)|PST 파일 내의 데이터가 인코딩되는 방식을 나타냅니다. 미리 정의된 값(NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC) 중 하나로 설정해야 합니다(MUST).
|rgb예약됨(2바이트)| 예약된; 0으로 설정해야 합니다.
|bidNextB(8바이트)|사용 가능한 다음 BID 값을 나타냅니다. 유니코드 PST 파일 형식 전용.
|bidNextB(유니코드 전용: 8바이트)|다음 BID. 이 값은 다음 할당 블록에 할당될 BID를 나타내는 단조 카운터입니다. BID 값은 4씩 증가합니다. 자세한 내용은 섹션 2.2.2.2를 참조하십시오.
|dwCRCFull(4바이트)|wMagicClient에서 시작하여 bidNextB까지의 516바이트 데이터의 32비트 CRC 값입니다. 유니코드 PST 파일 형식 전용.
|ullReserved(8바이트)|예약됨; 0으로 설정해야 합니다. ANSI PST 파일 형식 전용.
|dwReserved(4바이트)|예약됨; 0으로 설정해야 합니다. ANSI PST 파일 형식 전용.
|rgbReserved2(3바이트)|
|b예약됨(1바이트) |
|rgbReserved3(32바이트) |

### 데이터 보호 ###

보안을 위해 PST 파일을 암호로 보호할 수도 있습니다. 로드 응용 프로그램에서 보기 전에 암호를 적용해야 합니다. PST 파일에 적용된 비밀번호는 메시지 저장소에 저장됩니다. 그러나 사용 가능한 도구로 암호를 제거할 수 있으므로 강력한 데이터 보호 기능을 제공하지 않습니다. 또한 사용자 지정 암호는 암호 알고리즘을 인코딩 및 디코딩하기 위한 키의 일부로 사용되지 않습니다. 따라서 승인되지 않은 당사자가 액세스하는 데이터를 보호하는 이점이 없습니다. 암호를 원래 문자열의 CRC-32 해시로 저장하는 것도 무차별 대입 접근에 대한 데이터 보안에 약한 방법이 됩니다.

## 참조 ##

* [Outlook 개인 폴더(.pst) 파일 형식](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [개인 폴더 파일 형식 사양](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

