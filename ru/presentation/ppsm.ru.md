{
  "date" : "2019-10-11",
  "keywords" :[ "файл ppsm", "формат файла ppsm", "что такое файл ppsm", "файл", "пример ppsm", "расширение файла ppsm", "расширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PPSM — файл презентации PowerPoint с поддержкой макросов",
  "description":"Узнайте о формате файла PPSM и API-интерфейсах, которые могут создавать и открывать файлы PPSM.",
  "linktitle" : "PPSM",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## .PPSM вариант №

Файлы с расширением PPSM представляют собой формат файлов слайд-шоу с поддержкой макросов, созданный с помощью Microsoft PowerPoint 2007 или более поздней версии. Другим похожим форматом файла является [PPTM](/ru/presentation/pptm/), который отличается тем, что открывается с помощью Microsoft PowerPoint в редактируемом формате, а не в виде слайд-шоу. При запуске в виде слайд-шоу файл PPSM показывает слайды презентации с неповрежденным содержимым в слайд-шоу и по умолчанию находится в режиме только для чтения. Файлы PPSM по-прежнему можно редактировать в Microsoft PowerPoint, открыв их в PowerPoint.

## Формат файла ##

Формат файла PPSM был представлен в PowerPoint 2007 и основан на формате файла OpenXML, в котором для хранения содержимого используется комбинация XML и [ZIP](/ru/compression/zip/). Файлы, созданные с помощью офисного формата файлов Open XML, представляют собой набор файлов XML вместе с другими файлами, которые обеспечивают связи между всеми составными файлами. Эта коллекция на самом деле представляет собой сжатый архив, который можно распаковать, чтобы просмотреть его содержимое. Для этого просто переименуйте расширение файла PPSM в zip и извлеките его, чтобы просмотреть его содержимое.

Следующие разделы проливают свет на каждый из них.

### [Типы содержимого].xml ###

Это единственный файл, который находится на базовом уровне при распаковке zip-архива. В нем перечислены типы содержимого для частей внутри пакета. Все ссылки на XML-файлы, включенные в пакет, указаны в этом XML-файле. Ниже приведен тип содержимого для части слайда:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Если в пакет необходимо добавить новые части, это можно сделать, добавив новую часть и обновив все отношения в файлах .rels. Следует иметь в виду, что для такого изменения необходимо также обновить Content_Types.xml.

### \_rels (папка) ###

Отношения между другими частями и ресурсами вне пакета поддерживаются частью отношений. Папка «Отношения» содержит один XML-файл, в котором хранятся отношения на уровне пакетов. Ссылки на ключевые части файлов презентации содержатся в этом файле в виде URI. Эти URI определяют тип отношения каждой ключевой части к пакету. Это включает отношение к основному офисному документу, расположенному как ppt/presentation.xml, и другим частям в docProps в качестве основных и расширенных свойств.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```
Каждая часть документа, являющаяся источником одного или нескольких взаимосвязей, будет иметь свою собственную часть взаимосвязей, где каждая такая часть взаимосвязи находится в подпапке \_rels части и именуется путем добавления '.rels' к имени часть. Основная часть содержимого (presentation.xml) имеет собственную часть отношений (presentation.xml.rels). Он содержит связи с другими частями содержимого, такими как slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml, а также URI для внешних ссылок.

#### Явная связь ####

Для явной связи ресурс ссылается с использованием атрибута Id объекта.<Relationship> элемент. То есть идентификатор в источнике сопоставляется непосредственно с идентификатором элемента отношения с явной ссылкой на цель.

Например, слайд может содержать такую гиперссылку:
```
<a:hlinkClick r:id#"rId2">
```
r:id#"rId2" ссылается на следующую связь в части отношений для слайда (slide1.xml.rels).
```
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
```
#### Неявная связь ####

Для неявной связи нет такой прямой ссылки на `<Relationship> Идентификатор`. Вместо этого ссылка понимается.

### Папка ppt ###

Это основная папка, содержащая все подробности о содержимом презентации. По умолчанию он имеет следующие папки:

* \_rels
* тема
* слайды
* макеты слайдов
* мастера слайдов

и следующие xml-файлы:

* презентация.xml
* преспропс.xml
* таблицаСтили.xml
* viewProps.xml

## Использованная литература ##

* [Формат файла презентации OpenXML] (https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [Open Office XML] (http://officeopenxml.com/anatomyofOOXML-pptx.php)
