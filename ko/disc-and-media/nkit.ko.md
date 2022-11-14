{
  "date" : "2022-04-01",
  "keywords" :[ "nkit 파일", "nkit 파일 형식", "nkit 파일이란", "파일", "nkit 예제", "nkit 파일 확장자","확장자", "형식", "nkit 바닥글", "파일 nkit의 형식"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"NKIT 파일 형식과 NKIT 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"NKIT - 디스크 이미지 파일 형식",
  "linktitle" : "NKIT",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-04-01"
}

## .NKIT 파일이란?

NKIT 파일은 NintendoWii 및 GameCube 게임에서 추출한 데이터의 디스크 이미지입니다. NKIT는 Nintendo Toolkit 형식입니다. 결과 압축 [ISO](/ko/compression/iso/) 파일은 Dolphin, Swiss 및 Nintendont와 같은 에뮬레이터 프로그램으로 실행되는 이러한 게임의 주요 데이터를 활용합니다. NKit은 보기 재생성과 크기를 유지하도록 설계된 원시(iso) 및 압축(gcz) 파일 형식으로 제공됩니다.

## NKIT 파일 형식

NKit 파일 형식은 손실이 없는 형식으로 Nintendo Wii 및 GameCube 이미지를 축소 및 복원하는 데 사용됩니다. 형식은 각 GameCube 및 Wii 게임에 대해 ISO 및 GCZ 파일 형식으로 제공됩니다.

|시스템 |포맷 |하드웨어 지원 |돌핀 지원 |1:1 복원 가능 |참고|
---|---|---|---|---|---|
|게임큐브| nkit.iso| 예 |예| 예 |압축된 GameCube iso와 동일|
|게임큐브| nkit.gcz| 아니오| 예| 예 |GCZ는 Dolphin의 자체 블록 탐색 가능 압축 형식입니다|
|Wii| nkit.iso| 아니요 예| 예| RVT-H 형식은 돌고래에서만 재생 가능|
|Wii| nkit.gcz| 아니요 예| 예| 돌핀에서만 플레이 가능한 GCZ의 RVT-H|

### NKIT 헤더

NKIT 파일 형식 헤더는 다음과 같습니다.

|오프셋 |길이 |이름|
---|---|---|
|0x200 |0x4 |NKit 헤더 'NKIT'|
|0x204 |0x4 |NKit 버전 ' v01'|
|0x208 |0x4 |소스 이미지 원본 CRC32|
|0x20C |0x4 |NKit CRC - NKit 파일 CRC32를 0x208(GCZ의 0x4)에서 소스 CRC와 동일하게 만듭니다.|
|0x210 |0x4 |소스 이미지 길이|
|0x214 |0x4 |강제 정크 ID(디스크 ID가 다른 경우 - 희귀 - GameCube만 해당)|
|0x218 |0x4 |변환할 때 제거된 경우 Wii 업데이트 파티션 CRC32|

## 참조 ##

* [NKIT 파일 형식 - gbatemp 기준](https://wiki.gbatemp.net/wiki/NKit/NKitFormat)

