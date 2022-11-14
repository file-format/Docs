{
  "date" : "2022-03-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VPK 파일 - PlayStation Vita 애플리케이션 패키지 파일 형식",
  "description":"VPK 파일 형식과 VPK 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-01"
}

## .VPK 파일이란?

확장자가 .vpk인 파일은 Sony PlayStation Vita 게임 콘솔에 타사 앱을 설치하는 데 사용되는 압축 아카이브 패키지 파일입니다. 이 파일은 PS Vita 및 PSTV가 사용자 제작 콘텐츠를 사용할 수 있도록 한 HENkaku의 탈옥 Vita PlayStation에만 설치할 수 있습니다. VPK 아카이브 파일에는 [PNG](/ko/image/png/) 파일과 같은 이미지, [.bin](/ko/disc-and-media/bin/)과 같은 설정 파일 및 [XML](/ko/web/xml/) 파일 형식의 모든 구성.

## VPK 파일 형식

VPK 파일은 표준 압축 [ZIP](/ko/compression/zip/) 아카이브로 디스크에 저장됩니다. 여기에는 Vita 게임 콘솔에 설치할 타사 앱에 대한 여러 폴더 및 기타 관련 파일이 포함될 수 있습니다. VPK 패키지 파일의 내용을 보려면 확장자를 .vpu에서 .zip으로 바꾸고 WinZip 또는 WinRAR과 같은 표준 압축 해제 유틸리티를 사용하여 내용을 추출하십시오.

Valvesoftware에는 개발자의 관점에서 참조할 수 있는 [VPK 파일 형식](https://developer.valvesoftware.com/wiki/VPK_File_Format)에 대한 자세한 정보가 있습니다.

## VPK 파일을 설치하는 방법?

VPK 파일은 명령줄 유틸리티 VPK.exe에서 설치할 수 있습니다. Windows OS에서는 모든 패키지 파일이 포함된 \*.vpk를 반환하는 vpk.exe 파일에 파일을 놓을 수 있습니다. 또는 다음과 같이 명령줄 도구를 사용할 수 있습니다.

### VPK 생성 및 파일 추가

```
vpk <dirname>
```

### VPK 파일 추출

```
vpk x <vpkfile> <filename1> <filename2> ...
```

## VPK 뷰어

* [VRF VPK 뷰어](https://github.com/SteamDatabase/ValveResourceFormat)

## 참고문헌

* [VPK 파일 형식](https://developer.valvesoftware.com/wiki/VPK_File_Format)
* [VPK 파일](https://developer.valvesoftware.com/wiki/VPK)

