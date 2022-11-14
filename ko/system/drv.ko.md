{
  "date" : "2021-07-08",
  "keywords" :[ "DRV", "확장자", "파일", "포맷", "시스템", "드라이버", "Windows 장치 드라이버", "프로그램", "컴퓨터", "응용 프로그램"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRV - Windows 장치 드라이버",
  "description":"DRV 파일을 만들고 열 수 있는 DRV 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "DRV",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## .DRV 파일이란? ##

.drv 확장자를 가진 파일은 Windows 장치 드라이버에 속합니다. Windows 운영 체제는 이러한 파일을 사용하여 내부 및 외부 하드 장치를 연결합니다. DRV 파일은 장치와 운영 체제가 함께 연결되는 방법에 대한 지침과 매개변수로 구성됩니다. 이 파일은 Windows에서 제대로 작동하도록 장치 드라이버를 설치하는 데 도움이 됩니다. 또한 버스나 케이블을 통해 PC의 마더보드와 연결된 장치에는 DRV 파일이 필요합니다.


## DRV 파일 형식 ##

DRV 파일은 일반적으로 동적 라이브러리([DDL](/ko/system/dll/) 파일) 또는 [EXE](/ko/executable/exe/) 파일로 패키지됩니다. 이러한 파일은 스마트폰과 같은 모든 시스템 플랫폼에서 지원될 수 있으며 각 플랫폼에서 이러한 파일을 적절하게 지원한다는 보장은 없습니다. 그러나 .drv 파일 확장자를 사용하는 가장 일반적인 장치는 다음과 같습니다.

* 사운드 카드
* 그래픽 카드
* 프린터
* 저장 장치
* 네트워크 어댑터
* 컴퓨터 하드웨어 액세서리

이메일로 전송된 DRV 파일은 바이러스 및 기타 악성 프로그램이 포함되어 있으므로 열지 않는 것이 좋습니다. 알 수 없는 DRV 파일을 열기 전에 포괄적인 검사를 수행하십시오.


## DRV 예 ##

```
// Include necessary files...
#include <font.defs>
#include <media.defs>
#include <hp.h>
#include <epson.h>
#include <label.h>

// Localizations are provided for all of the base languages supported by
// CUPS...
#po ar ""
#po ca ""
#po de ""
#po el ""
#po es ""
#po fr ""
#po no ""
#po ru ""
#po sk ""
#po sv ""
#po th ""
#po tr ""
#po uk ""

// MediaSize sizes used by label drivers...
#media "w90h18/1.25x0.25\"" 90 18
#media "w90h162/1.25x2.25\"" 90 162
#media "w108h18/1.50x0.25\"" 108 18
#media "w108h36/1.50x0.50\"" 108 36
#media "w108h72/1.50x1.00\"" 108 72
#media "w108h144/1.50x2.00\"" 108 144
#media "w144h26/2.00x0.37\"" 144 26
#media "w576h360/8.00x5.00\"" 576 360
#media "w576h432/8.00x6.00\"" 576 432
#media "w576h468/8.00x6.50\"" 576 468

// Common stuff for all drivers...
Attribute "cupsVersion" "" "2.2"
Attribute "FileSystem" "" "False"
Attribute "LandscapeOrientation" "" "Plus90"
Attribute "TTRasterizer" "" "Type42"

Font *

Version "2.1"

// Dymo Label Printer
{
  Manufacturer "Dymo"
  ModelName "Label Printer"
  Attribute NickName "" "Dymo Label Printer"
  PCFileName "dymo.ppd"
  DriverType label
  ModelNumber $DYMO_3x0
  Throughput 8
  ManualCopies Yes
  ColorDevice No

  HWMargins 2 14.9 2 14.9

  *MediaSize w81h252
  MediaSize w101h252
  MediaSize w54h144
  MediaSize w167h288
  MediaSize w162h540
  MediaSize w162h504
  MediaSize w41h248
  MediaSize w41h144
  MediaSize w153h198

  Resolution k 1 0 0 0 136dpi
  Resolution k 1 0 0 0 203dpi
  *Resolution k 1 0 0 0 300dpi

  Darkness 0 Light
  Darkness 1 Medium
  *Darkness 2 Normal
  Darkness 3 Dark
}

```

