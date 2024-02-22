{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Файл SDF – файл формату просторових даних",
  "description":"Дізнайтеся про формат файлу SDF та API, які можуть створювати та відкривати файли SDF.",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "identifier":"gis-sdf-uk",
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## Що таке файл SDF?

A Spatial Data File (SDF) is a Geodatabase file format that was developed by Autodesk. It stores geospatial data and is used by Autodesk GIS program MapGuide and AutoCAD Map 3D. SDF file format is based on the single file database file format SQLite3. Він вважається оптимізованим форматом файлу для великих наборів даних просторової інформації.

Ви можете відкрити файл SDF за допомогою Autodesk AutoCAD Map 3D 2022 і Autodesk AutoCAD Civil 3D 2023.

## Формат файлу SDF - Додаткова інформація

Формат файлів SDF зберігається на диску як двійкові файли. Він заснований на базі даних SQLite, яка використовує компоненти зберігання низького рівня для двійкової серіалізації даних. Файл SDF містить кілька класів об’єктів на файл і кілька геометричних властивостей для кожного класу об’єктів. Дані у файлі SDF доступні з високою швидкістю завдяки індексуванню кожної властивості геометрії за допомогою R-дерева.

## Список літератури

* [Формат даних SDF](https://en.wikipedia.org/wiki/Spatial_Data_File)

* [Importing Autodesk SDF](http://docs.autodesk.com/CIV3D/2013/ENU/index.html?url=filesMAPC3D/GUID-EC7140D6-F14F-4F7B-B431-FF0BAD7AE86C.htm,topicNumber=MAPC3Dd30e43012)

