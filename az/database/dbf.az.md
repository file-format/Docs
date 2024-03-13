{
  "date": "2021-06-15",
  "keywords": [
"DBF",
"uzadılması",
"dbf faylı",
"dbf fayl formatı",
"Verilənlər bazası fayl növü",
"Verilənlər bazası fayl formatı",
"dbf faylı nədir",
"dBASE"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "DBF fayl formatı və DBF fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "DBF - dBase verilənlər bazası faylı",
  "linktitle": "DBF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-db-azf"
}
},
  "lastmod": "2021-06-15"
}

## DBF faylı nədir?
The file with .dbf extension is a database file used by a database management system application called **dBASE**. Inititally, the dBASE database was named as Project Vulcan; started by **Wayne Ratliff** in 1978. DBF fayl növü dBASE II ilə 1983-cü ildə təqdim edilmişdir. O, Array tipli sahələrlə çoxlu məlumat qeydlərini təşkil edir. **xBase** verilənlər bazası proqramı geniş çeşidli fayl formatları ilə uyğunluğuna görə populyardır; DBF fayllarını da dəstəkləyir.

## DBF fayl formatı
DBF fayl formatı dBASE verilənlər bazası idarəetmə sisteminə aiddir, lakin o, xBase və ya digər DBMS proqramları ilə uyğun ola bilər. dbf faylının ilkin versiyası ASCII simvol dəstindən istifadə etməklə məlumatların əlavə edilməsi, dəyişdirilməsi, silinməsi və ya çap edilməsi mümkün olan sadə cədvəldən ibarət idi. Zaman keçdikcə .dbf təkmilləşdirildi və verilənlər bazası sisteminin xüsusiyyətlərini və imkanlarını artırmaq üçün əlavə fayllar əlavə edildi.

Müasir dBASE-də DBF faylı başlıqdan, məlumat qeydlərindən və EOF (Faylın sonu) markerindən ibarətdir.

- Başlıq fayl haqqında məlumatı ehtiva edir, məsələn, qeydlərin sayı və qeydlərdə istifadə olunan sahə növlərinin sayı.
- Qeydlər faktiki məlumatları ehtiva edir.
- Faylın sonu 0x1A dəyəri ilə bir bayt ilə qeyd olunur.

### Fayl başlığı
dBase-də fayl başlığının düzülüşü aşağıdakı cədvəldə verilmişdir:

| Bayt | İçindəkilər | Məna |
---|---|---|
| 0 | 1 bayt | DOS faylı üçün etibarlı dBASE; 0-2 bitləri versiya nömrəsini, bit 3 DOS memo faylı üçün dBASE-nin mövcudluğunu, bit 4-6 SQL cədvəlinin mövcudluğunu, bit 7 hər hansı memo faylın (ya dBASE m PLUS və ya dBASE üçün) olduğunu göstərir. DOS) |
| 1–3 | 3 bayt | Son yeniləmə tarixi; YYMMDD | kimi formatlanmışdır
| 4–7 | 32 bitlik nömrə | Verilənlər bazası faylındakı qeydlərin sayı |
| 8–9 | 16 bitlik nömrə | Başlıqdakı baytların sayı |
| 10-11 | 16 bitlik nömrə | Qeyddəki baytların sayı |
| 12–13 | 2 bayt | Qorunur; 0 | ilə doldurun
| 14 | 1 bayt | Natamam əməliyyatı göstərən bayraq[qeyd 1] |
| 15 | 1 bayt | Şifrələmə bayrağı[qeyd 2] |
| 16–27 | 12 bayt | Çox istifadəçi mühitində DOS üçün dBASE üçün qorunur |
| 28 | 1 bayt | İstehsal .mdx fayl bayrağı; İstehsal .mdx faylı varsa 1, yoxdursa 0 |
| 29 | 1 bayt | Dil sürücüsü ID |
| 30–31 | 2 bayt | Qorunur; 0 | ilə doldurun
| 32–n [qeyd 3][qeyd 4] | Hər biri 32 bayt | sahə deskriptorları massivi (deskriptorların tərtibatı üçün aşağıya baxın) |
| n + 1 | 1 bayt | 0x0D sahə deskriptor massiv terminatoru kimi |

- ISMARKEDO funksiyası bu bayrağı yoxlayır (BAŞLAT TRANSACTION onu 1, SON TRANSACTION və ROLLBACK onu 0-a təyin edir).
- Bu bayraq 1-ə təyin edilərsə, Database encrypted mesajı görünür.
- Sahələrin maksimum sayı 255-dir.
- n sahə deskriptor massivindəki son baytı bildirir.

### Sahə təsviri massivi
dBASE-də sahə deskriptorlarının düzülüşü:

| Bayt | İçindəkilər | Məna |
---|---|---|
| 0–10 | 11 bayt | ASCII-də sahə adı (sıfırla doldurulmuş) |
| 11 | 1 bayt | Sahə növü. İcazə verilən dəyərlər: C, D, F, L, M və ya N (mənalar üçün növbəti cədvələ baxın) |
| 12–15 | 4 bayt | Qorunur |
| 16 | 1 bayt | Binar sistemdə sahə uzunluğu (maksimum 254 (0xFE)). |
| 17 | 1 bayt | İkilik sistemdə sahənin onluq sayı |
| 18–19 | 2 bayt | İş sahəsi ID |
| 20 | 1 bayt | Nümunə |
| 21-30 | 10 bayt | Qorunur |
| 31 | 1 bayt | İstehsal MDX sahə bayrağı; Sahənin istehsal MDX faylında indeks teqi varsa 1, yoxsa 0. |

### Verilənlər bazası qeydləri
Hər bir qeyd silinmə (1 bayt) bayrağı ilə başlayır. Sahələr sahə ayırıcıları olmadan qeydlərə bükülür. Bütün sahə məlumatları ASCII-dir. Sahənin növündən asılı olaraq, tətbiq əlavə məhdudiyyətlər qoyur. dBase-də sahə növləri bunlardır:

| Sahə növü | Mnemonik | Nə qəbul edir |
-------|-----|----|
| C | Xarakter | İstənilən ASCII mətni (sahənin uzunluğuna qədər boşluqlarla doldurulmuşdur) |
| D | Tarix | Ay, gün və ili ayırmaq üçün rəqəmlər və simvol (YYYYAAG formatında daxili olaraq 8 rəqəm olaraq saxlanılır) |
| F | Üzən nöqtə | -, ., 0–9 (sağda əsaslandırılmış, boşluqlarla doldurulmuş) |
| L | Məntiqi | Y, y, N, n, T, t, F, f və ya ? (başlanılmadıqda) |
| M | Memo | İstənilən ASCII mətni (daxili olaraq .dbt blok nömrəsini təmsil edən 10 rəqəm kimi saxlanılır, sağa əsaslandırılmış, boşluqlarla doldurulmuşdur) |
| N | Rəqəm | -, ., 0–9 (sağda əsaslandırılmış, boşluqlarla doldurulmuş) |









## İstinadlar ##

* [.dbf - Vikipediya](https://en.wikipedia.org/wiki/.dbf)


