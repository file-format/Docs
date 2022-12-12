{
  "date" : "2019-12-12",
  "keywords" :[ "JT", "файл", "разширение", "формат", "3D fbx", "" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Научете за JT файловия формат и API, които могат да създават и отварят JT файлове.",
  "title" :"JT – файлов формат за теселация на Юпитер",
  "linktitle" : "JT",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Какво е JT файл?

**JT** (Jupiter Tessellation) е ефективен, фокусиран върху индустрията и гъвкав ISO-стандартизиран 3D формат на данни, разработен от Siemens PLM Software. Механичните CAD области на аерокосмическата, автомобилната индустрия и тежкото оборудване използват JT като техен най-водещ формат за 3D визуализация.

JT форматът е графика на сцена, която поддържа атрибутите и възлите, които са специфични за CAD. Използват се сложни техники за компресиране за съхраняване на фасетни данни (триъгълници). Този формат е структуриран да поддържа визуални атрибути, информация за продукта и производството (PMI) и метаданни. Има добра поддръжка за асинхронно поточно предаване на съдържание. В тежката механична индустрия професионалистите използват JT файл в своите CAD решения и софтуерни програми за управление на жизнения цикъл на продукта (PLM), за да изследват геометрията на сложни стоки.

Тъй като JT поддържа почти всички важни 3D CAD формати, неговото сглобяване може да се справи с различни комбинации, които са известни като "multi-CAD". Този мулти-CAD модул винаги е добре управляван и актуален, тъй като синхронизирането между собствените CAD файлове с описание на продукта с техните свързани JT файлове се извършва автоматично. JT файловете първоначално са леки, така че се считат за подходящи за интернет сътрудничество. Компаниите си сътрудничат чрез изпращане на 3D визуализации през медиите много по-лесно в сравнение с „тежките“ оригинални CAD файлове. Освен това JT файловете осигуряват много функции за сигурност, които правят споделянето на интелектуална собственост по-сигурно.

## Кратка история на файловия формат JT

Engineering Animation, Inc. и Hewlett Packard бяха първоначалните дизайнери на JT, които разработиха този формат като инструментариум Direct Model. След като EAI беше придобит от UGS Corp. JT стана част от пакета на UGS. В началото на 2007 г. UGS обяви JT като техен главен 3D формат. През същата година Siemens AG купува UGS и се оказва Siemens PLM Software. Siemens използва JT като общ формат за оперативна съвместимост и формат за архивиране на данни. През 2009 г. ISO прие JT спецификацията за публикуване като ISO публично достъпна спецификация (PAS). В средата на 2010 г. ProSTEP iViP обяви, че на индустриално ниво JT и STEP AP 242 XML могат да се използват заедно за постигане на максимално предимство в данните обмен на сценарии. През 2012 г. JT беше официално деклариран като стандартизиран по ISO (ISO 14306:2012 (ISO JT V1)) формат за 3D визуализация.

## JT файлов формат ##

Всички обекти във формата JT са представени чрез идентификатор на обект и препратките между обектите се обработват чрез идентификатора на реферирания обект. Целостта на тези препратки към обекти може да се поддържа чрез премахване/преместване на указатели.

JT файлът е подреден като поредица от блокове и блокът Header винаги е първият блок от данни във файла. Поредица от сегменти с данни и сегмент TOC следват непосредствено блока на заглавката. Единият сегмент от данни (6 LSG сегмент) притежава референтен съвместим JT файл, който винаги съществува. TOC сегментът съдържа информацията за местоположението на всички други сегменти от данни на този файл.

{{< figure src="../JT-1.png" alt="JT файлов формат" >}}

### Заглавка на файл ###

Заглавката на файла е първият блок в йерархията на данните на JT файла. Информацията за версията и информацията за местоположението на TOC са включени в заглавката, което улеснява зареждащите устройства при четене на файлове. Съдържанието на заглавката на файла е подредено по следния начин.

### TOC сегмент ###

Сегментът TOC трябва да съществува във файл и да съдържа информация за идентификация и местоположение на всички други сегменти от данни. Действителното местоположение на TOC сегмента се определя от полето TOC Offset на заглавката на файла. Всеки индивидуално адресируем сегмент от данни е представен от TOC запис в TOC сегмент.

### Сегмент от данни ###

JT файлът дефинира всички съхранени данни в рамките на сегмент от данни. Някои сегменти от данни могат да компресират всички байтове данни с информация, останали в сегмента. Сегментите от данни имат следната структура:

![alt text](../JT-2.png "JT Data Segment")

Следващата таблица описва различни типове сегменти от данни:

|Име|Описание
---|---|
|LSG сегмент|Съдържа колекция от обекти, свързани чрез насочени препратки, за да образуват LSG (насочена ациклична графична структура)
|Shape LOD segment|съдържа дефиниращите данни за геометричните фигури (напр. върхове, нормали, полигони и т.н.)
|JT B-Rep сегмент|Имам елемент за данните за представяне на точната геометрична граница за отделна част във формат JT B-Rep.
|XT B-Rep segment|Имам елемент за данните за представяне на точната геометрична граница за отделна част във формат за представяне на граници
|Сегмент на телена рамка|Данните представляват прецизна 3D телена рамка за определена част, дефинирана от елемент, съдържащ се в този сегмент.
|Сегмент с метаданни|Позволява да се съхраняват метаданни в отделни адресируеми сегменти.
|JT ULP сегмент|Имам елемент за данните за представяне на полупрецизната геометрична граница за отделна част във формат JT ULP.
|JT LWPA сегмент|Съдържа елемент, дефиниращ аналитични данни за определена част. LWPA обхваща колекцията от аналитични повърхности в дефиницията на b-rep на детайла.

## Компресия ##

Изискванията за предаване и съхранение на 3D модели са по-взискателни, така че JT файловете могат да се възползват от компресията. Един JT модел на данни може да бъде съставен от различни файлове, използващи различни техники за компресиране, но процесът на компресиране е прозрачен за потребителя на JT данни.

Досега JT Open Toolkit (като стандарт) и разширеното компресиране са две техники за компресиране, използвани от JT файлове. JT Open Toolkit използва лесен алгоритъм за компресия без загуби, докато усъвършенстваната компресия използва по-усъвършенствана техника за компресиране, специфична за домейн, което води до геометрична компресия със загуби. Клиентските приложения предпочитат усъвършенствано компресиране, вместо да използват стандартно компресиране, тъй като усъвършенстваното компресиране дава доста високи съотношения на компресия. Обратната съвместимост с обикновените JT приложения за гледане на файлове се поддържа чрез предоставяне на стандартна компресия. Формата за компресиране трябва да е съвместима с версията на файловия формат JT, която може да се види, когато JT файл се отваря с помощта на текстов редактор и е затворен в информация за заглавката на ASCII.

## Препратки ##

* [Справка за JT файлов формат](https://www.plm.automation.siemens.com/en_us/Images/JT-v10-file-format-reference-rev-B_tcm1023-233786.pdf)
* [JT (формат за визуализация)](https://en.wikipedia.org/wiki/JT_(visualization_format)#Data_model)
