{
  "date" : "2019-10-11",
  "keywords" :[ "файл png", "формат файла png", "что такое файл png", "файл", "пример png", "расширение файла png", "расширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файла PNG - файл растрового изображения",
  "description":"Узнайте о формате файлов PNG и API, которые могут создавать и открывать файлы PNG.",
  "linktitle" : "PNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Что такое PNG-файл?

Файл **PNG** (Portable Network Graphics) — это формат файла растрового изображения, в котором используется сжатие без потерь. Этот формат файла был создан в качестве замены формата обмена графикой ([GIF](/ru/image/gif/)) и не имеет ограничений авторского права. Однако формат файла PNG не поддерживает анимацию. Формат файлов PNG поддерживает сжатие изображений без потерь, что делает его популярным среди пользователей. С течением времени PNG превратился в один из широко используемых форматов файлов изображений.

## Краткая история формата файлов PNG

Основной причиной создания формата файла PNG был запатентованный алгоритм сжатия Lempel-Ziv-Welch, используемый в формате файла GIF. Это, наряду с другими ограничениями GIF, привело к необходимости замены формата файла [**GIF**](/ru/image/gif/). Первое предложение и название для формата файлов PNG поступило в январе 1995 года. Основные события, связанные с форматами файлов PNG, перечислены ниже:

* Октябрь 1996: Спецификации PNG версии 1.0 были выпущены и позже появились как [RFC] (https://en.wikipedia.org/wiki/Request_for_Comments) 2083. В октябре 1996 года они стали рекомендацией W3C.
* Декабрь 1998: Выпущена версия 1.1 с небольшими изменениями и добавлением трех новых частей.
* Август 1999: Выпущена версия 1.2, добавляющая один дополнительный фрагмент.
* Ноябрь 2003 г.: PNG стал международным стандартом (ISO/IEC 15948:2003). Эта версия PNG лишь незначительно отличается от версии 1.2 и не добавляет новых фрагментов.
* Март 2004 г.: ИСО/МЭК 15948:2004.

## Функциональное сравнение GIF и PNG

Формат файла PNG был разработан, чтобы быть простым и портативным, юридически свободным, взаимозаменяемым, гибким и надежным. В следующей таблице перечислены функции GIF, унаследованные форматом файла PNG, в дополнение к новым функциям.

|Функция|GIF|PNG|
---|---|---|
|Индексные изображения до 256 цветов|Да|Да|
|Поддержка потоковой передачи|Да|Да|
|Прозрачность|Да|Да|
|Дополнительная информация|Да|Да|
|Независимость от оборудования и платформы|Да|Да|
|Действует|Да|Да|
|Truecolor изображения до 48 бит на пиксель|Нет|Да|
|Изображения в оттенках серого до 16 бит на пиксель|Нет|Да|
|Полный альфа-канал (общие маски прозрачности)|Нет|Да|
|Информация о гамме изображения|Нет|Да|
|Надежность|Нет|Да|
|Быстрая начальная презентация|Нет|Да|

## Структура файла PNG

Почти все операционные системы поддерживают открытие файлов PNG. Например, средство просмотра Microsoft Windows имеет возможность открывать файлы PNG, поскольку ОС по умолчанию поддерживает эту поддержку, доступную как часть установки. Файл PNG состоит из «подписи» PNG, за которой следует серия //фрагментов//.

### Заголовок файла PNG

Первые восемь байтов файла PNG всегда содержат следующие (десятичные) значения:

{{{137 80 78 71 13 10 26 10 }}}

Эта сигнатура указывает, что оставшаяся часть файла содержит одно изображение PNG, состоящее из серии фрагментов, начиная с фрагмента IHDR и заканчивая фрагментом IEND.

### Кусочки ###

Каждый чанк состоит из четырех частей:

**Длина:** 4-байтовое целое число без знака, указывающее количество байтов в поле данных фрагмента. Длина учитывает только поле данных, а не само поле, код типа блока или CRC. Нуль является допустимой длиной. Хотя кодировщики и декодеры должны рассматривать длину как беззнаковую, ее значение не должно превышать 231 байт.

**Тип фрагмента:** 4-байтовый код типа фрагмента. Для удобства описания и изучения файлов PNG коды типов могут состоять только из прописных и строчных букв ASCII (AZ и az или 65–90 и 97–122 в десятичном формате). Однако кодировщики и декодеры должны обрабатывать коды как фиксированные двоичные значения, а не строки символов. Например, было бы неправильно представлять код типа IDAT эквивалентами этих букв в формате EBCDIC. Дополнительные соглашения об именах для типов фрагментов обсуждаются в следующем разделе.

**Данные фрагмента:** Байты данных, соответствующие типу фрагмента, если таковые имеются. Это поле может иметь нулевую длину.

**CRC:** 4-байтовый CRC (проверка циклическим избыточным кодом), рассчитанный для предыдущих байтов в блоке, включая код типа блока и поля данных блока, но не включая поле длины. CRC присутствует всегда, даже для фрагментов, не содержащих данных.

Длина данных чанка может быть любым числом байтов вплоть до максимального; поэтому разработчики не могут предполагать, что фрагменты выровнены по любым границам, превышающим байты.

Фрагменты могут появляться в любом порядке с учетом ограничений, наложенных на каждый тип фрагментов. (Одним заметным ограничением является то, что IHDR должен стоять первым, а IEND должен стоять последним; таким образом, фрагмент IEND служит маркером конца файла.) Могут появляться несколько фрагментов одного и того же типа, но только если это специально разрешено для этого типа.

#### Типы чанков

Типы фрагментов подразделяются на **Критические** и **Вспомогательные** на основе 4-байтового значения ASCII с учетом регистра, присвоенного Типу фрагмента. Все реализации должны понимать и успешно отображать стандартные критические фрагменты. Допустимое изображение PNG должно содержать фрагмент IHDR, один или несколько фрагментов IDAT и фрагмент IEND.

### Сжатие

Метод сжатия PNG 0 (единственный метод сжатия, определенный в настоящее время для PNG) задает сжатие deflate/inflate со скользящим окном размером не более 32768 байт. Сжатие Deflate — это производная LZ77, используемая в zip, gzip, pkzip и связанных с ними программах. Были проведены обширные исследования, подтверждающие его безпатентный статус. Сжатые данные в потоке данных zlib хранятся в виде серии блоков, каждый из которых может представлять необработанные (несжатые) данные, данные, сжатые с помощью LZ77, закодированные с помощью фиксированных кодов Хаффмана, или данные, сжатые с помощью LZ77, закодированные с помощью пользовательских кодов Хаффмана. Бит маркера в последнем блоке идентифицирует его как последний блок, позволяя декодеру распознать конец сжатого потока данных.

#### Фильтрация перед сжатием

Фильтры предварительного сжатия применяются для подготовки данных изображения к оптимальному сжатию. Метод фильтра PNG определяет пять основных типов фильтров:

|Тип фильтра|Имя|Прогнозируемое значение|
---|---|---|
|0|Нет|Сканерлайн передается без изменений|
|1|Sub|Передает разницу между каждым байтом и значением соответствующего байта предыдущего пикселя.|
|2|Up|Фильтр Up() аналогичен фильтру Sub(), за исключением того, что в качестве предиктора используется пиксель непосредственно над текущим пикселем, а не слева от него.|
|3|Среднее|Фильтр Average() использует среднее значение двух соседних пикселей (слева и сверху) для прогнозирования значения пикселя.|
|4|Paeth|Фильтр Paeth() вычисляет простую линейную функцию трех соседних пикселей (слева, вверху, вверху слева), затем выбирает в качестве предиктора соседний пиксель, ближайший к вычисляемому значению.|

Алгоритмы фильтрации применяются к «байтам», а не к пикселям, независимо от битовой глубины или типа цвета изображения. Алгоритмы фильтрации работают с последовательностью байтов, сформированной строкой сканирования. Если изображение включает альфа-канал, альфа-данные фильтруются так же, как данные изображения.

Когда изображение чересстрочное, каждый проход шаблона чересстрочной развертки обрабатывается как независимое изображение для целей фильтрации. Фильтры работают с последовательностями байтов, образованными пикселями, фактически переданными во время прохода, а «предыдущая строка сканирования» — это та, которая ранее была передана в том же проходе, а не соседняя в полном изображении. Обратите внимание, что частичное изображение, передаваемое за один проход, всегда прямоугольное, но имеет меньшую ширину и/или высоту, чем полное изображение. Фильтрация не применяется, когда это фрагмент изображения пуст.

## Использованная литература ##

* [PNG — домашняя страница] (http://www.libpng.org/pub/png/)
