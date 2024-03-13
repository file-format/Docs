{
  "date": "2022-02-17",
  "keywords": [
"gpg faylı",
"gpg fayl formatı",
"gpg faylı nədir",
"fayl",
"gpg nümunəsi",
"gpg fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GPG Faylı - GNU Privacy Guard Public Keyring File",
  "description": "GPG faylları yarada və aça bilən GPG faylı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "GPG",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-gp-azg"
}
},
  "lastmod": "2022-02-17"
}

## GPG faylı nədir?

GPG faylı GNU Privacy Guard (GnuPG) şifrələmə proqramı tərəfindən istifadə edilən şifrələmə/şifrləmə açarı faylıdır. GnuPC proqramının özü RFC4880 müəyyən edilmiş OpenPGP standartına əsaslanır və PGP kimi də tanınır. Müasir əməliyyat sistemində GPG-dən uğurlu istifadənin açarı onun çox yönlü açar idarəetmə sistemidir. GPG-nin komanda xətti proqramı digər proqramlarla asanlıqla inteqrasiya etməyə imkan verir.

## GPG fayl formatı

GPG faylları şifrələnmiş ikili fayllar kimi saxlanılır və təbii ki, onlar insan tərəfindən oxunmur. Şifrələnmiş GPG faylının şifrəsini açmaq üçün eyni təhlükəsiz açardan istifadə etməlisiniz. Və buna görə də bu faylların daxili fayl formatı məlum deyil.

## Linux-da GPG ilə faylları şifrələyin və deşifrə edin

GPG komanda xətti yardım proqramı Linux-da faylları şifrələmək və deşifrə etmək üçün istifadə edilə bilər.

### Faylın Şifrələnməsi

Fayl aşağıda göstərildiyi kimi -c (yarat) seçimi ilə gpg əmrindən istifadə edərək şifrələnə bilər.

```
gpg -c file1.txt
```
Bu əmrin icrası orijinal `file1.txt` faylının məzmununu şifrələmək üçün açar söz tələb edir. Bu, şifrələnmiş file1.txt.gpg faylının yaradılması ilə nəticələnir.

### Şifrənin açılması və Faylın çıxarılması

Şifrələnmiş faylın şifrəsini açmaq və çıxarmaq üçün aşağıdakı əmrdən istifadə etmək olar.

```
gpg cfile.txt.gpg
```

## İstinadlar

* [GNUPG](https://gnupg.org/)

* [HDF - Wikipedia](https://en.wikipedia.org/wiki/Hierarchical_Data_Format)


