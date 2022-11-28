{
  "date" : "2019-12-12",
  "keywords" :["JT", "файл", "расширение", "формат", "3D fbx", "" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Узнайте о формате файлов JT и API, которые могут создавать и открывать файлы JT.",
  "title" :"JT - формат файла тесселяции Юпитера",
  "linktitle" : "JT",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## .JT вариант №

**JT** (Jupiter Tessellation) — это эффективный, отраслевой и гибкий формат 3D-данных, соответствующий стандарту ISO, разработанный Siemens PLM Software. Механические области САПР аэрокосмической, автомобильной промышленности и тяжелого оборудования используют JT в качестве наиболее ведущего формата 3D-визуализации.

Формат JT — это граф сцены, который поддерживает атрибуты и узлы, специфичные для САПР. Для хранения данных фасетов (треугольников) используются сложные методы сжатия. Этот формат структурирован для поддержки визуальных атрибутов, информации о продукте и производстве (PMI) и метаданных. Есть хорошая поддержка асинхронной потоковой передачи контента. В тяжелой механической промышленности профессионалы используют файл JT в своих решениях САПР и программах управления жизненным циклом продукта (PLM) для изучения геометрии сложных товаров.

Поскольку JT поддерживает почти все важные форматы 3D CAD, его сборка может работать с различными комбинациями, известными как «мульти-CAD». Эта мульти-CAD-сборка всегда хорошо управляется и актуальна, потому что синхронизация файлов описания продуктов CAD с соответствующими JT-файлами происходит автоматически. Файлы JT изначально легкие, поэтому считаются подходящими для совместной работы в Интернете. Компании Совместная работа посредством отправки 3D-визуализации через носитель намного проще по сравнению с «тяжелыми» оригинальными файлами САПР. Кроме того, файлы JT обеспечивают множество функций безопасности, которые делают обмен интеллектуальной собственностью более безопасным.

## Краткая история формата файла JT

Engineering Animation, Inc. и Hewlett Packard были первоначальными разработчиками JT, которые разработали этот формат как инструментарий Direct Model. После того, как EAI была приобретена UGS Corp., JT стала частью пакета UGS. В начале 2007 года UGS объявила JT своим основным форматом 3D. В том же году Siemens AG приобрела UGS и стала Siemens PLM Software. Siemens использует JT в качестве общего формата взаимодействия и формата архивирования данных. В 2009 году ISO приняла спецификацию JT для публикации в качестве общедоступной спецификации ISO (PAS). В середине 2010 года ProSTEP iViP объявила, что на промышленном уровне JT и STEP AP 242 XML могут использоваться вместе для достижения максимального преимущества в данных. сценарии обмена. В 2012 году JT был официально объявлен стандартизированным по ISO (ISO 14306:2012 (ISO JT V1)) форматом 3D-визуализации.

## Формат файла JT ##

Все объекты в формате JT представлены через идентификатор объекта, а ссылки между объектами обрабатываются через идентификатор объекта, на который делается ссылка. Целостность этих ссылок на объекты может поддерживаться за счет развертки/перестановки указателей.

Файл JT организован в виде серии блоков, а блок заголовка всегда является первым блоком данных в файле. Сразу за блоком заголовка следует ряд сегментов данных и сегмент TOC. Один сегмент данных (сегмент 6 LSG) всегда содержит JT-файл, совместимый со ссылкой. Сегмент TOC содержит информацию о расположении всех других сегментов данных этого файла.

{{< figure src="../JT-1.png" alt="JT Формат файла" >}}

### Заголовок файла ###

Заголовок файла — это первый блок в иерархии данных файла JT. Информация о версиях и информация о расположении оглавления заключены в заголовок, что облегчает загрузчикам чтение файла. Содержимое заголовка файла устроено следующим образом.

### Сегмент оглавления ###

Сегмент TOC должен существовать в файле и содержать информацию об идентификации и расположении всех других сегментов данных. Фактическое местоположение сегмента TOC определяется полем смещения TOC в заголовке файла. Каждый отдельно адресуемый сегмент данных представлен записью TOC в сегменте TOC.

### Сегмент данных ###

Файл JT определяет все сохраненные данные в сегменте данных. Некоторый сегмент данных может сжимать все байты данных информации, оставшиеся в сегменте. Сегменты данных имеют следующую структуру:

![alt text](../JT-2.png "JT Data Segment")

В следующей таблице описаны различные типы сегментов данных:

|Имя|Описание
---|---|
| Сегмент LSG | Содержит набор объектов, связанных направленными ссылками для формирования LSG (структура ориентированного ациклического графа).
| Сегмент детализации формы | содержит определяющие данные для геометрических фигур (например, вершины, нормали, многоугольники и т. д.)
|JT B-Rep Segment|Наличие элемента данных для представления точной геометрической границы отдельной части в формате JT B-Rep.
|XT B-Rep сегмент|Наличие элемента данных для представления точной геометрической границы отдельной части в формате представления границы
|Сегмент каркаса|Данные представляют собой точный трехмерный каркас для конкретной части, определяемой элементом, содержащимся в этом сегменте.
|Сегмент метаданных|Позволяет хранить метаданные в отдельных адресуемых сегментах.
| Сегмент JT ULP | Наличие элемента данных для представления полуточной геометрической границы отдельной части в формате JT ULP.
|JT Сегмент LWPA|Содержит элемент, определяющий аналитические данные для конкретной детали. LWPA заключает коллекцию аналитических поверхностей в определение детали b-rep.

## Сжатие ##

Требования к передаче и хранению 3D-моделей более строгие, поэтому файлы JT могут использовать преимущества сжатия. Модель данных JT может состоять из разных файлов с использованием разных методов сжатия, но процесс сжатия прозрачен для пользователя данных JT.

На данный момент JT Open Toolkit (в качестве стандарта) и расширенное сжатие являются двумя методами сжатия, используемыми файлами JT. JT Open Toolkit использует простой алгоритм сжатия без потерь, в то время как расширенное сжатие использует более совершенный метод сжатия, специфичный для предметной области, что приводит к сжатию геометрии с потерями. Клиентские приложения предпочитают расширенное сжатие, а не стандартное сжатие, поскольку расширенное сжатие дает довольно высокие коэффициенты сжатия. Обратная совместимость с обычными приложениями для просмотра файлов JT поддерживается за счет предоставления стандартного сжатия. Форма сжатия должна быть совместима с версией формата файла JT, которую можно увидеть, когда файл JT открывается с помощью текстового редактора и заключен в информацию заголовка ASCII.

## Использованная литература ##

* [Справочник по формату файла JT] (https://www.plm.automation.siemens.com/en_us/Images/JT-v10-file-format-reference-rev-B_tcm1023-233786.pdf)
* [JT (формат визуализации)](https://en.wikipedia.org/wiki/JT_(формат_визуализации)#Модель_данных)
