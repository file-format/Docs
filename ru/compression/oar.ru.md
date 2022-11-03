{
  "date" : "2021-04-08",
  "keywords" :[ "файл весла", "формат файла весла", "что такое файл весла", "файл", "пример весла", "расширение файла весла", "расширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAR — формат файла архива OpenSimulator",
  "description":"Узнайте о формате файла OAR и API-интерфейсах, которые могут создавать и открывать файлы OAR.",
  "linktitle" : "OAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-15"
}

## .OAR вариант №

Файл с расширением .oar представляет собой архивный файл, используемый приложением OpenSimulator, которое представляет собой сервер 3D-приложений с открытым исходным кодом для создания виртуальной среды, доступной для нескольких пользователей по сети. Формат файла OAR предоставляет необходимые данные активов, необходимые для полной загрузки ландшафта, текстур объектов и инвентаря в другой системе. OpenSimulator также имеет дополнительную гиперсетку, которая позволяет пользователям посещать другие установки OpenSimulator в Интернете. Файлы OAR имеют интернет-приложение/весло типа MIME и содержат один или несколько заархивированных файлов.


## Формат файла OAR

OAR — это двоичные файлы, которые хранятся в формате сжатого архивного файла. Последней версией формата файлов OAR является [версия 1.0](http://opensimulator.org/wiki/OAR_Format_1.0), в которой есть существенные изменения по сравнению с предыдущей [версией 0.8](http://opensimulator.org/wiki/OAR_Format_0). .8). Последняя версия поддерживает хранение нескольких регионов в одном OAR и не имеет обратной совместимости с версиями OpenSimulator до 0.7.5. Файл OAR представляет собой сжатый tar-файл (tar.gz) в исходном формате tar unix (не USTAR).

## Пример регионов OAR
Файлы AOR могут содержать несколько областей. Структура архива следующая (данный пример содержит 4 региона):

```
archive.xml
assets/
regions/
  1_1_Arizona/
    landdata/
    objects/
    settings/
    terrain/
  2_1_New_Mexico/
    landdata/
    objects/
    settings/
    terrain/
  1_2_Utah/
    landdata/
    objects/
    settings/
    terrain/
  2_2_Colorado/
    landdata/
    objects/
    settings/
    terrain/
```
## Архив ОАР.xml

Файл управления архивом содержит основной номер версии для определения совместимости с будущими изменениями формата. Наличие активов в формате OAR указывается логическим элементом<assets_included> . Информация о включенных регионах содержится в манифесте, присутствующем в управляющем файле. Ниже приведен пример файла Archive.xml.

```
<?xml version="1.0" encoding="utf-16"?>
<archive major_version="1" minor_version="0">
  <creation_info>
    <datetime>1343204139</datetime>
  </creation_info>
  <assets_included>True</assets_included>
  <regions>
    <row>
      <region>
        <id>12345678-1111-1111-1111-111111111111</id>
        <dir>1_1_Arizona</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-2222-2222-2222-222222222222</id>
        <dir>2_1_New_Mexico</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
    <row>
      <region>
        <id>12345678-3333-3333-3333-333333333333</id>
        <dir>1_2_Utah</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-4444-4444-4444-444444444444</id>
        <dir>2_2_Colorado</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
  </regions>
</archive>
```

## использованная литература

* [Формат OAR v 1.0] (http://opensimulator.org/wiki/OAR_Format_1.0)
* [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

