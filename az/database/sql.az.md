{
  "date": "2020-11-11",
  "keywords": [
"SQL",
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
  "description": "SQL faylları yarada və aça bilən SQL fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "SQL Fayl Format - Strukturlaşdırılmış Sorğu Dili Məlumat Faylı",
  "linktitle": "SQL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-sq-azl"
}
},
  "lastmod": "2020-11-11"
}

## SQL faylı nədir?

.sql uzantısı olan fayl, əlaqəli verilənlər bazaları ilə işləmək üçün kodu ehtiva edən Strukturlaşdırılmış Sorğu Dili (SQL) faylıdır. Verilənlər bazalarında CRUD (Yarat, Oxu, Yenilə və Sil) əməliyyatları üçün SQL ifadələrini yazmaq üçün istifadə olunur. SQL faylları həm masaüstü, həm də veb əsaslı verilənlər bazaları ilə işləyərkən geniş yayılmışdır. Java Persistence Query Language (JPQL), LINQ, HTSQL, 4D QL və digərləri kimi SQL-ə bir neçə alternativ var. SQL faylları Microsoft SQL Server, MySQL və Windows OS-də Notepad kimi digər sadə mətn redaktorlarının sorğu redaktorları tərəfindən açıla bilər.

## Qısa tarix

* 1970-ci illərin əvvəllərində IBM-də Donal D. Chamberlin və Raymond F. Boyce tərəfindən hazırlanmış və təqdim edilmişdir.

* IBM-in orijinal kvazi-relational verilənlər bazası idarəetmə sistemi olan System R-dən məlumatları saxlamaq və əldə etmək üçün istifadə olunur.

* Ticarət məhsulları bazasında müvafiq olaraq 1979, 1981 və 1983-cü illərdə kommersiya olaraq mövcud olan System/38, SQL/DS və DB2 daxil olmaqla System R prototipindən istifadə olunmağa başlandı.

* Rəsmi olaraq ANSI və ISO standart qrupları tərəfindən 1986-cı ilə qədər əlaqəli verilənlər bazası idarəetmə sistemləri (RDBMS) üçün standart "Database Language SQL" kimi qəbul edilmişdir.


## SQL fayl formatı

SQL faylları düz mətn formatındadır və bir neçə dil elementindən ibarət ola bilər. Bir SQL faylına birdən çox ifadələr əlavə edilə bilər, əgər onların icrası bir-birindən asılı olmadan mümkündür. Bu SQL əmrləri CRUD əməliyyatlarını yerinə yetirmək üçün sorğu redaktorları tərəfindən yerinə yetirilə bilər.

### SQL Dil elementləri

SQL dili elementləri aşağıda sadalandığı kimidir.

|Element|Təsvir|
---|---|
|bəndlər| Bəyanatların və sorğuların tərkib komponentləri.|
|İfadələr| Ya skalyar qiymətlər, ya da sütunlar və verilənlər sətirlərindən ibarət cədvəllər yarada bilər|
|Predikatlar| SQL üç dəyərli məntiq (3VL) (doğru/yanlış/naməlum) və ya Boolean həqiqət dəyərlərinə görə qiymətləndirilə bilən və ifadələrin və sorğuların təsirlərini məhdudlaşdırmaq və ya proqram axınını dəyişmək üçün istifadə olunan şərtləri müəyyənləşdirin.|
|Sorğular| Xüsusi meyarlar əsasında məlumatları əldə edin. Bu SQL-in mühüm elementidir.|
|Bəyanatlar| Sxemlərə və verilənlərə davamlı təsir göstərə bilər və ya əməliyyatlara, proqram axınına, bağlantılara, sessiyalara və ya diaqnostikaya nəzarət edə bilər.|

### SQL Nümunəsi
Aşağıdakı SQL ifadəsi **DATA** adlı cədvəl yaradır, ardınca bu cədvələ qeydlər daxil etmək üçün əlavə `INSERT` əmrləri.
```
CREATE TABLE DATA
(ID INTEGER REFERENCES STATION(ID),
MONTH INTEGER CHECK (MONTH BETWEEN 1 AND 12),
TEMP_F REAL CHECK (TEMP_F BETWEEN -80 AND 150),
RAIN_I REAL CHECK (RAIN_I BETWEEN 0 AND 100),
PRIMARY KEY (ID, MONTH));
```
```
INSERT INTO STATS VALUES (23, 1, 57.4, 0.31);
INSERT INTO STATS VALUES (21, 7, 91.7, 5.15);
INSERT INTO STATS VALUES (45, 1, 27.3, 0.18);
INSERT INTO STATS VALUES (65, 7, 74.8, 2.11);
INSERT INTO STATS VALUES (78, 1, 6.7, 2.10);
INSERT INTO STATS VALUES (88, 7, 65.8, 4.52);
```

## İstinadlar ##

* [SQL by Wikipedia](https://en.wikipedia.org/wiki/SQL)

* [SQL Sintaksisi](https://en.wikipedia.org/wiki/SQL_syntax)


