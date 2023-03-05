{
  "date" : "2019-10-11",
   "keywords": [ "sln file", "how to run a sln file", "sln", "extension", "format", "What is sln file", "sln file format", "Visual Studio Solution", "Visual Studio solution VS project" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"СЛН",
  "description":"Узнайте о формате файла SLN и API-интерфейсах, которые могут создавать и открывать файлы SLN.",
  "linktitle" : "SLN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## SLN вариант №
Файл с расширением .SLN представляет собой файл решения **Visual Studio**, в котором хранится информация об организации проектов в файле решения. Содержимое такого файла решения записывается в виде простого текста внутри файла, и его можно просмотреть/отредактировать, открыв файл в любом текстовом редакторе. Информация, содержащаяся в файле решения, остается постоянной и используется для загрузки информации, связанной с решением, такой как [проекты](/ru/programming/csproj/) и любой другой необходимой информации. Файлы проекта, на которые ссылается файл решения, содержат дополнительную информацию, позволяющую среде заполнять иерархию элементами этого проекта. Никакие данные не сохраняются в файле .sln, хотя при необходимости информация о проекте может быть записана в файл .sln.

## **История версий SLN** ##

Версия формата решения менялась с каждым решением Microsoft Visual Studio с течением времени. Подробности о них следующие.


|Версия Visual Studio|Версия формата решения
---|---|
|2003|8.00
|2005|9.00
|2008|10.00
|2010|11.00
|2013|12.00
|2015|12.00
|2017|12.00

### **Содержимое файла решения** ###

Файл решения состоит из нескольких разделов, которые считываются средой для загрузки проекта. Пример содержимого файла .sln показан ниже.

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

### **Декларация проекта** ###

Файл решения может содержать более одного объявления проектов, а также разных типов проектов. Например, один файл решения может содержать как проект CSharp, так и проект VB.NET. Эти типы различаются в решении с помощью [Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUID). Приведенную выше декларацию проекта можно обобщить следующим образом для ясности понимания.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`Project-Type-GUID:` Project-Type-GUID уникален для различных типов проектов и используется программой чтения решений для определения типа проекта. В данном случае F184B08F-C81C-45F6-A57F-5ABD9991F28F показывает, что это проект VB.NET.

`Project GUID:` Уникальный GUID проекта, который отличает его от других проектов в решении. Уникальный идентификатор проекта в решении позволяет другим проектам в решении получить к нему доступ.

На основе информации, содержащейся в разделе проекта файла .sln, среда загружает каждый файл проекта. Затем сам проект отвечает за заполнение иерархии проектов и загрузку любых вложенных проектов. Любые изменения, внесенные в решение, сохраняются обратно в файл решения при сохранении или закрытии проекта.

## Решение Visual Studio VS проект

**Проект.** По логике вещей, когда вы начинаете создавать приложение или программное обеспечение с помощью Visual Studio, вы начинаете новый проект. Проект содержит все необходимые файлы, такие как исходный код, значки, изображения, файлы данных и т. д., которые будут скомпилированы в исполняемое приложение, веб-сайт или библиотеку.

**Решение.** Решение содержит один или несколько проектов. Таким образом, решение похоже на контейнер для проектов Visual Studio. Логически можно сказать, что кто-то хочет получить комплексное решение для своего бизнеса, включая веб-сайт, настольное приложение, сервис для отдыха и мобильное приложение.

### **Использованная литература** ###

* [Файл решения — по MSDN](https://docs.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)
* [GUID типа проекта](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUID)

