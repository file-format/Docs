{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HTACCESS Faylı - Apache HTACCESS Fayl Formatı",
  "description": "HTACCESS faylının nə olduğunu öyrənmək üçün fayl formatı bələdçisi",
  "linktitle": "HTACCESS",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-htacces-azs"
}
},
  "lastmod": "2019-09-10"
}

## HTACCESS faylı nədir?

HTACCESS faylı vebsaytın müxtəlif qovluqları/kataloqları üçün konfiqurasiya dəyişikliklərinə icazə verən mexanizm təmin edən Apache konfiqurasiya faylıdır. Bu, kataloq və alt kataloqlara tətbiq olunan konfiqurasiya direktivlərini ehtiva edir.

HTACCESS faylı vebsaytın indeks səhifəsini təyin etmək, 404 (Səhifə tapılmadı) səhv səhifəsini siyahıya almaq, 301 və ya 302 səhifə yönləndirmələrini yerinə yetirmək, müəyyən bir IP ünvanından və ya digər vebsaytlardan girişi bloklamaq kimi bir sıra yoxlamalar həyata keçirir. .htaccess fayllarının istifadəsi Apache HTTP serverinizin ümumi performansını ləngidir.

## HTACCESS fayl formatı

HTACCESS faylları düz mətn faylı formatında diskdə saxlanılır. Bu o deməkdir ki, siz bu faylları istənilən mətn redaktorunda aça və redaktə edə bilərsiniz. . hərfindən əvvəl heç bir ad yoxdur. .htaccess faylında, onun qovluq daxilində gizli fayl olduğunu göstərir.

## HTACCESS faylının ümumi istifadələri

HTACCESS faylının beş ümumi istifadəsi aşağıdakı kimidir.

### Mod_Yenidən Yaz

HTACCESS faylı vebsaytdakı URL-lərin və veb səhifələrin istifadəçilərə necə göstərildiyini təyin etmək və dəyişdirmək üçün istifadə edilə bilər.

### İdentifikasiyası

Doğrulama .htpasswd adlı passowrd faylı yaratmaqla .htaccess ilə əldə edilə bilər. Bu, sayt ziyarətçilərinə veb səhifənin müəyyən bir bölməsinə daxil olmaq istədikləri təqdirdə parol təqdim etməyə imkan verir.

### Xüsusi Xəta Səhifələri

.htaccess faylı ilə 400 Bad Request, 401 Authorization Required, 403 Forbidden Page, 404 File not found and 500 Internal Error kimi fərdi xəta səhifələri yarada bilərsiniz. Bununla belə, bunlar serverin fəaliyyətini yavaşlatacaq, çünki bütün yoxlamalar səhifələrə daxil olduqda həyata keçiriləcək.

### MIME növləri

Apache HTACCESS faylları Çoxməqsədli İnternet Poçt Genişləndirmələri (MIME) növlərini daxil etmək üçün dəyişdirilə bilər. Bu, serverinizə sayt tərəfindən dəstəklənməyən proqram fayllarının çatdırılmasını dəstəkləməyə imkan verir.

### SGK

Server Side Includes (SSI) vebsaytda əla vaxta qənaət rolunu oynayır. SSI, hte aşağıdakı kodu .htaccess faylınıza daxil etməklə aktivləşdirilə bilər.

```
AddType text/html .shtml
AddHandler server-parsed .shtml</pre>
```

## Apache HTACCESS fayl nümunəsi

```
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

## İstinadlar

* [Apache HTTP Server Tutorial: .htaccess files](https://httpd.apache.org/docs/current/howto/htaccess.html)

