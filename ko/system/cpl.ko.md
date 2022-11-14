{
  "date" : "2021-06-29",
  "keywords" :[ "CPL", "확장자", "파일", "형식", "시스템", "제어판 파일", "Windows", "프로그램", "컴퓨터", "응용 프로그램" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPL - 제어판 파일",
  "description":"CPL 파일 형식과 CPL 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "CPL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## .CPL 파일이란? ##

CPL 파일은 "시스템" 파일 유형입니다. Windows 운영 체제에서 사용됩니다. CPL 파일은 Control Panel File의 약자입니다. 이 파일은 Microsoft Windows 운영 체제의 제어판으로 열리는 바이너리 파일이며, 특히 마우스, 디스플레이, 네트워킹 등과 같이 제어판에서 사용할 수 있는 도구를 표시하고 여는 데 사용됩니다. CPL 파일은 일반적으로 장치의 시스템 폴더에 저장됩니다. 이러한 파일은 수동으로 열면 안 됩니다.


## CPL 파일 형식 ##

Windows 운영 체제의 서로 다른 CPL 파일은 서로 다른 제어판 항목을 나타내기 위해 연결됩니다. 모든 제어판 항목은 CPL 파일에 연결되어 있으며 항목에 접미사 ".cpl"이 첨부되어 있습니다.

형식이 있는 몇 가지 일반적인 유형의 CPL 파일은 다음과 같습니다.

* Inetcpl.cpl – 장치의 인터넷 속성용
* Appwiz.cpl – 장치에서 프로그램 속성을 추가하거나 제거하려면
* Desk.cpl – 디스플레이 속성용
* Main.cpl – 마우스, 글꼴, 키보드 및 프린터와 관련된 속성입니다.
* Netcpl.cpl – 네트워크 관련 속성의 경우
* System.cpl – 시스템 관련 속성 및 새 하드웨어 추가 마법사용
* TimeDate.cpl – 날짜 또는 시간 속성의 경우
* Mlcfg32.cpl – Microsoft Exchange 또는 Windows 메시징 속성의 경우
* Intl.cpl – 이는 국가별 설정 속성과 관련이 있습니다.
* Modem.cpl – 모뎀 관련 속성
* Themes.cpl – 바탕 화면 테마 및 속성을 저장합니다.
* Password.cpl – 비밀번호 속성용
* Mmsys.cpl – 멀티미디어 속성용
* Wgpocpl.cpl – Microsoft Mail 우체국 관련

## 간략한 역사 ##

CPL 파일 유형은 Microsoft Windows에 의해 개발되었으며 Windows 1.0 이후 Windows 운영 체제의 필수적인 부분입니다. 여전히 모든 Windows 버전에서 사용되며 모든 제어판 항목 속성은 이 파일 형식을 사용하여 저장됩니다.

## CPL 예 ##

샘플 CPL 파일은 아래에서 볼 수 있습니다.

```
<!-- Copyright (c) Microsoft Corporation -->
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity name="Microsoft.Windows.Net.ncpa" processorArchitecture="x86" version="5.1.0.0" type="win32"/>
<description>NCPA CPL</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="x86" 
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3">
    <security>
        <requestedPrivileges>
            <requestedExecutionLevel level="asInvoker" uiAccess="false"/>
        </requestedPrivileges>
    </security>
</trustInfo>
</assembly>

```
