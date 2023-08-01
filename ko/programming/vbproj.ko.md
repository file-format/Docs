{
  "date" : "2019-10-11",
  "keywords" :[ "vbproj", "파일", "확장자", "파일 형식", "VB 프로젝트 파일", "프로그래밍 가이드" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBPROJ",
  "description":"VBPROJ 파일을 만들고 열 수 있는 VBPROJ 파일 형식 및 API에 대해 알아보세요.",
  "linktitle" : "VBPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## .VBPROJ 파일이란?

확장자가 .vbproj인 파일은 Microsoft의 MSBuild 엔진에서 Visual Studio 솔루션 내에서 프로젝트를 빌드하는 데 사용하는 Microsoft Visual Basic 프로젝트 파일입니다. [C#](/ko/programming/cs/)로 작성된 .NET 프로젝트용 [CSPROJ](/ko/programming/csproj/) 파일과 유사합니다. MSBuild 엔진은 VBPROJ 파일에서 다른 그룹에 포함된 정보를 읽고 출력 파일을 생성합니다. VBPROJ 파일에는 프로젝트를 정의하는 전역 식별자, 클래스 및 속성과 관련된 정보가 포함될 수 있습니다. VBPROJ 파일은 Microsoft Visual Studio와 Windows 및 MacOS 운영 체제의 메모장과 같은 일반적인 텍스트 편집기를 사용하여 열고 편집할 수 있습니다.

## VBPROJ 파일 형식 - 추가 정보

VBPROJ 파일은 [MSBuild XML Schema](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019)를 기반으로 [XML](/ko/web/xml/) 파일 형식으로 작성된 텍스트 파일입니다. VBPROJ 파일에는 특정 설정 그룹과 관련된 정보를 정의하는 XML 태그 형식의 정보가 포함되어 있습니다. Microsoft Visual Studio IDE에서 이러한 설정 파일을 열고 편집하는 것이 좋습니다.

### VBPROJ 요소

VB 설정 파일의 구성 요소는 다음 이미지와 같습니다.

{{< figure src="../vbproj.png" alt="VBPROJ 파일 형식" >}}

다음 표는 이러한 요소에 대한 간략한 설명을 제공합니다.

|요소|설명|
---|---|
|프로젝트| 모든 프로젝트 파일의 루트 요소이며 프로젝트 파일에 대한 XML 스키마를 식별하는 것 외에도 빌드 프로세스에 대한 진입점을 지정하는 속성을 포함할 수 있습니다.
|속성 및 조건| 속성은 키-값 쌍으로 구성되며 PropertyGroup 요소로 정의됩니다. 속성 요소 이름은 속성 키를 나타내고 요소의 내용은 속성 값을 정의합니다.|
|항목 및 항목 그룹|프로젝트 파일의 항목은 빌드 프로세스의 일부로 필요한 파일 코드 파일, 구성 파일, 명령 파일 및 기타와 같은 빌드 프로세스에 대한 입력입니다. 항목은 ItemGroup 요소 내에서 정의되어야 합니다.|
|대상 및 작업| Task 요소는 개별 빌드 명령(또는 작업)을 나타냅니다. MSBuild에는 Copy, CSC, VBC, Exec과 같은 미리 정의된 여러 작업이 포함되어 있습니다. 작업은 항상 순차적으로 실행되는 하나 이상의 작업 집합인 `Target` 요소에 포함되어야 하며 프로젝트 파일에는 여러 대상이 포함될 수 있습니다.|

## 참고문헌

* [프로젝트 파일 이해하기](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)
* [MSBuild 스키마 요소](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019)

