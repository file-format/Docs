{
  "date": "2023-03-22",
  "keywords": [
"cnf faylı",
"cnf faylı nədir",
"cnf faylını necə açmaq olar",
"fayl",
"cnf fayl uzantısı",
"uzadılması"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CNF Fayl Format - MySQL Konfiqurasiya Faylı",
  "description": "CNF faylları yarada və aça bilən CNF formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "CNF",
  "menu": {
    "docs": {
      "identifier": "settings-cnf-az",
      "parent": "settings"
}
},
  "lastmod": "2023-03-22"
}

## CNF faylı nədir?

MySQL-də CNF faylı (konfiqurasiya faylı kimi də tanınır) MySQL serveri üçün konfiqurasiya parametrlərini saxlamaq üçün istifadə olunur. CNF faylının yeri əməliyyat sistemindən və istifadə edilən quraşdırma metodundan asılı olaraq dəyişə bilər. Konfiqurasiya adətən istifadə əsasında verilənlər bazası performansını optimallaşdırmaq üçün tənzimlənə bilən standart simvol kodlaşdırması, fasilələr, keş və bufer konfiqurasiyaları kimi müxtəlif parametrləri ehtiva edir.

## CNF Fayl Format - Əlavə məlumat

MySQL-də aşağıdakı addımlardan istifadə edərək CNF yarada bilərsiniz:

1. Mətn redaktorunu açın, məsələn, Notepad və yeni fayl yaradın.
2. İstədiyiniz konfiqurasiya seçimlərini fayla əlavə edin, hər sətirdə bir. Budur bir nümunə:

```
[mysqld]
datadir=/var/lib/mysql
socket=/var/lib/mysql/mysql.sock
user=mysql
symbolic-links=0

[client]
user=root
password=password123
```

3. Faylı .cnf uzantısı ilə yadda saxlayın, məsələn, mysql.cnf.
4. Faylı müvafiq qovluğa köçürün. Məsələn, Linux sistemlərində kataloq /etc/mysql/conf.d/ və ya /etc/mysql/ ola bilər.
5. Yeni konfiqurasiya parametrlərinin qüvvəyə minməsi üçün MySQL serverini yenidən başladın.

CNF faylına edilmiş hər hansı dəyişiklikləri istehsal mühitində tətbiq etməzdən əvvəl qeyri-istehsal mühitində sınaqdan keçirdiyinizə əmin olun.

## CNF faylını necə açmaq olar?

CNF faylı mətn faylıdır və Notepad kimi istənilən mətn redaktorundan istifadə etməklə asanlıqla açıla bilər. Siz həmçinin sağ klikləyib menyudan Birlikdə Aç seçimini etməklə onu aça bilərsiniz. Fayl açıq olduqdan sonra lazım olduqda konfiqurasiya parametrlərini redaktə edə bilərsiniz. CNF MySQL serverinə aid müxtəlif parametrləri ehtiva edir, məsələn, port nömrəsi, giriş seçimləri və bufer ölçüləri. Parametrləri redaktə etdikdən sonra dəyişiklikləri yadda saxlayın və mətn redaktorunu bağlayın. Nəhayət, dəyişikliklərin qüvvəyə minməsi üçün MySQL serverini yenidən başladın.

Qeyd edək ki, MySQL konfiqurasiya faylını redaktə edərkən diqqətli olmaq vacibdir, çünki səhv parametrlər serverin gözlənilməz davranışına və ya ümumiyyətlə başlamamasına səbəb ola bilər. Hər hansı bir dəyişiklik etməzdən əvvəl orijinal faylın ehtiyat nüsxəsini çıxarmaq tövsiyə olunur, belə ki, zəruri hallarda onu bərpa edə bilərsiniz.

## İstinadlar
* [MySQL](https://en.wikipedia.org/wiki/MySQL)


