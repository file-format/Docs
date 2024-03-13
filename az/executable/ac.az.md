{
  "date" : "2023-01-11",
  "keywords" : ["ac file", "what is an aci file", "file", "how to open ac file", "ac file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "ACCDB faylları yarada və aça bilən AC fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title" : "AC Fayl Format - Autoconf Skript Faylı",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac-az",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## AC faylı nədir?

AC faylı Autoconf skript faylıdır. **Autoconf** proqram mənbə kodu paketlərini avtomatik konfiqurasiya etmək üçün qabıq skriptləri istehsal edən M4 makrolarının genişləndirilə bilən paketidir. Bu skriptlər istifadəçinin əl müdaxiləsi olmadan paketləri UNIX-ə bənzər sistemlərin bir çox növlərinə uyğunlaşdıra bilər. Autoconf paketin M4 makro çağırışları şəklində istifadə edə biləcəyi əməliyyat sistemi xüsusiyyətlərini sadalayan şablon faylından paket üçün konfiqurasiya skripti yaradır.

Producing configuration scripts using Autoconf requires GNU M4. Autoconf-un konfiqurasiya skripti onu tapa bilməsi üçün Autoconf-u konfiqurasiya etməzdən əvvəl GNU M4-ü quraşdırmalısınız (ən azı 1.4.6 versiyası, baxmayaraq ki, 1.4.13 və ya daha sonrakı versiya tövsiyə olunur). Autoconf tərəfindən hazırlanmış konfiqurasiya skriptləri öz-özünə mövcuddur, ona görə də onların istifadəçilərinin Autoconf (və ya GNU M4) olması lazım deyil.

## AC faylını necə açmaq olar?

AC avtomatik konfiqurasiya deməkdir. Bu, GNU Autoconf tərəfindən yaradılan skriptdir ki, paketdəki lazımi xüsusiyyətləri sınamaqla proqram mənbə kodunu müxtəlif Posix-ə bənzər sistemlərə uyğunlaşdırmağa imkan verir. Skript AC faylı adlanır.

## Əsas Autotools Komponentləri

An understanding of GNU autotools (`automake`, `autoconf` etc.) can be useful when working with ebuilds:

Autotools əlaqəli paketlər toplusudur və birlikdə istifadə edildikdə portativ proqram təminatının yaradılması ilə bağlı çətinliklərin çoxunu aradan qaldırır. Bu alətlər, bir neçə nisbətən sadə yuxarı axınla təchiz edilmiş daxiletmə faylları ilə birlikdə paket üçün qurma sistemi yaratmaq üçün istifadə olunur.

**Əsas avtoalət komponentlərinin bir-birinə necə uyğunlaşmasının əsas icmalı.**

![A basic overview of how the main autotools components fit together](https://devmanual.gentoo.org/general-concepts/autotools/diagram.png "A basic overview of how the main autotools components fit together")

Sadə bir quraşdırmada:

- `Autoconf` proqramı `configure.in` və ya `configure.ac`-dan konfiqurasiya skripti istehsal edir.
- `automake` proqramı Makefile.am-dan Makefile.in yaradır.
- `konfiqurasiya` skripti Makefile.in fayllarından bir və ya daha çox Makefile faylı yaratmaq üçün işlədilir.
- make” proqramı proqramı tərtib etmək üçün Makefile faylından istifadə edir.

## İstinadlar
* [Autoconf Software](https://www.gnu.org/software/autoconf/)
* [Avtotools əsasları](https://devmanual.gentoo.org/general-concepts/autotools/index.html)



