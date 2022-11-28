{
  "date" : "2020-03-16",
  "keywords" :[ "Файл IFC", "Формат", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Узнайте о формате файлов IFC и API-интерфейсах, которые могут создавать и открывать файлы IFC.",
  "title" :"Формат файла IFC",
  "linktitle" : "IFC",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## .IFC вариант №

Файлы с расширением IFC относятся к формату файлов Industry Foundation Classes (IFC), который устанавливает международные стандарты для импорта и экспорта строительных объектов и их свойств. Этот формат файла обеспечивает взаимодействие между различными программными приложениями. Спецификации для этого формата файла разрабатываются и поддерживаются BuildingSMART International в качестве стандарта данных. Конечной целью формата файла IFC является улучшение связи, производительности, времени доставки и качества на протяжении всего жизненного цикла здания.

Благодаря установленным стандартам для распространенных объектов в строительной индустрии снижается потеря информации при передаче из одного приложения в другое. IFC может хранить данные для геометрии, расчета, количества, управления объектами, ценообразования и т. д. для многих различных профессий (архитектор, электрик, HVAC, строительство, ландшафт и т. д.).

## Краткая история ##

Инициатива IFC была предпринята Autodesk в 1994 году для поддержки интегрированной разработки приложений и включала такие компании, как Honeywell, Butler Manufacturing и AT&T. В 1995 году членство было открыто для всех, и название было изменено на Международный альянс за интероперабельность. Целью некоммерческой организации было опубликовать Industry Foundation Class (IFC) в качестве модели продукта AEC. В 2005 году название снова было изменено, и теперь buildSMART поддерживает его.

## Формат файла IFC ##

В прошлом формат файла IFC претерпел несколько изменений, чтобы достичь спецификации формата файла v4. Время от времени происходило несколько незначительных изменений, которые были включены в спецификации в качестве дополнений. Ниже приведен список различных версий спецификаций файлов, которые были обнародованы в прошлом.

* IFC4 Дополнение 2 (2016 г.) IFC4 Дополнение 1 (2015 г.)
* IFC4 (март 2013 г.) ifcXML2x3 (июнь 2007 г.)
* IFC2x3 (февраль 2006 г.) ifcXML2 для IFC2x2 add1 (RC2)
* Приложение IFC2x2 1 (июль 2004 г.) ifcXML2 для IFC2x2 (RC1)
* Приложение IFC 2x2IFC 2x 1ifcXML1 для IFC2x и
* Приложение IFC2x 1IFC 2xIFC 2.0IFC 1.5.1IFC 1.5

Последние версии спецификаций формата файлов IFC всегда доступны на веб-сайте buildingSMART, и разработчик должен обращаться к ним для любого типа приложений, которые они планируют разрабатывать. На момент написания этой статьи спецификации версии 4 были последними доступными в Интернете.

### Форматы файлов данных IFC ###

Формат файла IFF поддерживает обмен данными между приложениями, использующими различные форматы, перечисленные ниже:

**IFC:** Это формат обмена IFC по умолчанию, в котором используется физическая файловая структура STEP в соответствии со стандартом ISO 10303-21. Этот формат файла имеет расширение .ifc и является наиболее часто используемым форматом IFC.

**IFC-XML:** Это версия IFC в формате файла XML, которая может быть создана непосредственно отправляющим приложением в соответствии со структурой ISO 10303-28, также называемой STEP-XML. Формат файла IFC-XML считается подходящим для взаимодействия инструментов XML. По сравнению с форматом файла IFC размер файла IFC-XML на 300–400 % больше.

**IFC-ZIP:** Это [ZIP](/ru/compression/zip/) сжатая версия IFC или IFC-XML, где один из этих файлов находится в основном каталоге zip-архива. Этот формат сжимает файл .ifc на 60–80 %, а XML-файл .ifc — на 90–95 %.

### Архитектура IFC ###

Спецификация IFC включает в себя термины, концепции и элементы спецификации данных, которые возникают в результате использования в рамках дисциплин, профессий и профессий в секторе строительства и управления объектами. В терминах и понятиях используются простые английские слова, элементы данных в спецификации данных следуют соглашению об именах.

имена элементов данных для типов, сущностей, правил и функций начинаются с префикса «Ifc» и продолжаются английскими словами в соглашении об именах CamelCase (без подчеркивания, первая буква в слове в верхнем регистре); имена атрибутов внутри объекта следуют соглашению об именах CamelCase без префикса; определения наборов свойств, которые являются частью этого стандарта, начинаются с префикса «Pset_» и продолжаются английскими словами в соглашении об именах CamelCase; определения наборов величин, которые являются частью этого стандарта, начинаются с префикса «Qto_» и продолжаются английскими словами в соглашении об именах CamelCase.

Архитектура схемы данных IFC определяет четыре концептуальных уровня, каждая отдельная схема назначается ровно одному концептуальному уровню.

**Ресурсный уровень** — самый нижний уровень включает в себя все отдельные схемы, содержащие определения ресурсов, эти определения не включают глобально уникальный идентификатор и не должны использоваться независимо от определения, объявленного на более высоком уровне;

**Основной уровень** — следующий уровень включает в себя схему ядра и схемы расширения ядра, содержащие наиболее общие определения сущностей, все сущности, определенные на базовом уровне или выше, имеют глобально уникальный идентификатор и, возможно, информацию о владельце и истории;

**Уровень функциональной совместимости** — следующий уровень включает схемы, содержащие определения сущностей, характерные для общего продукта, процесса или специализации ресурсов, используемых в нескольких дисциплинах. Эти определения обычно используются для междоменного обмена и совместного использования информации о конструкции;

**Доменный уровень** — самый высокий уровень включает схемы, содержащие определения сущностей, которые являются специализациями продуктов, процессов или ресурсов, характерных для определенной дисциплины. Эти определения обычно используются для внутридоменного обмена и совместного использования информации.

## Использованная литература ##

* [Основные отраслевые классы — по Википедии] (https://en.wikipedia.org/wiki/Industry_Foundation_Classes)
