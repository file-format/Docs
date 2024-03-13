{
  "date": "2019-10-11",
  "keywords": [
"apkg",
"apkg faylı",
"apkg fayl formatı",
"apkg fayl növü",
"fayl",
"növü",
"APKG faylı nədir"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "APKG - Anki Flashcard Deck File Format",
  "description": "APKG faylı və onları yarada və aça bilən API-lərin nə olduğunu öyrənin.",
  "linktitle": "APKG",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-apk-azg"
}
},
  "lastmod": "2021-06-16"
}

## APKG faylı nədir?

.apkg uzantısı olan fayl fləşkarta əsaslanan öyrənmə proqramı olan [Anki](https://ankiweb.net/about) proqram proqramında istifadə edilmək üçün yaradılan yaddaş kartları göyərtəsidir. O, yüklənəcək və Anki proqramında nümayiş etdiriləcək [HTML](/web/html/) mətni ehtiva edir və əlavə olaraq vizual və səsli öyrənmə üçün şəkillər və səslərə malik ola bilər. Anki istifadəçilərə öz Anki flashcard göyərtələrini yaratmağa, eləcə də digər istifadəçinin flashcard göyərtələrini idxal etməyə imkan verir.

## APKG fayl formatı

Anki kart göyərtələri veb səhifələr yaratmaq üçün məşhur və ümumi dil olan HTML-də yazılmış şablonlardan yaradılmışdır. Göyərtə kartlarının üslubu veb səhifələrin üslubu üçün istifadə olunan dil olan CSS istifadə edərək həyata keçirilir. Üslub aşağıdakı dəyişiklikləri əhatə edir:

 * font-family - Kartda istifadə olunacaq şriftin adı.
 * font-size - Şriftin piksellərlə ölçüsü.
 * text-align - Mətnin mərkəzə, sola və ya sağa düzülməsini müəyyən edir.
 * rəng - mavi, qırmızı və s. kimi sadə rəng adları və ya HTML rəng kodları ola bilən mətnin rəngini müəyyən edir.
 * background-color - Kartın fon rəngini müəyyən edir

Üslub məlumatı bütün kartlar arasında paylaşılır və dəyişiklik edildikdə bütün kartlara təsir göstərir. Aşağıdakı nümunə, birincidən başqa bütün kartlarda sarı fondan istifadə edəcək:

```CSS
.card {
  background-color: yellow;
}
.card1 {
  background-color: blue;
}
```

Anki kartında ölçüləri dəyişdirilən şəkillər aşağıdakı kimi idarə oluna bilər.

```CS
img {
  max-width: none;
  max-height: none;
}
```

## Javascript-in Anki kartlarına yerləşdirilməsi

Kart şablonlarından istifadə etməklə [Javascript](/web/js/)-ni Anki kartına yerləşdirmək mümkündür. Lakin Javascript-in qabaqcıl səviyyəsinə görə onun dəstəyi təmin edilmir. Üstəlik, render cihazları kartda Javascript-in tətbiq təsirlərini fərqli göstərə bilər ki, bu da tətbiqin bütün cihazlarda sınaqdan keçirilməsinə ehtiyac yaradır. Windows.alert kimi bəzi Javascript xüsusiyyətləri, yazdığınız Javascript kodunu sazlamağı çətinləşdirir.

## İstinadlar ##

* [Anki Documentation](https://docs.ankiweb.net/intro.html)

