{
  "date" : "2021-06-30",
  "keywords" :[ "mst 파일", "mst 파일 형식", "mst 파일이란", "파일", "mst 예", "mst 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"MST 파일 형식과 MST 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"MST - Windows Installer 패키지 파일",
  "linktitle" : "MST",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## .MST 파일이란?
확장자가 .mst인 파일은 MSI 패키지의 내용을 변환하는 데 사용됩니다. 시스템 관리자는 일반적으로 사용자 지정 설정을 기존 MSI 파일에 적용하는 데 사용합니다. MST 파일은 그룹 정책과 같은 소프트웨어 배포 시스템에서 원본 MSI 패키지와 함께 사용됩니다. MST 파일은 일반적으로 개발 중인 소프트웨어 버전을 구성하기 위한 소프트웨어 개발 및 테스트에 사용됩니다.

## MST 파일 형식
MST 또는 변환 파일은 파일에서 Microsoft Windows Installer를 사용하는 프로그램의 설치 옵션을 수집하는 데 사용됩니다. 이러한 파일은 일반적으로 설치 프로그램(MSIEXEC.EXE) 명령줄에서 사용되거나 소프트웨어 설치의 그룹 정책에서 사용됩니다. Microsoft Active Directory 도메인에서. MST 파일은 래핑된 실행 가능한 설치 프로그램과 함께 사용할 수도 있습니다. 일반적인 경우는 누군가가 명령줄 매개변수를 래핑된 설치 프로그램에 전달하려고 하는 것입니다. 이를 위해서는 WRAPPED_ARGUMENTS 속성을 속성 테이블에 추가하는 MST 파일이 필요합니다. 이러한 파일은 일반 편집기를 사용하여 만들거나 편집할 수 없습니다. 이를 위해 특정 도구를 사용할 수 있습니다.

### MST 파일을 사용하는 방법?
MST 파일은 다양한 도구를 사용하여 생성할 수 있으며 일반적으로 Ocra를 사용하여 MST 파일을 생성합니다. 그런 다음 필요에 따라 설정을 사용자 정의하고 특정 위치에 저장할 수 있습니다. 그 후 MST 파일을 MSI 파일과 함께 사용할 수 있습니다. 이 파일을 테스트하려면; 명령줄에서 다음 구문을 사용하십시오.

```
msiexec /i setup_1.0.msi TRANSFORMS=mylog.mst
```
### TRANSFORMS 속성

실제로 패키지를 설치할 때 설치 프로그램이 적용하는 변환 목록인 Windows 설치 프로그램의 **TRANSFORMS** 속성을 사용할 수도 있습니다. 설치 프로그램은 TRANSFORM 속성에 나열된 것과 동일한 순서로 변환을 실행합니다. 변환은 확장자가 .mst인 파일 이름 또는 전체 경로로 지정할 수 있습니다. 둘 이상의 변환을 지정하려면 다음 예와 같이 각 파일 이름 또는 세미콜론을 구분하십시오.

```
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
```

## 참고문헌

* [MST 변환 파일](https://www.exemsi.com/documentation/mst-transformation-files/)
* [TRANSFORMS 속성](https://learn.microsoft.com/en-us/windows/win32/msi/transforms)


