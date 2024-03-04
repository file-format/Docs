{
  "date" : "2023-05-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "CPIO failas – Unix CPIO archyvo failo formatas",
  "description":"Sužinokite, kas yra CPIO failas ir API, kurios gali kurti ir atidaryti CPIO failus.",
  "linktitle" : "CPIO",
  "menu" : {
    "docs" : {
      "identifier" : "compression-cpio-lt",
      "parent" : "compression"
}
},
  "lastmod" : "2023-05-10"
}

## Kas yra CPIO failas?

CPIO failas yra archyvo failas, sukurtas Unix Copy In Copy Out (CPIO) formatu. Jis panašus į TAR failo formatą, išskyrus tai, kad jis yra nesuspaustas. CPIO failai gali saugoti įrenginio failus, simbolines nuorodas ir išplėstinius failų atributus.

## CPIO failo formatas

CPIO archyvas sukuriamas kaip dvejetainis failas, kurio žmogus neskaito. Jame saugoma failų ir katalogų kolekcija. CPIO archyvo turinys identifikuojamas su metaduomenų informacija, tokia kaip failų pavadinimai, leidimai, nuosavybės teisė ir laiko žymos. Ši metaduomenų informacija taip pat saugoma archyvo faile, kad sistema galėtų ją pasiekti iš šono.

## CPIO archyvo formatas

CPIO failą sudaro vienas ar daugiau sujungtų narių failų. Kiekvieną archyve esantį failą sudaro antraštė, po kurios eina failo turinys, kaip nurodyta antraštėje. Archyvo pabaigoje yra kita antraštė, kurią apibūdina tuščias failas pavadinimu TRAILER!!.

### CPIO archyvų tipai

Yra dviejų tipų CPIO archyvai. Jie skiriasi tik antraštės stiliumi.

* ASCII archyvai – šie CPIO archyvai turi spausdinamą antraštę, kuri tampa CPIO archyvo dalimi, jei patį archyvą sudaro ASCII failai

* Dvejetainiai archyvai – šie CPIO archyvai turi dvejetaines antraštes.


## Darbas su CPIO archyvu

### Kaip sukurti CPIO archyvus?

Galite sukurti CPIO Unix tipo sistemose naudodami komandą **cpio**. Ši komanda suras visus failus ir katalogus dabartiniame kataloge ir jo pakatalogiuose. Tada ši išvestis perduodama į cpio komandą, kuri sugeneruos naują CPIO archyvą pavadinimu archive.cpio.

```
find . -depth -print | cpio -ov > archive_cpio.cpio
```
### Kaip ištraukti failus iš CPIO archyvų?

Ši komanda ištraukia failus iš esamo archyvo.

```
cpio -id < archive_cpio.cpio
```
Jis nuskaitys archyvą.cpio failą iš standartinės įvesties ir ištrauks failus į dabartinį katalogą.


## Nuorodos

* [CPIO – Vikipedija](https://en.wikipedia.org/wiki/Cpio)

* [CPIO File Format](https://www.ibm.com/docs/en/zos/2.2.0?topic=formats-cpio-format-cpio-archives)

