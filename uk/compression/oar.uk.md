{
  "date" : "2021-04-08",
  "keywords" :[ "файл oar", "формат файлу oar", "що таке файл oar", "файл", "приклад oar", "розширення файлу oar", "розширення", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAR - формат файлу архіву OpenSimulator",
  "description":"Дізнайтеся про формат файлу OAR та API, які можуть створювати та відкривати файли OAR.",
  "linktitle" : "OAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-15"
}

## Що таке файл OAR?

Файл із розширенням .oar — це архівний файл, який використовується програмою OpenSimulator, яка є сервером тривимірних програм із відкритим вихідним кодом для створення віртуального середовища, доступного багатьом користувачам через мережу. Формат файлу OAR надає необхідні дані про активи, необхідні для повного завантаження рельєфу, текстур об’єктів та інвентарю в іншій системі. OpenSimulator також має додаткову гіперсітку, яка дозволяє користувачам відвідувати інші інсталяції OpenSimulator в Інтернеті. Файли OAR мають тип Internet MIME application/oar і містять один або кілька заархівованих файлів.


## Формат файлу OAR

OAR — це двійкові файли, які зберігаються у форматі стисненого архіву. Останньою версією формату файлів OAR є [версія 1.0](http://opensimulator.org/wiki/OAR_Format_1.0), яка має значні зміни порівняно з попередньою [версією 0.8](http://opensimulator.org/wiki/OAR_Format_0). .8). Остання версія підтримує зберігання кількох регіонів в одному OAR і не сумісна з версіями OpenSimulator до 0.7.5. Файл OAR — це файл tar, стиснутий у форматі gzip (tar.gz) в оригінальному форматі tar для Unix (не USTAR).

## Приклад регіонів OAR
Файли AOR можуть містити кілька регіонів. Структура архіву така (у цьому прикладі 4 регіони):

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
## OAR Archive.xml

Керуючий файл архіву містить основний номер версії для визначення сумісності з майбутніми змінами формату. Наявність ресурсів у форматі OAR позначається логічним елементом<assets_included> . Інформація про включені регіони міститься в маніфесті, який присутній у контрольному файлі. Нижче наведено приклад Archive.xml.

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

## Список літератури

* [Формат OAR v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
* [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

