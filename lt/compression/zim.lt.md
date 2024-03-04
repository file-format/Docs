{
  "date": "2019-12-09",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ZIM failo formatas – OpenZIM archyvo failas",
  "description": "Sužinokite apie ZIM failo formatą ir API, kurios gali kurti ir atidaryti ZIM failus.",
  "linktitle": "ZIM",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-zi-ltm"
}
},
  "lastmod": "2019-12-09"
}

## Kas yra ZIM failas? ##

Failai su plėtiniu .zim yra archyvai, sukurti Wiki turiniui saugoti neprisijungus. Jis laikomas tinkamiausiu atviro failo formatu Vikipedijai saugoti USB atmintinėje. Jis saugo svetainės turinį kompaktišku formatu. Jo pavadinimas kilęs iš Zeno Improved, kuris buvo ankstesnis Zeno failo formatas. ZIM palaiko [openZIM ](https://openzim.org/)projektas, kurį remia Wikimedia CH ir remia Wikimedia Foundation. ZIM failus galima atidaryti tokiomis programomis kaip Kiwix ir ZIMReader. OpenZIM projektas priglobė ZIM failo formato diegimą [Github](https://github.com/openzim), kad prisidėtų prie atvirojo kodo bendruomenės.

## ZIM failo formato specifikacijos

ZIM failo formatas buvo sukurtas naudojant [Zeno file format](https://openzim.org/wiki/Zeno_file_format) ir nėra suderinamas atgal. ZIM failo formato formato specifikacijos yra [available online](https://openzim.org/wiki/ZIM_file_format), skirtos openZIM kūrėjui. OpenZIM suteikė C++ atvirojo kodo diegimą [LibZim](https://openzim.org/wiki/Zimlib), skirtą ZIM failams skaityti ir rašyti.

ZIM failo formatas naudoja LZMA2 glaudinimą, kad turinys būtų kompaktiškas.

{{< figure src="../ZIM_File_Format.jpeg" alt="ZIM failo formatas" >}}


### ZIM antraštė

A ZIM file starts with a header that is at offset 0. Visos sudedamosios dalys yra pagrįstos little-endian ir visi sveikieji skaičiai yra beženkliai sveikieji skaičiai, ty uint_16, uint_32, uint_64.

|Lauko pavadinimas |Tipas| Offset| Ilgis| Aprašymas|
---|---|---|---|---|
|magicNumber| sveikasis skaičius| 0| 4| Stebuklingas skaičius, kad atpažintų failo formatą, turi būti 72173914 (0x44D495A)|
|pagrindinė versija| sveikasis skaičius| 4| 2| Pagrindinė ZIM failo formato versija (5 arba 6)|
|minorVersion| sveikasis skaičius| 6| 2| Nedidelė ZIM failo formato versija|
|uuid| sveikasis skaičius| 8| 16| unikalus šio zim failo ID|
|straipsnių skaičius| sveikasis skaičius| 24| 4| bendras straipsnių skaičius|
|clusterCount| sveikasis skaičius| 28| 4| bendras klasterių skaičius|
|urlPtrPos| sveikasis skaičius| 32| 8| katalogo rodyklių sąrašo padėtis, išdėstyta pagal URL|
|titlePtrPos| sveikasis skaičius| 40| 8| katalogo rodyklių sąrašo padėtis pagal Title|
|klasterisPtrPos| sveikasis skaičius| 48| 8| klasterio rodyklės sąrašo padėtis|
|mimeListPos| sveikasis skaičius| 56| 8| MIME tipų sąrašo padėtis (taip pat antraštės dydis)|
|pagrindinis puslapis| sveikasis skaičius| 64| 4| pagrindinis puslapis arba 0xffffffff, jei nėra pagrindinio puslapio|
|išdėstymasPuslapis| sveikasis skaičius| 68| 4| išdėstymo puslapis arba 0xffffffffff, jei nėra maketo puslapio|
|checksumPos| sveikasis skaičius| 72| 8| nukreipkite žymiklį į šio failo md5checksum be pačios kontrolinės sumos. Tai visada nurodo 16 baitų prieš failo pabaigą.|

## Nuorodos Nr.

* [OpenZIM](https://openzim.org/)

* [C++ LibZim](https://openzim.org/wiki/Zimlib)


