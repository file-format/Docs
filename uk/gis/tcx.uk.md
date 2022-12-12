{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файлу TCX - XML-файл навчального центру",
  "description":"Дізнайтеся про формат файлу TCX та API, які можуть створювати та відкривати файли TCX.",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Що таке файл TCX?

Файл TCX (Training Center XML) — це формат обміну даними, який використовується для обміну даними між фітнес-пристроями. Він був представлений у 2008 році з продуктом Garmin Training Center. Дані про тренування, такі як частота пульсу, частота бігу, велосипеда, калорії та час кола, зберігаються у форматі [XML](/uk/web/xml/) у файлі TCX. Крім того, підсумкові дані про трек тренування також включені у файл TCX. Файли TCX схожі на файли [FIT](/uk/gis/fit/), створені за допомогою спортивних пристроїв Garmin.

## Формат файлу TCX - Додаткова інформація

Файли TCX зберігаються на диску як XML-файли, кожен запис зберігається як дія. Діяльність містить усі дані тренування, такі як час, час кола, ідентифікатор, частота серцевих скорочень, інтенсивність, частота педалей та інформація про трек, яка містить пари позицій разом із міткою часу для цієї позиції по ширині та довжині, подібно до [GPX] (/uk/gis/gpx/) файлів.

### Версії формату файлу TCX

Існує дві версії цього формату з власними XML-схемами, розміщеними в Garmin. Ось кілька з них:

* https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
* https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
* https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## Протокол даних TCX

Швидка версія формату TCX XML доступна на Github як [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol).

## Посилання ##

* [Training Center XML](https://en.wikipedia.org/wiki/Training_Center_XML)
* [TCX Viewer](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)

