{
  "date": "2019-10-11",
  "keywords": [
"rar failą",
"rar failo formatas",
"kas yra rar failas",
"failą",
"retas pavyzdys",
"rar failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RAR",
  "description": "Kas yra RAR failo plėtinys ir API, kurios gali kurti ir atidaryti RAR failus.",
  "linktitle": "RAR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-ra-ltr"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra RAR failas?

Failai su plėtiniu .rar yra archyviniai failai, sukurti informacijai saugoti suglaudinta arba įprasta forma. RAR, kuris reiškia Roshal ARchive failo formatą, yra patentuotas failo formatas, kurį 1995 m. sukūrė Eugene Roshal, kuris buvo Rusijos programinės įrangos inžinierius. Formatas naudojamas failams archyvuoti įvairiais būdais, įskaitant įvairius suspaudimo būdus. Yra keletas taikomųjų programų, skirtų Windows, Linux ir MacOS, kad būtų galima išgauti RAR failus. WinRAR programinė įranga, kurią sukūrė RARLab, yra bendro naudojimo failų archyvavimo programa (nemokama 40 dienų), skirta Microsoft Windows platformai; programinę įrangą į Linux (tik kaip ištraukiklį) perkėlė tas pats autorius Eugene Roshal.

## RAR failo formato versijų istorija

* v1.3 (originalas, neturi „Rar!“ parašo)

* v1.5

* v2.0 – išleista su WinRAR 2.0 ir Rar, skirta MS-DOS 2.0

* v2.9 – išleista WinRAR 3.00 versijoje

* v5.0 – palaiko WinRAR 5.0 ir naujesnės versijos


## Pagrindinės RAR formato savybės

RAR buvo gana ilgą laiką ir buvo vienas iš mėgstamiausių archyvavimo failų formatų. Pagrindinės RAR formato savybės yra šios:

**`Didelis suspaudimo laipsnis:`** Geresnis, palyginti su [ZIP](/compression/zip/), palyginamas su 7z ir zipx formatu.

**`Tvirtas failų šifravimas pagal dizainą:`** Šifruoti RAR4 archyvai remiasi AES-128 pagrįstu šifravimu, o šifruoti RAR5 archyvai remiasi AES-256 šifravimu su patobulintu raktų planavimu

**`Išplėstinės klaidų taisymo ir duomenų atkūrimo galimybės:`** pasirenkami atkūrimo įrašai kuriant archyvą

**`Failo dydis:`** Mažiausiai 20 baitų ir daugiausiai 2^63 baitų (8 eksabaitai viso archyvo dydžio)

**`Kelių tomų RAR archyvai:`** Galimybė padalyti didelius archyvus į kelis mažesnius failus, kad būtų lengviau perkelti tinkle. Tokiu atveju failų plėtiniai padidinami 1, kad būtų rodomi padalinti tomai

## RAR failo formatas

Išsamios RAR formato specifikacijos nėra viešai prieinamos, todėl informacijos apie formatą negalima suformuluoti glaustai.

### Bendras archyvo išdėstymas

Bendras 5.0 versijoje pristatyto RAR failo formato išdėstymas yra toks:

|Failo formatas
---|
|Savaime ištraukiamas modulis (neprivaloma)
|RAR 5.0 parašas
|Archyvo šifravimo antraštė (pasirenkama)
|Pagrindinio archyvo antraštė
|Archyvuoti komentarų paslaugos antraštę (pasirenkama)
1 failo antraštė
|Ankstesnio failo paslaugų antraštės (NTFS ACL, srautai ir kt.) (neprivaloma)
|...
|Failo antraštė N
|Ankstesnio failo paslaugų antraštės (NTFS ACL, srautai ir kt.) (neprivaloma)
|Atkūrimo įrašas (neprivaloma)
|Archyvo pabaigos antraštė

Informacijos apie kiekvieną aukščiau paminėtą RAR failo skyrių rasite [RAR 5.0 File Format specifications](https://www.rarlab.com/technote.htm#arcstruct) dokumente.

#### Savaiminio išskleidimo RAR archyvai

Jei pats RAR failas išsiskleidžia savaime, savaiminio išskleidimo informacija yra failo pradžioje prieš archyvo parašą. Jo dydis ir turinys nėra apibrėžti.

#### RAR 5.0 parašas

RAR parašas yra 8 baitų antraštė, kurią sudaro šis stebuklingas skaičius:

0x 52 61 72 21 1A 07 00

kur

0x6152 – HEAD_CRC

0x72 – HEAD_TYPE

0x1A21 – HEAD_FLAGS

0x0007 – HEAD_SIZE

## Nuorodos

* [RAR 5.0 archyvo formatas](https://www.rarlab.com/technote.htm)

* [RAR – Vikipedija](https://en.wikipedia.org/wiki/RAR_(file_format))


