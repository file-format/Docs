{
  "date" : "2019-10-11",
  "keywords": [ "csproj file", "csproj", "extension", "format", "What is a csproj file", "csproj file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSPROJ",
  "description":"CSPROJ 파일을 만들고 열 수 있는 API와 CSPROJ 파일 형식에 대해 알아보세요.",
  "linktitle" : "CSPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## CSProj 파일이란?
CSPROJ 확장자를 가진 파일은 시스템 어셈블리에 대한 참조와 함께 프로젝트에 포함된 파일 목록이 포함된 C# 프로젝트 파일을 나타냅니다. Microsoft VIiual Studio에서 새 프로젝트가 시작되면 기본 솔루션([.sln](/ko/programming/sln/)) 파일과 함께 하나의 .csproj 파일을 얻습니다. 프로젝트에 둘 이상의 어셈블리가 있는 경우 .sln 파일이 프로젝트의 일부로 이들을 모두 연결하는 동일한 수의 프로젝트 파일이 있습니다. 이 파일의 내용은 포함할 내용, 플랫폼 요구 사항, 버전 정보, 웹 서버 또는 데이터베이스 서버 설정, 수행해야 하는 작업 등 프로젝트를 빌드하는 데 필요한 모든 요구 사항을 정의합니다. 프로젝트 파일의 내용은 XML 파일 형식으로 정렬되며 편집 및 보기를 위해 모든 텍스트 편집기에서 열 수 있습니다. 또한 적절한 배열을 위해 프로젝트 파일에 대한 논리적 보기를 제공합니다.

## CSPROJ 파일 형식 #

개발자는 [MSBuild XML 스키마](https://msdn.microsoft.com/library/5dy88c2e.aspx)를 준수하면서 스스로 프로젝트 파일을 생성할 수 있습니다. 프로젝트 파일의 개방적이고 투명한 구조를 통해 애플리케이션 개발자는 프로젝트 구축 및 배포 방법을 정교하고 세밀하게 제어할 수 있습니다. 그러한 프로젝트 파일의 내용은 그들 사이에 매우 명확한 관계가 있습니다. 다음 그림은 이러한 프로젝트 파일에 대한 주요 요소와 이들 간의 관계를 보여줍니다.

![](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file/_static/image2.png)

다음 섹션에서는 프로젝트 파일의 파일 형식 요소를 자세히 설명합니다.

### 프로젝트 요소 ###

[Project](https://msdn.microsoft.com/library/bcxfsh87.aspx) 요소는 모든 프로젝트 파일의 루트 요소입니다. 프로젝트 파일에 대한 XML 스키마를 식별하고 빌드 프로세스의 진입점을 지정하는 속성을 포함할 수 있습니다.

```
<Project ToolsVersion#"4.0" DefaultTargets#"FullPublish"
        xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

### 속성 및 조건

속성은 프로젝트를 빌드하는 데 필요한 정보를 나타냅니다. 이러한 속성은 [PropertyGroup](https://msdn.microsoft.com/library/t4w159bs.aspx) 요소 내에서 정의됩니다. 이러한 속성은 속성 요소 이름이 속성 키를 정의하고 요소의 내용이 속성 값을 정의하는 키-값 쌍으로 구성됩니다. 예를 들어, 정적 서버 이름과 연결 문자열을 저장하기 위해 ServerName 및 ConnectionString이라는 속성을 정의할 수 있습니다.

```
<PropertyGroup>    
 <ServerName>FABRIKAM\TEST1</ServerName>
 <ConnectionString>
     Data Source#FABRIKAM\TESTDB;InitialCatalog#ContactManager,...
 </ConnectionString>
</PropertyGroup>
```

요소를 평가하기 위한 기준을 지정하기 위해 요소를 통해 조건을 지정할 수 있습니다. 이것은 아래와 같이 속성을 정의하는 동안 조건 단어로 지정됩니다.

```
<PropertyGroup>
<OutputRoot Condition#" '$(OutputRoot)'##'' ">..\Publish\Out\</OutputRoot>
   ...
</PropertyGroup>
```

MSBuild는 이 속성 정의를 처리할 때 먼저 **$(OutputRoot)** 속성 값을 사용할 수 있는지 여부를 확인합니다. 속성 값이 비어 있는 경우(즉, 사용자가 이 속성에 대한 값을 제공하지 않은 경우) 조건은 **true**로 평가되고 속성 값은 **..\Publish\Out.**으로 설정됩니다.

### 항목 및 항목 그룹

프로젝트 파일은 실제로 다른 파일 유형인 빌드 프로세스에 대한 입력을 정의합니다. MSBuild 명명법에서 이러한 입력은 항목 요소로 표시되며 [ItemGroup](https://msdn.microsoft.com/library/646dk05y.aspx) 요소 내에서 정의됩니다. **Property** 요소와 마찬가지로 **Item** 요소의 이름을 원하는 대로 지정할 수 있습니다. 그러나 항목이 나타내는 파일 또는 와일드카드를 식별하려면 **Include** 속성을 지정해야 합니다.

```
<ItemGroup>
<ProjectsToBuild Include#"$(SourceRoot)ContactManager-WCF.sln"/>
</ItemGroup>
```

### 대상 및 작업

[Task](https://msdn.microsoft.com/library/77f2hx1s.aspx) 요소는 개별 빌드 명령(또는 작업)을 나타냅니다. MSBuild에는 미리 정의된 여러 작업이 포함되어 있습니다. 예를 들어:

* **복사** 작업은 파일을 새 위치로 복사합니다.
* **Csc** 작업은 Visual C# 컴파일러를 호출합니다.
* **Vbc** 작업은 Visual Basic 컴파일러를 호출합니다.
* **Exec** 작업은 지정된 프로그램을 실행합니다.
* **Message** 작업은 로거에 메시지를 씁니다.

작업은 항상 [Target](https://msdn.microsoft.com/library/t50z2hka.aspx) 요소 내에 포함되어야 합니다. **Target** 요소는 순차적으로 실행되는 하나 이상의 작업 집합이며 프로젝트 파일에는 여러 대상이 포함될 수 있습니다.

```
<Project xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
<Target Name#"LogMessage">
 <Message Text#"Hello world!" />
</Target>
</Project>
```

## 참고문헌

* [프로젝트 파일 이해 - MSDN](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project- 파일)

