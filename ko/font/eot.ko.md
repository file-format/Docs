{
  "date" : "2020-08-20",
  "keywords" :[ "eot 파일", "eot 파일 형식", "eot 파일이란", "파일", "eot 예", "eot 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EOT - 트루타입 글꼴 파일 형식",
  "description":"EOT 파일 형식 및 API를 사용하여 EOT 파일을 만들고 여는 방법에 대해 알아보세요.",
  "linktitle" : "EOT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## .EOT 파일이란?

확장자가 .eot인 파일은 문서에 포함된 OpenType 글꼴입니다. 이들은 주로 웹 페이지와 같은 웹 파일에서 사용됩니다. 마이크로소프트에서 제작했으며 파워포인트 프레젠테이션[.pps](/ko/presentation/pps) 파일을 포함한 마이크로소프트 제품에서 지원한다. 파일은 주요 용도가 아니며 기본 문서 또는 웹 페이지와 함께 제공되는 일종의 문서입니다. OTF 글꼴과 유사하게 EOT는 글리프에 대해 Postscript 및 TrueType 윤곽선을 모두 지원합니다. EOT 파일은 LZ 압축을 사용하여 압축되기 때문에 크기가 더 작습니다. EOT는 Microsoft 도구를 사용하여 기존 TTF/OTF 글꼴에서 글꼴을 만듭니다.

## 약력

EOT 글꼴은 2007년 CSS3의 일부로 W3C에 제출되었지만 원격 시스템에 영구적으로 설치해야 하는 요구 사항으로 인해 거부 사유가 되었습니다. 2008년 3월에 다시 제출했지만 W3C는 최종적으로 당시 표준화된 [Web Font Format](/ko/font/woff/) (WOFF)을 선택했습니다.

## EOT 파일 형식

EOT 파일 형식에 대한 자세한 내용은 [W3 제출 페이지](https://www.w3.org/Submission/EOT/#FileFormat)에서 찾을 수 있으며 이 글꼴 형식이 사용하는 구조를 자세히 설명합니다. EOT는 글꼴 이름과 지원되는 문자에 대한 충분한 기본 정보를 제공하는 단일 EMBEDDEDFONT 구조로 구성됩니다. 이 정보를 압축하면 사용자 에이전트가 글꼴이 이미 컴퓨터에 있는 경우 압축 풀기, 압축 해제 또는 글꼴 설치를 방지할 수 있습니다.

### EMBEDDEDFONT 구조
EMBEDDEDFONT 구조는 세 번의 개정을 거쳤으며 각 개정과 함께 구조 끝에 추가 데이터가 추가되었습니다. EMBEDDEDFONT 구조체의 마지막 개정판은 아래와 같습니다.

|데이터 유형|항목 이름|설명|
---|---|---|
|unsigned long|EOTSize|바이트 단위의 전체 구조 길이(문자열 및 글꼴 데이터 포함)|
|unsigned long|FontDataSize|OpenType 글꼴(FontData)의 길이(바이트)|
|unsigned long|버전|이 형식의 버전 번호 - 0x00020002|
|unsigned long|플래그|플래그 처리|
|byte[10]|FontPANOSE|이 글꼴의 PANOSE 값 - 참조 http://www.microsoft.com/typography/otspec/os2.htm#pan|
|byte|Charset|Windows에서 이것은 TEXTMETRIC.tmCharSet에서 파생됩니다. 이 값은 글꼴의 문자 집합을 지정합니다. DEFAULT_CHARSET(0x01)은 기본 설정이 없음을 나타냅니다. - 참조 http://msdn2.microsoft.com/en-us/library/ms534202.aspx|
|byte|기울임꼴|ITALIC에 대한 비트가 OS/2.fsSelection에서 설정되면 값은 0x01이 됩니다. - http://www.microsoft.com/typography/otspec/os2.htm#fss를 참조하십시오.
|unsigned long|Weight|이 글꼴의 가중치 값 - http://www.microsoft.com/typography/otspec/os2.htm#wtc|를 참조하십시오.
|unsigned short|fsType|권한 포함에 대한 정보를 제공하는 유형 플래그 - http://www.microsoft.com/typography/otspec/os2.htm#fst|를 참조하십시오.
|unsigned short|MagicNumber|EOT 파일용 매직 넘버 - 0x504C. 데이터 손상을 확인하는 데 사용됩니다.|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1(비트 0-31) - http://www.microsoft.com/typography/otspec/os2.htm#ur| 참조
|unsigned long|UnicodeRange2|os/2.UnicodeRange2(비트 32-63) - http://www.microsoft.com/typography/otspec/os2.htm#ur| 참조
|unsigned long|UnicodeRange3|os/2.UnicodeRange3(비트 64-95) - http://www.microsoft.com/typography/otspec/os2.htm#ur| 참조
|unsigned long|UnicodeRange4|os/2.UnicodeRange4(비트 96-127) - http://www.microsoft.com/typography/otspec/os2.htm#ur| 참조
|unsigned long|CodePageRange1|CodePageRange1(비트 0-31) - http://www.microsoft.com/typography/otspec/os2.htm#cpr| 참조
|unsigned long|CodePageRange2|CodePageRange2(비트 32-63) - http://www.microsoft.com/typography/otspec/os2.htm#cpr| 참조
|unsigned long|CheckSumAdjustment|head.CheckSumAdjustment - 참조 http://www.microsoft.com/typography/otspec/head.htm|
|unsigned long|Reserved1|Reserved - 0이어야 함|
|unsigned long|Reserved2|Reserved - 0이어야 함|
|unsigned long|Reserved3|Reserved - 0이어야 함|
|unsigned long|Reserved4|예약됨 - 0이어야 함|
|unsigned short|Padding1|긴 정렬을 유지하기 위한 패딩. 패딩 값은 항상 0x0000으로 설정해야 합니다.|
|unsigned short|FamilyNameSize|FamilyName 배열이 사용하는 바이트 수|
|byte|FamilyName[FamilyNameSize]|FamilyNameSize 바이트 길이의 UTF-16 문자 배열. 이것은 글꼴의 이름 테이블에 있는 영어 글꼴 모음 문자열입니다(이름 ID = 1) - http://www.microsoft.com/typography/otspec/name.htm| 참조
|unsigned short|Padding2|패딩 값은 항상 0x0000으로 설정되어야 합니다.|
|unsigned short|StyleNameSize|StyleName이 사용하는 바이트 수|
|byte|StyleName[StyleNameSize]|UTF-16 문자 배열 StyleNameSize 바이트 길이. 이것은 글꼴의 이름 테이블에 있는 영어 글꼴 하위 계열 문자열입니다(이름 ID = 2) - http://www.microsoft.com/typography/otspec/name.htm| 참조
|unsigned short|Padding3|패딩 값은 항상 0x0000으로 설정되어야 합니다.|
|unsigned short|VersionNameSize|VersionName이 사용하는 바이트 수|
|bytes|VersionName[VersionNameSize]|VersionNameSize 바이트 길이의 UTF-16 문자 배열. 이것은 글꼴의 이름 테이블에 있는 영어 버전 문자열입니다(이름 ID = 5) - http://www.microsoft.com/typography/otspec/name.htm| 참조
|unsigned short|Padding4|패딩 값은 항상 0x0000으로 설정되어야 합니다.|
|unsigned short|FullNameSize|FullName이 사용하는 바이트 수|
|byte|FullName[FullNameSize]|FullNameSize 바이트 길이의 UTF-16 문자 배열. 이것은 글꼴의 이름 테이블에 있는 영어 전체 이름 문자열입니다(이름 ID = 4) - http://www.microsoft.com/typography/otspec/name.htm| 참조
|unsigned short|Padding5|패딩 값은 항상 0x0000으로 설정되어야 합니다.|
|unsigned short|RootStringSize|RootString 배열이 사용하는 바이트 수|
|byte|RootString[RootStringSize]|UTStringSize 바이트 길이의 UTF-16 문자 배열|
|unsigned long|RootStringCheckSum|RootString CheckSum 값. 아래 RootStringChecksum을 처리하는 알고리즘을 참조하십시오.|
|unsigned long|EUDCCodePage|EUDC 글꼴 지원에 필요한 코드 페이지 값.|
|unsigned short|Padding6|패딩 값은 항상 0x0000으로 설정되어야 합니다.|
|unsigned short|SignatureSize|서명 배열이 사용하는 바이트 수. 현재 예약되어 있으며 0x0000으로 설정되어야 합니다.|
|byte|서명[SignatureSize]|현재 예약되어 있습니다. SignatureSize가 0x0000이면 이 배열에 길이가 없습니다.|
|unsigned long|EUDCFlags|EUDC 글꼴에 대한 처리 플래그. 일반적인 값은 TTEMBED_XORENCRYPTDATA 및 TTEMBED_TTCOMPRESSED일 수 있습니다.|
|unsigned long|EUDCFontSize|서명 배열이 사용하는 바이트 수.|
|byte|EUDCFontData[EUDCFontSize]|EUDC 글꼴 데이터에 사용된 바이트 수. EUDCFontSize가 0x00000000이면 이 배열에 길이가 없습니다.|
|byte|FontData[FontDataSize]|이 EOT 파일의 글꼴 데이터. 데이터는 처리 플래그에 표시된 대로 압축되거나 XOR 암호화될 수 있습니다.|

## 참고문헌

* [EOT 파일 형식](https://www.w3.org/Submission/EOT/)
* [임베디드 오픈타입](https://en.wikipedia.org/wiki/Embedded_OpenType)
* [글꼴 임베딩](https://en.wikipedia.org/wiki/Font_embedding)

