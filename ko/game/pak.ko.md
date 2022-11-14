{
  "date" : "2021-10-20",
  "keywords" :[ ".pak", "파일 형식", "pak 파일이란", "파일", "pak 예제", "비디오 게임 패키지 파일","확장자"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":".pak 파일과 PAK 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"PAK 파일 형식 - 비디오 게임 패키지 파일",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## .PAK 파일이란?

PAK 파일은 게임 데이터를 보관하기 위해 다른 비디오 게임에서 만든 패키지 파일입니다. 기본적으로 게임 파일 형식입니다. 여기에는 다른 게임 데이터와 함께 그래픽, 텍스처, 사운드, 개체와 같은 여러 게임 요소가 포함될 수 있습니다. 아카이브는 대부분 .zip 파일로 저장되며 WinZip 및 WinRAR와 같은 널리 사용되는 압축 해제 소프트웨어로 추출할 수 있습니다. PAK 파일을 사용하는 비디오 게임의 예로는 Quake, Hexen, Crysis 및 Half-Life가 있습니다.

## PAK 파일 형식 - 추가 정보

대부분의 경우 PAK 파일은 [ZIP 파일 형식](/ko/compression/zip/)으로 저장됩니다. 그러나 다른 응용 프로그램은 이러한 파일을 저장하기 위해 다른 파일 형식을 사용할 수 있습니다.


## .PAK 파일 여는 방법? .

[PakExplorer](https://www.quaketerminus.com/tools.shtml) 및 [SpriteExplorer](http://www.slackiller.com/hlprograms.htm)와 같은 응용 프로그램으로 PAK 파일을 열 수 있습니다.

**------------------------------------------------ -------------------------------------------------- -----------------------**

## PAK 파일 형식 - Simutrans 개체 파일

확장자가 .pak인 파일은 [Simutrans](https://www.simutrans.com/en/) 교통 시뮬레이션 게임 파일 형식입니다. 사용자가 만든 그래픽 및 데이터 콘텐츠와 같이 시뮬레이션에 사용된 개체가 포함되어 있습니다. 여기에는 게임 차량, 건물, 지형 등과 같은 여러 다른 개체가 있을 수 있습니다. PAK 파일은 이러한 시뮬레이션 개체를 만들기 위해 .dat 파일과 .png 그림을 컴파일하는 유틸리티인 MakeObject를 사용하여 생성됩니다. Simutrans를 통해 플레이어는 육상으로 승객, 우편 및 상품을 위한 운송 시스템을 구축 및 관리하여 성공적인 운송 시스템을 운영할 수 있습니다.

## PAK 파일을 만드는 방법?

Simutrans는 Windows 및 Linux OS에서 PAK 파일을 생성하기 위한 샘플 예제를 나열했습니다.

### 윈도우 OS

```
simutrans_src
   makeobj.exe
   haus_01
        haus_01.dat
        haus_01.png
        pak.bat
   auto_03
        auto_03.dat
        auto_03.png
        pak.bat
   triebzug_01
        triebzug_vorn.dat
        triebzug_mitte.dat
        triebzug_hinten.dat
        triebzug_01.png
        pak.bat
```
### 리눅스 BE/OS

```
simutrans_src
   makeobj
   haus_01
        haus_01.dat
        haus_01.png
        pak
   auto_03
        auto_03.dat
        auto_03.png
        pak
   triebzug_01
        triebzug_v.dat
        triebzug_m.dat
        triebzug_h.dat
        triebzug_01.png
        pak
```

## 참고문헌

* https://simutrans-germany.com/wiki/wiki/en_doPak
* https://en.wikipedia.org/wiki/Simutrans

