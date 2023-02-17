{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SP3 - файл NGS SP3",
  "description":"Дізнайтеся про формат файлу SP3 та API, які можуть створювати та відкривати файли SP3.",
  "linktitle" : "SP3",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## Що таке файл SP3?

Файл із розширенням .sp3 — це орбітальний формат Національної геодезичної служби (NGS) для зберігання орбітальної інформації. Це розширення форматів NGS SP1 і SP2 і містить інформацію про корекцію супутникового годинника, яка обчислюється одночасно з орбітами. Це в основному базується на позиції та годиннику, і не включає швидкості. Формат був запропонований Remondi в 1989 році та прийнятий у 1991 році. Окрім інформації про корекцію супутникового годинника, він містить таку інформацію, як показники точності орбіти, рядки коментарів, тиждень GPS і секунди тижня, пов’язані з першою епохою. Файли SP3 можна відкрити за допомогою Wolfram Research Mathematica.

## Формат файлу SP3 – Додаткова інформація

Файли SP3 зберігаються на диску у форматі ASCII, і його вміст можна відкрити в будь-якому текстовому редакторі для перегляду. Структуру файлу SP3 можна побачити на наступному зображенні.

{{< figure src="../sp3-file-format.png" title="" >}}

## Список літератури

* [Формат Extended Standard Product 3 Orbit (SP3-c)](http://epncb.oma.be/ftp/data/format/sp3c.txt#:~:text=The%20SP3%20format%20is%20similar ,%20більш%20гнучка%20заголовок%20структура)
* [Розширення стандартних форматів орбіти GPS Національної геодезичної служби] (https://beta.ngs.noaa.gov/PUBS_LIB/Extending_the_NGS_Standard_GPS_Orbit_Formats_TR_NOS133_NGS46.pdf)
