{
  "date" : "2023-01-17",
  "keywords" : [ "DSN", "what is a DSN file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "DSN faylları yarada və aça bilən DSN fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title" : "DSN Fayl Format - Verilənlər Bazasının Mənbə Adı Faylı",
  "linktitle" : "DSN",
  "menu" : {
    "docs" : {
      "identifier":"database-dsn-az",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-17"
}

## DSN faylı nədir?

DSN Məlumat Mənbəsinin Adı deməkdir və verilənlər bazası ilə əlaqə məlumatlarını saxlamaq üçün istifadə olunan fayl formatıdır. DSN faylları adətən ODBC (Açıq Database Connectivity) ilə birlikdə istifadə olunur və server adı, istifadəçi adı və parol kimi ona qoşulmaq üçün lazımi məlumatları təmin etməklə xüsusi verilənlər bazasına asan giriş imkanı verir. Fayl adətən düz mətndədir və mətn redaktoru vasitəsilə yaradıla və redaktə edilə bilər. Windows, Linux və Mac kimi müxtəlif əməliyyat sistemlərində istifadə edilə bilər.

## DSN faylını necə yaratmaq olar?

DSN faylının yaradılması üsulu əməliyyat sisteminə və mövcud alətlərə görə dəyişə bilər. Aşağıdakı addımlar Windows sistemində DSN faylının yaradılması prosesinin ümumi icmalını təqdim edir.

1. Başlanğıc menyusunda ODBC Məlumat Mənbələrini axtararaq ODBC Məlumat Mənbəsi Administratorunu açın.
2. Sistem DSN sekmesini seçin və Əlavə et düyməsini basın.
3. Qoşulmaq istədiyiniz verilənlər bazası üçün uyğun sürücünü seçin və Bitir düyməsini basın.
4. Verilənlər bazasına qoşulmaq üçün server adı, istifadəçi adı və parol kimi lazımi məlumatları doldurun.
5. DSN faylını saxlamaq üçün OK düyməsini basın.

Alternativ olaraq, siz .dsn uzantısı ilə düz mətn faylı yaradaraq və lazımi əlaqə məlumatlarını formatda daxil etməklə DSN faylını əl ilə yarada bilərsiniz:

```
[ODBC]
DRIVER=driver_name
SERVER=server_name
DATABASE=database_name
UID=username
PWD=password
```

Daha sonra verilənlər bazasına qoşulmaq üçün bu faylın yolundan kodunuzda/skriptinizdə DSN kimi istifadə edə bilərsiniz.

## DSN faylını açan proqramlar

DSN faylı verilənlər bazasına qoşulmaq üçün istifadə olunan server adı, istifadəçi adı və parol kimi məlumatları saxlayan düz mətn faylıdır. Xüsusi verilənlər bazasına asan girişi təmin etmək üçün adətən ODBC (Açıq Database Connectivity) ilə birlikdə istifadə olunur.

DSN faylının məzmununu açmaq və onlara baxmaq üçün siz Notepad, Sublime Text, Atom və s. kimi istənilən mətn redaktorundan istifadə edə bilərsiniz. Bu proqramlar sizə DSN faylını açmağa və onun daxilində saxlanılan əlaqə məlumatlarına baxmaq imkanı verəcək.

Bununla belə, verilənlər bazasına qoşulmaq və Python, Java, C# kimi proqramlaşdırma dili kimi ODBC dəstəyi olan proqramı və ya Microsoft Access kimi verilənlər bazası idarəetmə alətini SEÇ, INSERT, YENİLƏNDİR, SİL və s. kimi əməliyyatları yerinə yetirmək üçün DSN faylından istifadə etmək , SQL Server Management Studio tələb olunur. Bu proqramlar verilənlər bazasına qoşulmaq və istədiyiniz əməliyyatı yerinə yetirmək üçün DSN faylındakı məlumatlardan istifadə edə bilər.

## İstinadlar

* [DSN (Məlumat Mənbəsinin Adı) nədir?](https://support.microsoft.com/en-us/topic/what-is-a-dsn-data-source-name-ae9a0c76-22fc-8a30- 606e-2436fe26e89f)



