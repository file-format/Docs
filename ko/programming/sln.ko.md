{
  "date" : "2019-10-11",
   "keywords": [ "sln file", "how to run a sln file", "sln", "extension", "format", "What is sln file", "sln file format", "Visual Studio Solution", "Visual Studio solution VS project" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SLN",
  "description":"SLN 파일 형식과 SLN 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "SLN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## .SLN 파일이란?
확장자가 .SLN인 파일은 프로젝트 구성에 대한 정보를 솔루션 파일에 보관하는 **Visual Studio 솔루션** 파일을 나타냅니다. 이러한 솔루션 파일의 내용은 파일 내부에 일반 텍스트로 작성되며 텍스트 편집기에서 파일을 열어 관찰/편집할 수 있습니다. 솔루션 파일에 포함된 정보는 지속적으로 유지되며 [projects ](/ko/programming/csproj/) 및 기타 필요한 정보와 같은 솔루션과 관련된 정보를 로드하는 데 사용됩니다. 솔루션 파일에서 참조하는 프로젝트 파일에는 해당 프로젝트 항목으로 계층 구조를 채우기 위한 환경을 활성화하는 추가 정보가 포함되어 있습니다. 필요한 경우 프로젝트 정보를 .sln 파일에 쓸 수 있지만 데이터는 .sln 파일에 저장되지 않습니다.

## **SLN 버전 기록** ##

솔루션 형식 버전은 시간이 지남에 따라 각 Microsoft Visual Studio 솔루션과 함께 발전해 왔습니다. 이에 대한 자세한 내용은 다음과 같습니다.


|Visual Studio 버전|솔루션 형식 버전
---|---|
|2003년|8.00
|2005년|9.00
|2008년|10.00
|2010년|11.00
|2013년|12.00
|2015년|12.00
|2017|12.00

### **솔루션 파일의 내용** ###

솔루션 파일은 프로젝트를 로드하기 위해 환경에서 읽는 여러 섹션으로 구성됩니다. 샘플 .sln 파일 내용은 아래와 같습니다.

```
Project("{F184B08F-C81C-45F6-A57F-5ABD9991F28F}") # "Project1", "Project1.vbproj", "{8CDD8387-B905-44A8-B5D5-07BB50E05BEA}"  
EndProject  
Global  
  GlobalSection(SolutionNotes) # postSolution  
  EndGlobalSection  
  GlobalSection(SolutionConfiguration) # preSolution  
       ConfigName.0 # Debug  
       ConfigName.1 # Release  
  EndGlobalSection  
  GlobalSection(ProjectDependencies) # postSolution  
  EndGlobalSection  
  GlobalSection(ProjectConfiguration) # postSolution  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.ActiveCfg # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.Build.0 # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.ActiveCfg # Release|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.Build.0 # Release|x86  
  EndGlobalSection  
  GlobalSection(ExtensibilityGlobals) # postSolution  
  EndGlobalSection  
  GlobalSection(ExtensibilityAddIns) # postSolution  
  EndGlobalSection  
EndGlobal
```

### **프로젝트 선언** ###

솔루션 파일에는 둘 이상의 프로젝트 선언과 서로 다른 프로젝트 유형의 선언이 포함될 수 있습니다. 예를 들어 단일 솔루션 파일에는 CSharp와 VB.NET 프로젝트가 포함될 수 있습니다. 이러한 유형은 [Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)를 사용하여 솔루션에서 구별됩니다. 위의 프로젝트 선언은 명확한 이해를 위해 다음과 같이 일반화할 수 있습니다.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`Project-Type-GUID:` Project-Type-GUID는 다양한 프로젝트 유형에 대해 고유하며 솔루션 리더에서 프로젝트 유형을 식별하는 데 사용됩니다. 이 경우 F184B08F-C81C-45F6-A57F-5ABD9991F28F는 VB.NET 프로젝트임을 나타냅니다.

`프로젝트 GUID:` 솔루션의 다른 프로젝트와 구별되는 프로젝트의 고유 GUID입니다. 솔루션에 있는 프로젝트의 고유 ID를 사용하면 솔루션에 있는 다른 프로젝트가 액세스할 수 있습니다.

.sln 파일의 프로젝트 섹션에 포함된 정보를 기반으로 환경은 각 프로젝트 파일을 로드합니다. 그러면 프로젝트 자체가 프로젝트 계층 구조를 채우고 중첩된 프로젝트를 로드하는 역할을 합니다. 솔루션에 대한 모든 변경 사항은 프로젝트를 저장하거나 닫을 때 솔루션 파일에 다시 저장됩니다.

## Visual Studio 솔루션 VS 프로젝트

**프로젝트:** 논리적으로 Visual Studio를 사용하여 앱이나 소프트웨어를 만들기 시작할 때 새 프로젝트를 시작합니다. 프로젝트에는 실행 가능한 앱, 웹사이트 또는 라이브러리로 컴파일될 소스 코드, 아이콘, 이미지, 데이터 파일 등과 같은 모든 필수 파일이 포함됩니다.

**솔루션:** 솔루션에는 하나 이상의 프로젝트가 포함되어 있습니다. 따라서 솔루션은 Visual Studio 프로젝트의 컨테이너와 같습니다. 논리적으로 누군가가 웹 사이트, 데스크톱 앱, 편안한 서비스 및 모바일 앱을 포함하여 자신의 비즈니스를 위한 완벽한 솔루션을 원한다고 말할 수 있습니다.

### **참고문헌** ###

* [솔루션 파일 - By MSDN](https://learn.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)
* [프로젝트 유형 GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)

