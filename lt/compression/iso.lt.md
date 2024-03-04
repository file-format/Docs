{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ISO – disko vaizdo failo formatas",
  "description":"Kas yra ISO failas ir API, kurie gali kurti ir atidaryti ISO failus.",
  "linktitle" : "ISO",
  "menu" : {
    "docs" : {
     "identifier": "compression-iso-lt",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Kas yra ISO failas?

Failas su plėtiniu .iso yra nesuspaustas archyvo disko vaizdo failas, vaizduojantis visų duomenų turinį optiniame diske, pvz., CD arba DVD. Remiantis standartu [ISO-9660](https://www.iso.org/standard/17505.html), ISO vaizdo failo formate yra disko duomenys kartu su jame saugoma failų sistemos informacija. Dėl ISO failų galimybės turėti tikslią turinio kopiją tai yra puikus failo tipas CD / DVD kopijoms kurti ir dažniausiai naudojamas įkrovos duomenims saugoti, kad būtų galima įdiegti. Dažniausiai ISO failai įrašomi į USB / CD / DVD kaip įkrovos turinys, kad būtų galima paleisti įrenginį ir įdiegti. ISO failai turi MIME tipo programą / x-iso9660-image.

## ISO failo formatas

ISO failo formatas nepanašus į kitus konteinerio failų formatus, nors jis archyvuoja nurodytą duomenų turinį. Archyvas sukuriamas kaip dvejetainis failas su tikslia turinio struktūra ir failų sistemos informacija. ISO failo formatas aprašytas [ISO-9660](https://en.wikipedia.org/wiki/ISO_9660) taip.

### Aukščiausio lygio ISO failo struktūra

Bendra failo struktūra susideda iš:

 * Sistemos sritis – 32 768 baitai ir nenaudojama pagal ISO_9660
 * Duomenų sritis – susideda iš apimties deskriptorių rinkinio ir kelio lentelių, katalogų ir failų

### Tomo deskriptorių rinkinys

Duomenų sritis prasideda apimties deskriptorių rinkiniu, vieno ar daugiau apimties deskriptorių rinkiniu, kuris baigiamas apimties deskriptorių rinkinio terminatoriumi. Jie kartu veikia kaip duomenų srities antraštė, aprašanti jos turinį (panašiai į BIOS parametrų bloką, naudojamą FAT, HPFS ir NTFS formatuotų diskų).

Apimties deskriptorių rinkinys yra toks, kaip parodyta toliau.

|Tūrio deskriptorių rinkinys|
---|
|Tūrio aprašas #1|
|...|
|Tūrio aprašas #N|
|Tūrio deskriptorių rinkinio terminatorius|

#### Tomo aprašas

Kiekvienas tomo deskriptorius yra 2048 baitų dydžio ir turi tokią struktūrą:

|Dalis |Tipas |Identifikatorius |Versija |Duomenys|
---|---|---|---|---|
|Dydis |1 baitas |5 baitai (visada 'CD001') |1 baitas (visada 0x01) |2 041 baitas|

## Nuorodos

* [Optinio disko vaizdas – Vikipedija](https://en.wikipedia.org/wiki/Optical_disc_image)

* [Failo parašai](https://www.garykessler.net/library/file_sigs.html)

* [ISO 9660 – Vikipedija](https://en.wikipedia.org/wiki/ISO_9660)


