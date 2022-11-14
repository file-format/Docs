{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OST - Outlook 저장 파일 형식",
  "description":"OST 파일을 만들고 열 수 있는 OST 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "OST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## .OST 파일이란?

OST 또는 오프라인 저장소 파일은 Microsoft Outlook을 사용하여 Exchange Server에 등록할 때 로컬 컴퓨터의 오프라인 모드에서 사용자의 사서함 데이터를 나타냅니다. 서버와 연결 시 Microsoft Outlook을 처음 사용할 때 자동으로 생성됩니다. 파일이 생성되면 이메일 서버와 데이터가 동기화되어 이메일 서버와의 연결이 끊긴 경우에도 오프라인에서도 사용할 수 있습니다. OST 파일은 이메일, 연락처, 일정 정보, 메모, 작업 및 기타 유사한 데이터와 같은 사서함 항목을 사용할 수 있습니다. 사용자는 서버에 연결되지 않은 경우에도 OST 파일에 이메일 및 기타 데이터 항목을 생성할 수 있지만, 이는 서버와 동기화되지 않습니다. 연결이 설정되면 로컬 파일이 서버와 다시 동기화되어 서버와 로컬 복사본이 동일한 수준의 정보에 있게 됩니다.

## OST 파일 형식

OST(오프라인 저장소 테이블) 및 [PST](/ko/email/pst/)(개인 저장소 테이블) 파일 형식은 사용자의 이메일, 연락처 및 약속을 저장하는 데 해당하는 PFF(개인 폴더 파일) 형식으로 구성됩니다. PFF 파일의 데이터는 모든 날짜와 시간이 UTC의 FILETIME으로 표시되는 리틀 엔디안으로 저장됩니다. [MS-PST]는 두 가지 유형의 PFF를 정의합니다.

* 32비트 ANSI 형식
* 64비트 유니코드 형식

Microsoft에서 제공하는 PST 파일 형식[사양](https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx)은 OST 파일 형식에도 무료로 적용할 수 있으며 Open Specification Promise를 통한 취소 불가능한 특허 라이선스. 다음과 같은 구별 가능한 요소로 구성됩니다.

* 파일 헤더
* 파일 헤더 데이터
* 인덱스 분기 노드
* 인덱스 리프 노드
* (파일) 오프셋 인덱스
* (항목) 설명자 색인
* 로컬 디스크립터
* 항목 테이블 유형

### 헤더 정보

OST 파일의 HEADER 구조는 오프셋이 0인 파일의 맨 처음에 위치합니다. 여기에는 OST 파일에 대한 메타데이터 정보와 위에서 설명한 NDB 계층 데이터 구조에 액세스하기 위한 ROOT 정보가 포함됩니다. HEADER 구조는 OST 파일 형식의 유니코드 및 ANSI 버전에 따라 다릅니다.

헤더는 바이트(0x21, 0x42, 0x44, 0x4E)로 표시되는 4바이트 매직 워드 **!BDN**으로 시작합니다. 또 다른 2바이트 매직 넘버 **SM**(0x53, 0x4D)는 파일 시작에서 오프셋 8에 있습니다. 버전 정보(ANSI 또는 유니코드)는 파일 시작에서 오프셋 10에 있습니다. 16진수 값(0x17)은 유니코드 OST 파일을 지정하고 0x0E 또는 0x0F는 ANSI 파일 형식을 나타냅니다.

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
|rgnid[](128바이트)|각각 32개의 가능한 NID_TYPE(NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE, NID_TYPE_ASSOC_MESSAGE) 중 하나에 해당하는 32개의 NID 고정 배열
|qwUnused(8바이트)|사용하지 않은 공간; 0으로 설정해야 합니다. 유니코드 PST 파일 형식 전용.
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

## 참고문헌

* [Outlook 개인 폴더(.ost) 파일 형식](https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx)
* [개인 폴더 파일 형식 사양](https://github.com/libyal/libpff/blob/master/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

