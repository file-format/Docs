{
  "date" : "2019-10-11",
   "keywords": [ "sln file", "how to run a sln file", "sln", "extension", "format", "What is sln file", "sln file format", "Visual Studio Solution", "Visual Studio solution VS project" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SLN",
  "description":"Дізнайтеся про формат файлу SLN та API, які можуть створювати та відкривати файли SLN.",
  "linktitle" : "SLN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Що таке файл SLN?
Файл із розширенням .SLN являє собою файл **рішення Visual Studio**, який зберігає інформацію про організацію проектів у файлі рішення. Вміст такого файлу рішення записується у вигляді звичайного тексту всередині файлу, і його можна переглядати/редагувати, відкривши файл у будь-якому текстовому редакторі. Інформація, що міститься у файлі рішення, залишається постійною та використовується для завантаження інформації, пов’язаної з рішенням, наприклад [projects ](/uk/programming/csproj/) та будь-якої іншої необхідної інформації. Файли проекту, на які посилається файл рішення, містять додаткову інформацію, щоб увімкнути середовище для заповнення ієрархії елементами цього проекту. У файлі .sln дані не зберігаються, хоча інформацію про проект можна записати у файл .sln, якщо потрібно.

## **Історія версій SLN** ##

Версія формату рішення розвивалася з кожним рішенням Microsoft Visual Studio з плином часу. Подробиці про них наведені нижче.


|Версія Visual Studio|Версія формату рішення
---|---|
|2003|8.00
|2005|9.00
|2008|10.00
|2010|11.00
|2013|12.00
|2015|12.00
|2017|12.00

### **Вміст файлу рішення** ###

Файл рішення складається з кількох розділів, які зчитуються середовищем для завантаження проекту. Зразок вмісту файлу .sln наведено нижче.

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

### **Проектна декларація** ###

Файл рішення може містити кілька декларацій проектів, а також різних типів проектів. Наприклад, один файл рішення може містити як CSharp, так і проект VB.NET. Ці типи розрізняються в рішенні за допомогою [Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs). Для чіткого розуміння наведену вище проектну декларацію можна узагальнити наступним чином.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`Project-Type-GUID:` Project-Type-GUID є унікальним для різних типів проектів і використовується читачем рішень для визначення типу проекту. У цьому випадку F184B08F-C81C-45F6-A57F-5ABD9991F28F показує, що це проект VB.NET.

`Project GUID`: унікальний GUID проекту, який відрізняє його від інших проектів у рішенні. Унікальний ідентифікатор проекту в рішенні дає змогу іншим проектам у рішенні отримати до нього доступ.

На основі інформації, що міститься в розділі проекту файлу .sln, середовище завантажує кожен файл проекту. Тоді сам проект відповідає за заповнення ієрархії проекту та завантаження будь-яких вкладених проектів. Будь-які зміни, внесені до рішення, зберігаються у файлі рішення після збереження або закриття проекту.

## Рішення Visual Studio VS проект

**Проект:** Логічно, коли ви починаєте створювати програму або програмне забезпечення за допомогою Visual Studio, ви починаєте новий проект. Проект містить усі необхідні файли, такі як вихідний код, значки, зображення, файли даних тощо, які будуть скомпільовані у виконувану програму, веб-сайт або бібліотеку.

**Рішення:** Рішення містить один або кілька проектів. Отже, рішення схоже на контейнер для проектів Visual Studio. За логікою ми можемо сказати, що хтось хоче отримати повне рішення для свого бізнесу, включаючи веб-сайт, програму для настільного комп’ютера, зручне обслуговування та програму для мобільних пристроїв.

### **Посилання** ###

* [Файл рішення – від MSDN](https://docs.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)
* [GUID типу проекту](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)

