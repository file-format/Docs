{
  "date" : "2019-10-11",
   "keywords": [ "sln file", "how to run a sln file", "sln", "extension", "format", "What is sln file", "sln file format", "Visual Studio Solution", "Visual Studio solution VS project" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SLN",
  "description":"Научете за SLN файловия формат и API, които могат да създават и отварят SLN файлове.",
  "linktitle" : "SLN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Какво е SLN файл?
Файл с разширение .SLN представлява файл **решение на Visual Studio**, който съхранява информация за организацията на проектите във файл с решение. Съдържанието на такъв файл с решение е написано като обикновен текст във файла и може да бъде наблюдавано/редактирано чрез отваряне на файла във всеки текстов редактор. Информацията, съдържаща се във файл с решение, остава постоянна и се използва за зареждане на информацията, свързана с решението, като [projects](/bg/programming/csproj/) и всяка друга необходима информация. Файловете на проекта, посочени от файла на решението, съдържат допълнителна информация, за да активират средата за попълване на йерархията с елементи на този проект. В .sln файла не се съхраняват данни, въпреки че информацията за проекта може да бъде записана в .sln файла, ако е необходимо.

## **История на SLN версиите** ##

Версията на формата на решението е еволюирала с всяко решение на Microsoft Visual Studio с течение на времето. Подробностите за тях са както следва.


|Версия на Visual Studio|Версия на формата на решението
---|---|
|2003|8.00ч
|2005|9.00ч
|2008|10.00ч
|2010|11.00ч
|2013|12.00ч
|2015|12.00ч
|2017|12.00ч

### **Съдържание на файл с решение** ###

Файлът с решение се състои от няколко секции, които се четат от средата за зареждане на проекта. Примерно съдържание на .sln файл е показано по-долу.

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

### **Декларация за проекта** ###

Файлът с решение може да съдържа повече от една декларация на проекти и това също на различни типове проекти. Например един файл с решение може да съдържа както CSharp, така и VB.NET проект. Тези типове се разграничават в решение с помощта на [Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs). Горната декларация на проекта може да бъде обобщена, както следва за ясно разбиране.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`Project-Type-GUID:` Project-Type-GUID е уникален за различните типове проекти и се използва от четеца на решения за идентифициране на типа на проекта. В този случай F184B08F-C81C-45F6-A57F-5ABD9991F28F показва, че това е VB.NET проект.

`Project GUID:` Уникалният GUID на проекта, който го отличава от другите проекти в решението. Уникалният идентификатор на проект в решението дава възможност на други проекти в решението да имат достъп до него.

Въз основа на информацията, съдържаща се в проектния раздел на .sln файла, средата зарежда всеки проектен файл. Тогава самият проект отговаря за попълването на йерархията на проекта и за зареждането на всички вложени проекти. Всички промени, направени в решението, се записват обратно във файла на решението при записване или затваряне на проекта.

## Решение на Visual Studio VS проект

**Проект:** Логично, когато започнете да създавате приложение или софтуер с помощта на Visual Studio, стартирате нов проект. Проектът съдържа всички необходими файлове като изходен код, икони, изображения, файлове с данни и други, които ще бъдат компилирани в изпълнимо приложение, уебсайт или библиотека.

**Решение:** Едно решение съдържа един или повече проекти. Така че решението е точно като контейнер за проекти на Visual Studio. Логично можем да кажем, че някой иска да получи цялостно решение за своя бизнес, включително уебсайт, десктоп приложение, спокойна услуга и мобилно приложение.

### **Препратки** ###

* [Файл с решение – от MSDN](https://docs.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)
* [GUID за типове проекти] (https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)

