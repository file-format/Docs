{
  "date" : "2019-10-11",
  "keywords" :[ "vcxproj", "файл", "розширення", "формат файлу", "Проект Visual C++", "Посібник з програмування" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCXPROJ",
  "description":"Дізнайтеся про формат файлу VCXPROJ та API, які можуть створювати та відкривати файли VCXPROJ.",
  "linktitle" : "VCXPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Що таке файл VCXPROJ?

Файл із розширенням .vcxproj — це файл проекту Microsoft Visual C++, у якому зберігається інформація про проект [C++](/uk/programming/cpp/). Він містить інформацію, яка використовується системою проекту MSBuild для компіляції та створення остаточного результату. VCXPROJ проектів Visual C++ такий самий, як [CSPROJ](/uk/programming/csproj/) для проектів .NET. Файли VCXPROJ не містять жодного коду, але посилаються на всі класи, цілі та властивості, визначені для проекту для створення проекту. Їх можна відкрити в текстових редакторах або, бажано, в Microsoft Visual Studio IDE.


## Формат файлу VCXPROJ - Додаткова інформація

Файли VCXPROJ – це текстові файли, створені у форматі [XML](/uk/web/xml/). Їх можна відкрити в будь-якому текстовому редакторі, але настійно рекомендується використовувати Microsoft Visual Studio IDE для відкриття та редагування цих файлів. Вони не призначені для редагування вручну. Помилки можуть призвести до аварійного завершення роботи IDE або неочікуваної поведінки.

Нижче наведено вміст зразка файлу VCXPROJ.

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
### Елементи файлу VCXPROJ

Типовий файл VCXPROJ містить низку елементів, як можна побачити у прикладі XML вище. [Структура VCXPROJ](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) від Microsoft детально пояснює кожен елемент файлу, і до нього можна звернутися з точки зору розробника.

#### Елемент проекту

Це кореневий вузол файлу VCXPROJ. MSBuild використовує цей елемент для читання версії збірки та цілі за замовчуванням для компіляції.

#### Project Configurations ItemGroup Element

Він містить інформацію про конфігурацію проекту, яка може включати метод збірки (Debug або Release), 32- або 64-розрядну компіляцію, параметри оптимізації та інші. Інформація в цій групі використовується IDE для завантаження проекту.

#### Елементи конфігурації проекту

Елементи ProjectConfiguration у файлі VCXPROJ містять інформацію про збірку та платформу, для якої завантажено проект. Його назва має відповідати формату `$(Конфігурація)|$(Платформа)`.

#### Глобальний елемент PropertyGroup

Цей розділ містить параметри, які надають інформацію для рівня проекту, наприклад:

* ProjectGuid
* Кореневий простір імен
* ApplicationType або ApplicationTypeRevision


## Список літератури

* [Структура VCXPROJ – MSDN](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)
* [Файли проекту C++](https://learn.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)

