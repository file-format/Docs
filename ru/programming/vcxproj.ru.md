{
  "date" : "2019-10-11",
  "keywords" :[ "vcxproj", "файл", "расширение", "формат файла", "Проект Visual C++", "Руководство по программированию" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ВИКСПРОДЖ",
  "description":"Узнайте о формате файла VCXPROJ и API-интерфейсах, которые могут создавать и открывать файлы VCXPROJ.",
  "linktitle" : "VCXPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## .VCXPROJ вариант №

Файл с расширением .vcxproj представляет собой файл проекта Microsoft Visual C++, в котором хранится информация о проекте [C++](/ru/programming/cpp/). Он содержит информацию, которая используется системой проектов MSBuild для компиляции и создания окончательного вывода. VCXPROJ проектов Visual C++ такой же, как [CSPROJ](/ru/programming/csproj/) для проектов .NET. Файлы VCXPROJ не содержат никакого кода, но ссылаются на все классы, цели и свойства, определенные для проекта для создания проекта. Их можно открыть в текстовом редакторе или, что предпочтительнее, в Microsoft Visual Studio IDE.


## Формат файла VCXPROJ — дополнительная информация

Файлы VCXPROJ — это текстовые файлы, созданные в формате [XML](/ru/web/xml/). Их можно открыть в любом текстовом редакторе, но настоятельно рекомендуется использовать Microsoft Visual Studio IDE для открытия и редактирования этих файлов. Они не были предназначены для ручного редактирования. Ошибки могут привести к сбою или неожиданному поведению IDE.

Содержимое примера файла VCXPROJ следующее.

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
### Элементы файла VCXPROJ

Типичный файл VCXPROJ содержит ряд элементов, как показано в приведенном выше примере XML. [Структура VCXPROJ](https://docs.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) Microsoft подробно объясняет каждый элемент файла и может быть указан с точки зрения разработчика.

#### Элемент проекта

Это корневой узел файла VCXPROJ. MSBuild использует этот элемент для чтения версии сборки и цели по умолчанию для компиляции.

#### Элемент ItemGroup ProjectConfigurations

Он содержит информацию о конфигурации проекта, которая может включать метод сборки (отладка или выпуск), 32- или 64-разрядную компиляцию, параметры оптимизации и другие. Информация в этой группе используется IDE для загрузки проекта.

#### Элементы конфигурации проекта

Элементы ProjectConfiguration в файле VCXPROJ содержат информацию о сборке и платформе, для которых загружается проект. Его имя должно соответствовать формату `$(Конфигурация)|$(Платформа)`.

#### Элемент Globals PropertyGroup

Этот раздел содержит настройки, предоставляющие информацию для уровня проекта, такую как:

* Руководство по проекту
* Пространство корневых имен
* ApplicationType или ApplicationTypeRevision


## использованная литература

* [Структура VCXPROJ — MSDN](https://docs.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)
* [Файлы проекта C++](https://docs.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)

