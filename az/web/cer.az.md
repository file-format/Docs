{
  "date": "2021-07-13",
  "keywords": [
"CER",
"uzadılması",
"fayl",
"format",
"veb",
"sertifikat",
"dil"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CER - Sertifikat Fayl Formatı",
  "description": "CER fayl formatı və CER fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "CER",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ce-azr"
}
},
  "lastmod": "2021-07-13"
}

## CER faylı nədir? ##

A file with an extension .cer is responsible for storing some information about the owner certificate and the specific public key. This format of files cannot store the private keys and have the capacity to store only one certificate which is x509. Xüsusi olaraq qorunan sertifikat orqanları HTTPS-ə aid olanlardır, gözdən keçirmək üçün etibarlı və təhlükəsiz protokol  
CER serverinizin sertifikatıdır. Adətən domen üçün sertifikat orqanı tərəfindən qəbul edilir. CER, əsasən, [CRT](/web/crt/) ilə eyni hesab olunur, baxmayaraq ki, hər ikisi SSL sertifikatının eyni formatıdır, lakin fərqli fayl adı uzantılarıdır.
Bunlar sadəcə brauzeri açmaq və istifadə olunan brauzerin və ya veb-saytın təhlükəsizliyini yoxlamaqla əməliyyat sistemlərində istifadə edilə bilər.

## Qısa tarix ##

1995-ci ildə Thawte, ABŞ-dan kənarda ictimai SSL (təhlükəsiz yuva bağlantısı) sertifikatları məsələsini həll etmək üçün ilk sertifikatlaşdırma orqanı oldu. Bundan sonra 1995-ci ildən 2020-ci ilə qədər yaradılan bir sıra belə orqanlar var.

## CER Fayl Format ##

Bu fayllar sadə ola bilər
* PKC S#7 Base64 ASCII kodlamasından ibarətdir
* Onun fayl uzantıları p7b və ya p7cZ-dir
* Binar məzmun üçün sertifikat DER və ya pkcs12/pfx olacaqdır.
Bəzi unikal spesifikasiyaları olan bir çox sertifikat faylları var:
* .pem, Bu formatı zəncirləyən təşkilat usThawteificate zaman sertifikatlar yaratmaq üçün yaxşı məlumdur
* .arm, sertifikatın çıxarılması metodu özünü imzalamağa kömək etdikdə, tələb olunduqda, bu məqsəd üçün göstərilən format .arm-dır. Baza-64 ASCII kodlaşdırmasında təmsil olunur.
* .der, İkili məlumatlardan ibarətdir. Bu o deməkdir ki, yalnız bir sertifikat üçün istifadə edilə bilər
* .pfx (PKC512), CA tərəfindən verilmiş sertifikata və ya özünü imzalayan sertifikata uyğun gələn şəxsi açardan ibarətdir. Bu format bir SSL tətbiqinin digərinə çevrilməsi ilə məşhurdur.


