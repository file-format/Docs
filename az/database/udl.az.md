{
  "date": "2021-06-21",
  "keywords": [
"UDL",
"uzadılması",
"udl faylı",
"udl fayl formatı",
"Verilənlər bazası fayl növü",
"Verilənlər bazası fayl formatı",
"udl faylı nədir"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "UDL fayl formatı və UDL faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "UDL - Microsoft Universal Data Link Faylı",
  "linktitle": "UDL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ud-azl"
}
},
  "lastmod": "2021-06-21"
}

## UDL faylı nədir?
.udl uzantılı fayl Microsoft Universal Data Link faylı adlanır; əlaqə atributlarının təyin edilməsi; verilənlər bazası ilə əlaqə yaratmaq üçün Windows proqramları tərəfindən istifadə olunur. UDL faylı OLE DB məlumat mənbəyi üçün əlaqə sətrini ehtiva edir; istifadəçi adı və parol və əsas əlaqə simli xüsusiyyətləri ilə. Bağlantı sətirində xassələri birbaşa əl ilə göstərməyin qarşısını almaq üçün alternativ olaraq əlaqə məlumatını .udl faylında saxlamaq üçün Data Link Properties dialoq qutusu istifadə edilə bilər.

## UDL fayl formatı
Əsasən, UDL (Universal Data Link) faylı xüsusi atributları və ya xassələri olan verilənlər bazası əlaqə sətirindən ibarət sadə mətn faylıdır. UDL faylı yaradıldıqdan sonra əlaqəni yoxlamaq üçün SQL Server Management Studio istifadə edərək sınaqdan keçirilə bilər.

### Bağlantı sətirinin xüsusiyyətləri
Düzgün əlaqəni təmin etmək üçün UDL-də aşağıdakı xüsusiyyətlər təyin edilə bilər:

- **Server Adı**: daxil olmaq istədiyiniz verilənlər bazasının yerləşdiyi serverin yeri.
- **Autentifikasiya Seçimləri**
- **Windows Authentication**: Hazırda daxil olmuş istifadəçinin Windows hesabı etimadnaməsini istifadə edərək SQL Serverə doğrulama.
- **SQL Server Authentication**: Login ID və paroldan istifadə edərək doğrulama.
- **Active Directory - İnteqrasiya edilmiş**: Azure Active Directory identifikasiyası ilə inteqrasiya olunmuş autentifikasiya; SQL Server üçün Windows autentifikasiyası üçün də istifadə edilə bilər.
- **Active Directory - Parol**: Azure Active Directory identifikasiyası ilə istifadəçi ID və parol autentifikasiyası.
- **Active Directory - Xarici İşlər Nazirliyinin dəstəyi ilə Universal**: Azure Active Directory identifikasiyası ilə interaktiv autentifikasiya.
- **Active Directory - Service Principal**: Azure Active Directory xidmət prinsipi ilə identifikasiya.
- **Server SPN**: Etibarlı bağlantıdan istifadə edirsinizsə, server üçün xidmətin əsas adını (SPN) təyin edə bilərsiniz.
- **İstifadəçi adı**: Məlumat mənbəyinə daxil olarkən autentifikasiya üçün istifadə etmək üçün İstifadəçi ID-ni yazın.
- **Parol**: Məlumat mənbəyinə daxil olarkən autentifikasiya üçün istifadə ediləcək parolu yazın.
- **Boş parol**: Yoxlandıqda, göstərilən provayderə əlaqə sətirində boş paroldan istifadə etməyə imkan verir.
- **Parolun saxlanmasına icazə verin**: Parolun əlaqə sətri ilə yadda saxlanmasına imkan verir.
- **Məlumat üçün güclü şifrələmədən istifadə edin**: əlaqə vasitəsilə ötürülən məlumatlar şifrələnəcək.
- **Trust server certificate**: The server's certificate will be validated.
- **Database**: Daxil olmaq istədiyiniz verilənlər bazası adı.
- **Verilənlər bazası faylını verilənlər bazası adı kimi əlavə edin**: Əlavə edilə bilən verilənlər bazası üçün əsas faylın adını müəyyən edir.

## İstinadlar ##

* [Microsoft Data Access Components](https://en.wikipedia.org/wiki/Microsoft_Data_Access_Components#Universal_data_link)

* [Universal Data Link (UDL) konfiqurasiyası](https://learn.microsoft.com/en-us/sql/connect/oledb/help-topics/data-link-pages?view=sql-server-ver15)


