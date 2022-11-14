{
  "date" : "2021-04-08",
  "keywords" :[ "oar 파일", "oar 파일 형식", "oar 파일이란", "파일", "oar 예제", "oar 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAR - OpenSimulator 아카이브 파일 형식",
  "description":"OAR 파일을 만들고 열 수 있는 OAR 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "OAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-15"
}

## .OAR 파일이란?

확장자가 .oar인 파일은 네트워크를 통해 다중 사용자가 액세스할 수 있는 가상 환경을 만들기 위한 오픈 소스 3D 응용 프로그램 서버인 OpenSimulator 응용 프로그램에서 사용하는 아카이브 파일입니다. OAR 파일 형식은 다른 시스템에서 지형, 개체 텍스처 및 인벤토리를 완전히 로드하는 데 필요한 자산 데이터를 제공합니다. OpenSimulator에는 또한 사용자가 웹을 통해 다른 OpenSimulator 설치를 방문할 수 있도록 하는 선택적 하이퍼그리드가 있습니다. OAR 파일은 인터넷 MIME 유형 응용 프로그램/oar를 가지며 하나 이상의 아카이브 파일을 포함합니다.


## OAR 파일 형식

OAR은 압축된 아카이브 파일 형식으로 저장된 바이너리 파일입니다. OAR 파일 형식의 최신 버전은 [버전 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)으로 이전 [버전 0.8](http://opensimulator.org/wiki/OAR_Format_0 .8). 최신 버전은 단일 OAR에 여러 영역 저장을 지원하며 0.7.5 이전 버전의 OpenSimulator와 역호환되지 않습니다. OAR 파일은 USTAR가 아닌 원래 유닉스 tar 형식의 gzipped tar 파일(tar.gz)입니다.

## OAR 지역 예
AOR 파일에는 여러 영역이 포함될 수 있습니다. 아카이브의 구조는 다음과 같습니다(이 예에는 4개의 영역이 포함됨).

```
archive.xml
assets/
regions/
  1_1_Arizona/
    landdata/
    objects/
    settings/
    terrain/
  2_1_New_Mexico/
    landdata/
    objects/
    settings/
    terrain/
  1_2_Utah/
    landdata/
    objects/
    settings/
    terrain/
  2_2_Colorado/
    landdata/
    objects/
    settings/
    terrain/
```
## OAR 아카이브.xml

아카이브 제어 파일에는 향후 형식 변경과의 호환성을 정의하기 위한 주요 버전 번호가 포함되어 있습니다. OAR 형식의 자산이 있는지 여부는 부울 요소로 표시됩니다.<assets_included> . 포함된 영역에 대한 정보는 제어 파일에 있는 매니페스트에 포함됩니다. Archive.xml의 예는 다음과 같다.

```
<?xml version="1.0" encoding="utf-16"?>
<archive major_version="1" minor_version="0">
  <creation_info>
    <datetime>1343204139</datetime>
  </creation_info>
  <assets_included>True</assets_included>
  <regions>
    <row>
      <region>
        <id>12345678-1111-1111-1111-111111111111</id>
        <dir>1_1_Arizona</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-2222-2222-2222-222222222222</id>
        <dir>2_1_New_Mexico</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
    <row>
      <region>
        <id>12345678-3333-3333-3333-333333333333</id>
        <dir>1_2_Utah</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-4444-4444-4444-444444444444</id>
        <dir>2_2_Colorado</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
  </regions>
</archive>
```

## 참고문헌

* [OAR 형식 v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
* [오픈시뮬레이터](http://opensimulator.org/wiki/Main_Page)

