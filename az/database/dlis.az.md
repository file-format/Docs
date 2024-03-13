{
  "date" : "2023-01-16",
  "keywords" : [ "DLIS", "what is a DLIS file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "DLIS faylları yarada və aça bilən DLIS fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title" : "DLIS Fayl Format - Yaxşı Giriş Məlumat Faylı",
  "linktitle" : "DLIS",
  "menu" : {
    "docs" : {
      "identifier":"database-dlis-az",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-16"
}

## DLIS faylı nədir?

.dlis fayl formatı neft və qaz sənayesində quyu jurnalı məlumatlarının saxlanması və mübadiləsi üçün standart fayl formatıdır. Format Logging Industry Data Standard (LIDS) komitəsi tərəfindən hazırlanmışdır və Rəqəmsal Giriş Məlumatı Standartı deməkdir. Format müxtəlif sistemlər arasında oxumaq, yazmaq və mübadilə etmək asan bir şəkildə yaxşı jurnal məlumatlarını saxlamaq üçün nəzərdə tutulmuşdur.

DLIS faylları quyu jurnalı məlumatlarını və onun xarakteristikalarını, məsələn, jurnal məlumatlarının növü (məsələn, müqavimət, qamma şüası), ölçü vahidləri və quyudakı məlumatların yerini təsvir edən məntiqi qeydlər toplusunu ehtiva edir. Faktiki log məlumatları ayrıca ikili fayllarda saxlanılır və DLIS faylındakı məntiqi qeydlər tərəfindən istinad edilir.

## Quyu Giriş Məlumatları haqqında Qısa Məlumat

Quyu jurnalı məlumatları quyuda müxtəlif dərinliklərdə, adətən qazma prosesi zamanı və ya quyu qazıldıqdan sonra aparılmış ölçmələrin qeydidir. Bu ölçmələrə quyudakı süxur və mayelərin müxtəlif fiziki, kimyəvi və/və ya geofiziki xassələri daxil ola bilər. Quyu jurnalı məlumatlarının bəzi nümunələri bunlardır:

- Elektrik müqaviməti: süxurun elektrik cərəyanının axınına müqavimət göstərmə qabiliyyətinin ölçüsü
- Qamma şüası: süxurun təbii radioaktivliyinin ölçüsü
- məsaməlilik: qayadakı açıq boşluqların və ya məsamələrin miqdarının ölçüsü
- Sonic: səs dalğasının qayadan keçməsi üçün lazım olan vaxtın ölçüsü
- Sıxlıq: vahid həcmə düşən süxurun kütləsinin ölçüsü
- Litologiya: qaya növünün və ya formalaşmasının ölçüsü

Quyu jurnalı məlumatları neft və qaz sənayesində müxtəlif məqsədlər üçün istifadə olunur, məsələn:

- Karbohidrogen tərkibli layların yerinin və keyfiyyətinin müəyyən edilməsi
- Quyunun hasilat potensialının qiymətləndirilməsi
- Quyunun tamamlanmasının və stimullaşdırılmasının planlaşdırılması və monitorinqi
- Zamanla quyu davranışının monitorinqi

## PPDM ilə əlaqə

PPDM (Professional Petroleum Data Management) quyu və hasilat məlumatlarının idarə edilməsi üçün ümumi məlumat modelini təmin edən neft və qaz sənayesi məlumatlarının idarə edilməsi standartıdır. PPDM məlumat modeli, DLIS məlumatları da daxil olmaqla quyu jurnalı məlumatlarını təşkil etmək və idarə etmək üçün istifadə edilə bilən standart məlumat obyektləri və əlaqələrin dəstini müəyyən edir.

PPDM məlumat modelinə quyular, quyu başlıqları, quyu jurnalları və hasilat məlumatları kimi quyu və hasilat məlumatları üçün məlumat obyektləri daxildir. O, həmçinin bu məlumat obyektləri arasındakı əlaqələri, məsələn, quyu və onunla əlaqəli quyu qeydləri arasındakı əlaqəni ehtiva edir.

PPDM məlumat modeli, DLIS məlumatları da daxil olmaqla quyu jurnalı məlumatlarını təşkil etmək və idarə etmək üçün ardıcıl, sənaye standartlı bir üsul təqdim edir. Bu, müxtəlif təşkilatlara ümumi məlumat modelindən istifadə edərək məlumatları paylaşmağa və mübadilə etməyə, məlumatların qarşılıqlı fəaliyyət qabiliyyətini yaxşılaşdırmağa və məlumat inteqrasiyası xərclərini azaltmağa imkan verir.

PPDM məlumat modelinin və DLIS məlumatlarının birlikdə istifadəsi quyu jurnalı məlumatlarını sənaye standartlarına uyğun və digər sistemlər və proqramlar üçün asanlıqla əldə edilə bilən şəkildə saxlamağa və idarə etməyə imkan verir.


