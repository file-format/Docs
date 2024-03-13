{
  "date": "2022-09-01",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CRL Faylı - Sertifikat Ləğv Siyahısı",
  "description": "CRL faylları yarada və aça bilən CRL fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "CRL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cr-azl"
}
},
  "lastmod": "2022-09-01"
}

## CRL faylı nədir?

CRL (Certificate Revocation List) faylı sertifikat orqanının (CA) təyin edilmiş ləğv tarixindən əvvəl ləğv etdiyi X.509 rəqəmsal sertifikatların qara siyahısıdır. O, təhlükəsizlik administratorlarına təsirə məruz qalmış rəqəmsal sertifikatları bloklamağa imkan verən problem və ləğvetmə tarixi haqqında məlumatı ehtiva edir. Əsas məqsədi etibarsız və etibarsız sertifikatlar haqqında məlumat vermək olduğu üçün CRL müddəti bitmiş sertifikatları daxil etmir.

**CRL fayllarını** aça bilən proqramlara OpenSSL, Microsoft IIS Server və Citrix NetScaler daxildir.

## CRL Fayl Format - Ətraflı Məlumat

CRL faylları X.509 standartında məlumat ehtiva edir ki, bu da açıq açar məlumatlarının paylaşılması üçün onun semantikasını müəyyən edir. CRL faylında olan digər məlumatlara sertifikatların ləğv edildiyi vaxt məhdudiyyəti, ləğvin səbəbi, ləğv edilmiş sertifikatın seriya nömrəsi və vaxt möhürü daxil ola bilər.


### Sertifikatların CRL-ə əlavə edilməsinin əsas səbəbləri

Veb saytınızın sertifikatının ləğv edilməsinin və CRL-ə əlavə edilməsinin bir neçə səbəbi ola bilər. Onlardan bəziləri ola bilər;

1. Sertifikatınızın şəxsi açarı oğurlanıb
1. Sertifikatınız etibarlı deyil və ya CA tərəfindən yanlış verilmişdir
1. Sertifikatla əlaqəli təşkilati təfərrüatlar dəyişdirilir və CA yeni sertifikat verir
1. Sertifikatın ləğv edilməsinə səbəb olan hər hansı digər qaçılmaz səbəb

## İstinadlar

* [Milli Standartlar və Texnologiya İnstitutu (NIST)](https://csrc.nist.gov/glossary/term/CRL)

* [Internet Engineering Task Force (IETF) RFC 5280](https://tools.ietf.org/html/rfc5280)

* [Sertifikatlaşdırma Ləğv Siyahısı](https://en.wikipedia.org/wiki/Certificate_revocation_list)


