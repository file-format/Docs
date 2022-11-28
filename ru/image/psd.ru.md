{
  "date" : "2019-10-11",
  "keywords" :[ "файл psd", "формат файла psd", "что такое файл psd", "файл", "пример psd", "расширение файла psd", "расширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSD — формат файла изображения Photoshop",
  "description":"Узнайте о формате файла PSD и API, которые могут создавать и открывать файлы PSD.",
  "linktitle" : "PSD",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## .PSD вариант №

PSD, документ Photoshop, представляет собой собственный формат файлов Adobe Photoshop, используемый для графического дизайна и разработки. Файлы PSD могут включать в себя слои изображений, корректирующие слои, маски слоев, аннотации, информацию о файле, ключевые слова и другие элементы, характерные для Photoshop. Файлы Photoshop по умолчанию имеют расширение .PSD, максимальную высоту и ширину 30 000 пикселей и ограничение по длине в два гигабайта.

## Спецификации формата файла PSD ##

Данные в PSD-файле хранятся в порядке байтов с обратным порядком байтов. Это подразумевает замену коротких и длинных целых чисел при чтении или записи на платформе Windows. Формат файла Photoshop разделен на пять основных частей. Он имеет множество маркеров длины, которые можно использовать для перехода от одного раздела к другому. Маркеры длины обычно дополняются байтами для округления до ближайшего интервала в 2 или 4 байта. Пять основных частей:

* Заголовок файла
* Данные цветового режима
* Ресурсы изображений
* Информация о слое и маске
* Данные изображения

Для соответствия данные должны быть записаны во все эти поля в разделе, так как Photoshop может попытаться прочитать весь раздел. Это также означает, что при записи в файл в пропущенные поля записываются нули. Поле длины в разделах с разделителями по длине следует использовать для принятия решения о прекращении чтения. В большинстве случаев поле длины указывает количество следующих байтов, а не записей. При чтении файла необходимо помнить следующие моменты.

* Значения в столбце «Длина» во всех таблицах указаны в байтах.
* Все значения, определенные как строка Unicode, состоят из:
* Поле длины 4 байта, представляющее количество символов в строке (не байтов).
* Строка значений Unicode, два байта на символ.

### Заголовок файла ###

Заголовок файла содержит основные свойства изображения.

|Длина|Описание
---|---|
|4|Подпись: всегда равна '8BPS' . Не пытайтесь прочитать файл, если подпись не соответствует этому значению.
|2|Версия: всегда равна 1. Не пытайтесь прочитать файл, если версия не соответствует этому значению. (~*~*PSB~*~* версия 2.)
|6|Зарезервировано: должно быть равно нулю.
|2|Количество каналов в изображении, включая любые альфа-каналы. Поддерживаемый диапазон: от 1 до 56.
|4|Высота изображения в пикселях. Поддерживаемый диапазон: от 1 до 30 000.
|4|Ширина изображения в пикселях. Поддерживаемый диапазон: от 1 до 30 000.
|2|Глубина: количество бит на канал. Поддерживаемые значения: 1, 8, 16 и 32.
|2|Цветовой режим файла. Поддерживаемые значения: Bitmap # 0; Оттенки серого № 1; Индекс № 2; РГБ №3; CMYK#4; Многоканальный №7; Дуотон №8; Лаборатория № 9.

### Раздел данных цветового режима ###

Раздел данных цветового режима структурирован следующим образом:


|Длина|Описание
---|---|
|4|Длина следующих цветовых данных
|переменная|Данные цвета

Данные цветового режима доступны только для индексированного цвета и дуплекса, как определено полем режима в разделе «Заголовок файла». Для всех остальных режимов этот раздел представлен 4-байтовыми обнуленными значениями. Для индексированных цветных изображений длина составляет 768, а данные о цвете содержат таблицу цветов для изображения в порядке без чередования. Для изображений Duotone данные о цвете содержат спецификацию Duotone (формат которой не задокументирован). Другие приложения, которые читают файлы Photoshop, могут обрабатывать двухцветное изображение как серое и просто сохранять содержимое двухцветной информации при чтении и записи файла.

### Раздел ресурсов изображений ###

Третий раздел файла содержит ресурсы изображений. Он начинается с поля длины, за которым следует серия блоков ресурсов.


|Длина|Описание
---|---|
|4|Длина раздела ресурса изображения. Длина может быть нулевой.
|Переменная|Ресурсы изображения (блоки ресурсов изображения)

Ресурсы изображений используются для хранения непиксельных данных, связанных с изображениями, таких как траектории инструментов пера. Их называют блоками ресурсов, поскольку они содержат данные, хранившиеся в ресурсах Macintosh в ранних версиях Photoshop. Базовая структура блоков ресурсов изображений показана ниже:


|Длина|Описание
---|---|
|4|Подпись: '8BIM'
|2|Уникальный идентификатор ресурса. Идентификаторы ресурсов изображений содержат список идентификаторов ресурсов, используемых Photoshop.
|Переменная|Имя: строка Паскаля, дополненная для четного размера (нулевое имя состоит из двух байтов, равных 0).
|4|Фактический размер данных ресурсов, которые следуют
|Переменная|Данные ресурса, описанные в разделах, посвященных отдельным типам ресурсов. Он дополнен, чтобы сделать размер даже.

Ресурсы изображений используют несколько стандартных идентификационных номеров.

### Информация о слое и маске ###

Четвертый раздел файла Photoshop содержит информацию о слоях и масках, такую как количество слоев, каналы в слоях, диапазоны наложения, ключи корректирующего слоя, слои эффектов и параметры маски. Если нет слоев или масок, этот раздел представлен обнуленным 4-байтовым полем. Особое внимание следует уделить длине разделов при чтении этого раздела из-за обнуления значений. Расположение разделов «Слой и маска» следующее:


|Длина|Описание
---|---|
|4|Длина раздела информации о слое и маске. (Длина PSB составляет 8 байт.)
|Переменная|Информация о слое
|Переменная|Информация о глобальной маске слоя
|Переменная|Серии тегированных блоков, содержащих различные типы данных.

#### Информация о слое ####

В следующей таблице показана высокоуровневая организация информации слоя.


|Длина|Описание
---|---|
|4|Длина секции информации о слоях, округленная до кратного 2. (Длина PSB 8 байт.)
|2|Количество слоев. Если это отрицательное число, его абсолютное значение равно количеству слоев, а первый альфа-канал содержит данные о прозрачности для объединенного результата.
|Переменная|Информация о каждом слое. См. Записи слоя описывает структуру этой информации для каждого слоя.
|Переменная|Данные изображения канала. Содержит одну или несколько записей данных изображения для каждого слоя. Слои расположены в том же порядке, что и в информации о слоях.

### Данные изображения ###

Пиксельные данные изображения содержатся в разделе файла Image Data. Данные в разделе данных изображения расположены в плоском порядке, т. е. сначала все данные красного цвета, затем все данные зеленого цвета и т. д. Каждая плоскость хранится в порядке строк развертки, без дополнительных байтов. Раздел данных изображения расположен в формате как показано в следующей таблице.

|Длина|Описание
---|---|
|2|Метод сжатия: *0 = Необработанные данные изображения * 1 = Сжатые RLE данные изображения начинаются с подсчета байтов для всех строк сканирования (строк * каналов), при этом каждый подсчет сохраняется как двухбайтовое значение. Далее следуют сжатые данные RLE, причем каждая строка сканирования сжимается отдельно. Сжатие RLE — это тот же алгоритм сжатия, который используется подпрограммой Macintosh ROM PackBits и стандартом TIFF. *2 = ZIP без предсказания *3 = ZIP с предсказанием.
|Переменная|Данные изображения. Планарный порядок = RRR GGG BBB и т. д.

## Использованная литература ##

* [Спецификации формата файлов PSD — Adobe] (https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/#50577409_pgfId-1030196)
* [Формат файла Adobe Photoshop] (https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)
