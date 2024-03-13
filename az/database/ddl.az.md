{
  "date": "2020-11-11",
  "keywords": [
"DDL",
"uzadılması",
"fayl",
"fayl formatı",
"Verilənlər bazası fayl növü",
"Verilənlər bazası fayl formatı",
"Verilənlər Bazasının Faylları"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "DDL faylları yarada və aça bilən DDL fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "DDL Fayl Format - Məlumat Tərifi Dil Faylı",
  "linktitle": "DDL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-dd-azl"
}
},
  "lastmod": "2020-11-11"
}

## DDL faylı nədir?

.ddl uzantısı olan fayl verilənlər bazası sxemini müəyyən etmək üçün istifadə edilən Məlumat Tərifi Dili faylıdır. O, cədvəllər, sütunlar, qeydlər və digər sahələr kimi verilənlər bazası strukturları ilə işləmək üçün ifadələr/əmrlər ehtiva edir. DDL faylındakı əmrlər [SQL](/database/sql/) dilində yazılmışdır və verilənlər bazasında cədvəl yaratmaq, buraxmaq və yeniləmək kimi əməliyyatları yerinə yetirə bilər. Verilənlər bazası sxemi onun yaratdığına məxsusdur və onun üzərində bütün CRUD əməliyyatları yerinə yetirilə bilər. DDL faylları yarada və aça bilən populyar proqramlar Windows Text Editor, Jetbrains Intellij Idea və EclipseLink-dir.

## DDL əmrləri

Tək DDL faylı düzgün sintaksis sayəsində ardıcıllıqla yerinə yetiriləcək və simvol dəstləri və cədvəllər yaratmaq, cədvəlləri silmək, cədvəllərin adının dəyişdirilməsi və dəyişdirilməsi kimi sxemə dəyişiklik edəcək bir neçə əmrdən ibarət ola bilər. Verilənlər bazası sxemi ilə işləyərkən aşağıdakı DDL əmrləri adətən istifadə olunur.

`CREATE` - Verilənlər bazasını və ya onun obyektlərini (məsələn, cədvəl, indeks, funksiya, görünüşlər, mağaza proseduru və tetikleyiciler) yaratmaq üçün istifadə olunur.

`DROP` – verilənlər bazasından obyektləri silmək üçün istifadə olunur.

`ALTER` - Verilənlər bazasının strukturunu dəyişmək üçün istifadə olunur.

`KESİL` – Cədvəldən bütün qeydləri silmək üçün istifadə olunur, o cümlədən qeydlər üçün ayrılmış bütün boşluqlar silinir.

`ŞƏRH` – Məlumat lüğətinə şərhlər əlavə edir.

`RENAME` – verilənlər bazasında mövcud obyektin adını dəyişir.

## DDL nümunəsi

Aşağıdakı nümunə cədvəl yaradan və onun sahələrini təyin edən CREATE əmri üçün DDL ifadəsini göstərir.

```
CREATE TABLE employees (
    id            INTEGER       PRIMARY KEY,
    first_name    VARCHAR(50)   not null,
    last_name     VARCHAR(75)   not null,
    fname         VARCHAR(50)   not null,
    dateofbirth   DATE          not null
);
```

## İstinadlar ##

* [DDL by Wikipedia](https://en.wikipedia.org/wiki/Data_definition_language)


