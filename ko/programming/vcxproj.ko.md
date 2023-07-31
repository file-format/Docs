{
  "date" : "2019-10-11",
  "keywords" :[ "vcxproj", "파일", "확장자", "파일 형식", "비주얼 C++ 프로젝트", "프로그래밍 가이드" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCXPROJ",
  "description":"VCXPROJ 파일을 만들고 열 수 있는 VCXPROJ 파일 형식 및 API에 대해 알아보세요.",
  "linktitle" : "VCXPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## .VCXPROJ 파일이란?

확장자가 .vcxproj인 파일은 [C++](/ko/programming/cpp/) 프로젝트 정보를 저장하는 Microsoft Visual C++ 프로젝트 파일입니다. 여기에는 MSBuild 프로젝트 시스템에서 최종 출력을 컴파일하고 빌드하는 데 사용하는 정보가 포함됩니다. Visual C++ 프로젝트의 VCXPROJ는 .NET 프로젝트의 [CSPROJ](/ko/programming/csproj/)와 동일합니다. VCXPROJ 파일은 코드를 포함하지 않지만 프로젝트를 빌드하기 위해 프로젝트에 대해 정의된 모든 클래스, 대상 및 속성을 참조합니다. 이들은 일반 텍스트 편집기 또는 가급적이면 Microsoft Visual Studio IDE에서 열 수 있습니다.


## VCXPROJ 파일 형식 - 추가 정보

VCXPROJ 파일은 [XML](/ko/web/xml/) 파일 형식으로 생성된 텍스트 파일입니다. 이러한 파일은 모든 텍스트 편집기에서 열 수 있지만 이러한 파일을 열고 편집하려면 Microsoft Visual Studio IDE를 사용하는 것이 좋습니다. 수동 편집용으로 설계되지 않았습니다. 실수로 인해 IDE가 충돌하거나 예기치 않은 방식으로 작동할 수 있습니다.

샘플 VCXPROJ 파일의 내용은 다음과 같습니다.

```
<Project DefaultTargets="Build" ToolsVersion="4.0" xmlns='http://schemas.microsoft.com/developer/msbuild/2003'>
  <ItemGroup Label="ProjectConfigurations" />
  <PropertyGroup Label="Globals" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.default.props" />
  <PropertyGroup Label="Configuration" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.props" />
  <ImportGroup Label="ExtensionSettings" />
  <ImportGroup Label="PropertySheets" />
  <PropertyGroup Label="UserMacros" />
  <PropertyGroup />
  <ItemDefinitionGroup />
  <ItemGroup />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.targets" />
  <ImportGroup Label="ExtensionTargets" />
</Project>
```
### VCXPROJ 파일 요소

일반적인 VCXPROJ 파일에는 위의 예제 XML에서 볼 수 있는 여러 요소가 포함되어 있습니다. Microsoft의 [VCXPROJ 구조](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)에서 각 파일 요소에 대해 자세히 설명하고 참조할 수 있습니다. 개발자의 관점에서.

#### 프로젝트 요소

이것은 VCXPROJ 파일의 루트 노드입니다. MSBuild는 이 요소를 사용하여 컴파일을 위한 빌드 버전 및 기본 대상을 읽습니다.

#### 프로젝트 구성 항목 그룹 요소

여기에는 빌드 방법(디버그 또는 릴리스), 32비트 또는 64비트 컴파일, 최적화 옵션 등이 포함될 수 있는 프로젝트 구성 정보가 포함됩니다. 이 그룹의 정보는 IDE에서 프로젝트를 로드하는 데 사용됩니다.

#### 프로젝트 구성 요소

VCXPROJ 파일의 ProjectConfiguration 요소에는 프로젝트가 로드되는 빌드 및 플랫폼에 대한 정보가 포함되어 있습니다. 이름은 `$(Configuration)|$(Platform)` 형식을 따라야 합니다.

#### 전역 PropertyGroup 요소

이 섹션에는 다음과 같은 프로젝트 수준에 대한 정보를 제공하는 설정이 포함되어 있습니다.

* 프로젝트 안내
* 루트 네임스페이스
* ApplicationType 또는 ApplicationTypeRevision


## 참고문헌

* [VCXPROJ 구조 - MSDN](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)
* [C++ 프로젝트 파일](https://learn.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)

