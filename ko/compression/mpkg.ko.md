{
  "date" : "2019-10-11",
  "keywords" :[ "mpkg 파일", "mpkg 파일 형식", "mpkg 파일이란", "파일", "mpkg 예제", "mpkg 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPKG 파일 형식 - 메타 패키지 파일",
  "description":"MPKG 파일 형식과 MPKG 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "MPKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## .MPKG 파일이란?

확장자가 .mpkg인 파일은 대부분 MacOS 운영 체제에서 발견되는 아카이브 설치 프로그램 파일입니다. 관련 파일을 별도로 보관할 필요 없이 응용 프로그램에 필요한 모든 설치 파일이 포함되어 있습니다. 단일 MPKG 파일에는 패키지 파일[PKG](/ko/compression/pkg/)이 다른 파일과 함께 설치 파일 중 하나로 포함될 수 있습니다. MPKG 파일은 일반 소프트웨어로 열 수 없으며 Apple Installer를 사용하여 MacOS에서 자동으로 실행됩니다.

## MPKG 파일 형식

MPKG 파일에는 포함된 여러 패키지를 설치하는 데 필요한 다양한 유형의 파일이 포함되어 있습니다. 이는 샘플 MPKG 파일의 트리 구조인 아래 이미지에서 확인할 수 있습니다. 이 트리 구조는 MacOS 터미널에서 `tree` 명령을 사용하여 내보내집니다.

{{< figure src="../mpkg.png" alt="MPKG 파일 형식" >}}

이미지의 다른 요소에 대한 설명은 다음과 같습니다.

`Packages Directory` - pkg 파일 목록, 즉 하위 패키지 목록을 저장합니다.
`리소스 디렉토리` - 현지화된 리소스 및 이미지, Rtf 문서, pdf 문서 등과 같이 pkg에서 사용하는 리소스를 저장합니다.
`Distribution.dist 파일` - 설치할 하위 패키지 및 런타임 스크립트와 같은 정보가 포함된 xml 문서

MPKG 파일에 대한 샘플 XML 파일은 연관된 하위 패키지에 따라 다음과 같이 보일 수 있습니다.

```
<?xml version="1.0" encoding="utf-8" standalone="no"?>
<installer-script minSpecVersion="1.000000" authoringTool="com.apple.PackageMaker" authoringToolVersion="3.0.6" authoringToolBuild="201">
    <title>myframework installer</title>
    <options customize="never" allow-external-scripts="no" rootVolumeOnly="false"/>
    <installation-check script="pm_install_check();"/>
    <volume-check script="pm_volume_check();"/>
    <script>function pm_volume_check() {
  if(!(my.target.systemVersion &amp;&amp; /* &gt;= */ system.compareVersions(my.target.systemVersion.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}

function pm_install_check() {
  if(!(/ko/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}
</script>
    <choices-outline>
        <line choice="choice0"/>
    </choices-outline>
    <choice id="choice0" title="app">
        <pkg-ref id="com.macbook.myframeworkInstaller.pkg"/>
    </choice>
    <pkg-ref id="com.macbook.myframeworkInstaller.pkg" installKBytes="108" version="1.0" auth="Root">file:./Contents/Packages/app.pkg</pkg-ref>
</installer-script>
```
`app.pkg` - 설치할 하위 패키지입니다. pkg 형식의 번들 구조 디렉토리입니다. Contents 하위 디렉토리가 포함되어 있습니다.

## 참고문헌

* [OSX 플랫 패키지](https://matthew-brett.github.io/docosx/flat_packages.html)
* [C++ MPKG 패키지 관리자](https://github.com/puellavulnerata/mpkg)

