{
  "date": "2019-10-11",
  "keywords": [
"psb failą",
"psb failo formatas",
"kas yra psb failas",
"failą",
"psb pavyzdys",
"psb failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PSB – „Photoshop“ didelio vaizdo failo formatas",
  "description": "Sužinokite apie PSB failų formatą ir API, kurios gali kurti ir atidaryti PSB failus.",
  "linktitle": "PSB",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-ps-ltb"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra PSB failas?
Adobe Photoshop išsaugo failus dviem formatais. Failai, kurių dydis yra 30 000 x 30 000 pikselių, išsaugomi naudojant PSD plėtinį, o didesni nei PSD failai iki 300 000 x 300 000 pikselių išsaugomi naudojant PSB plėtinį, žinomą kaip Photoshop Big. Tiksliau, PSB failai gali būti 4 EB (daugiau nei 4,2 milijardo GB) dydžio, o vaizdai, kurių aukštis ir plotis yra iki 300 000 pikselių. Kita vertus, PSD gali būti iki 2 GB, o vaizdo matmenys – 30 000 pikselių.

PSB is also known as large format size for photoshop and supports all the photoshop features like layers, effects and filters.Photoshop can convert PSB file to [PSD](/image/psd/), [JPG](/image/jpeg/), [PNG](/image/png/), [EPS](/page-description-language/eps/), [GIF](/image/gif/) and other formats as well. Photoshop large document format is available once the feature of file handling pane of Photoshop’s preferences dialog box is enabled.

## Informacija apie failo formatą ##

Photoshop failo formatas yra padalintas į penkias pagrindines dalis su daugybe ilgio žymeklių, kad galėtumėte judėti tarp skyrių.

|Failo formatas
---|
|Failo antraštė
|Spalvų režimo duomenys
| Vaizdo ištekliai
|Sluoksnio ir kaukės informacija
|(((
Vaizdo duomenys
)))

### Failo antraštė ###

Failo antraštė turi fiksuotą 26 baitų ilgį ir apima pagrindines vaizdo savybes.

BYTE parašas [4] – lygus '8BPS'.

WORD versija [2] – versijos numeris, PSD # 1, PSB # 2.

BYTE Rezervuotas [6] – rezervuotas ir visada nulis.

WORD kanalai [2] – spalvų kanalų skaičius vaizde, įskaitant alfa kanalus. Jo vertė svyruoja nuo 1 iki 56.

LONG Rows [4] – vaizdo aukštis pikseliais, 1–30 000 PSD, 1–300 000 PSB.

LONG Columns [4] – vaizdo plotis pikseliais, 1-30 000 PSD, 1-300 000 PSB.

WORD Depth [2] – bitų skaičius kanale. Palaikomos reikšmės yra 1, 8, 16 ir 32.

WORD Mode [2] – failo spalvų režimas.

#### Režimo aprašymas ####


|Režimas|Aprašymas
---|---|
|0|Bitmap (vienspalvis)
|1|Pilkos spalvos
|2|Indeksuotas
|3|RGB
|4|CMYK
|7|Daugelis kanalų
|8|Duotonas (pustonis)
|9|Labor

### Spalvų režimo duomenys ###

Po failo antraštės seka spalvų režimo duomenų skyrius. Blokas prasideda LONG numeriu, kuris nurodo bloko ilgį baitais. Spalvų režimo duomenų struktūra yra tokia:

4 baitai – šių spalvų duomenų ilgis.

Kintamasis – spalvos duomenys

Jei režimo lauko reikšmė antraštės skiltyje nėra indeksuota spalva arba dvitonė, bloko ilgis bus 0 ir po ilgio lauko duomenų nebus.

Indeksuotų spalvotų vaizdų ilgis bus 768 baitai, kuriuose bus 256 spalvų paletė. Dviejų tonų duomenyse bus ekrano parametrai ir kita susijusi informacija.

### Vaizdo ištekliai ###

Po spalvų režimo duomenų skyriaus trečiasis blokas yra vaizdo išteklių skyrius. Pirmieji keturi baitai yra LONG skaičius, nurodantis bloko ilgį, po kurio seka išteklių blokų serija. Vaizdo išteklių bloko struktūra yra tokia:

BYTE tipas [4] – parašas 8BIM

WORD ID [2] – vaizdo šaltinio ID. Yra išteklių ID sąrašas, kurį galima pamatyti iš nuorodos.

BAITŲ pavadinimas [kintamasis] – pavadinimas: vienodo ilgio Pascal eilutė. ***

LONG Size [4] – faktinis toliau pateikiamų išteklių duomenų dydis.

BAITŲ duomenys [kintamasis} – išteklių duomenys. Jis yra paminkštintas, kad būtų vienodo dydžio.

Kai kurie išteklių formatai trumpai paaiškinti toliau:

**Tinklelio ir vadovų išteklių formatas:** Tinklelio ir vadovų informacija saugoma išteklių bloke. Šiuose išteklių blokuose yra 16 baitų tinklelis ir vadovo antraštė, po kurio seka 5 baitų kreipiamosios informacijos blokai.

**Miniatūros išteklių formatas:** Miniatiūros informacija saugoma vaizdo išteklių bloke, kad būtų galima peržiūrėti peržiūrą, kurią sudaro 28 baitų antraštė ir JFIF miniatiūra RGB formatu.

**Spalvų mėginių rinktuvų išteklių formatas:** Spalvų pavyzdžių informacija saugoma vaizdo išteklių bloke su 8 baitų antrašte ir kintamo ilgio spalvų mėginių informacijos bloku.

### Informacija apie sluoksnį ir kaukę ###

Ketvirtasis blokas yra sluoksnių ir kaukių informacijos blokas, kuriame yra informacija apie sluoksnius ir kaukes. Pirmiausia išsaugoma sluoksnio informacija, o tada maskuojama.

**Sluoksnio informacija:** sluoksnio informacija prasideda LONG reikšme, kuri rodo sluoksnio informacijos ilgį. Po to yra WORD reikšmių skaičius, rodantis sektinų sluoksnių įrašų skaičių.

[8] – sluoksnių ilgis

[2] – Sluoksnių skaičius

[Kintamasis] – informacija apie kiekvieną sluoksnį.

[Kintamas] – kanalo vaizdo duomenys.** **

**Kaukės informacija:** Kaukės struktūra yra tokio formato:


|Duomenų struktūra|Lauko pavadinimas| apibūdinimas
---|---|---|
|ŽODŽIS| Perdangos spalvų erdvė| (Nedokumentuota)
|BAITAS[8]| Spalvos komponentai| 4x2 baitų spalvų komponentai
|ŽODŽIS| Neskaidrumas| 0#skaidrus, 1#nepermatomas
|BAITAS| Malonus| 0#apversta, 1#apsaugota, 128#naudokite išsaugotą vertę
|BAITAS| pamušalas| nustatyti į nulį

### Vaizdo duomenys ###

Paskutiniame skyriuje yra vaizdo pikselių duomenys. Vaizdo duomenys saugomi kaip seka plokštumose, ty pirmiausia visi raudoni duomenys, tada visi žali duomenys ir tt WORD kiekvienos eilutės pradžioje rodo dydį baitais, susijusį su kiekviena nuskaitymo eilute.

[2] – Suspaudimo metodas:

[Kintamas] – vaizdo duomenys plokštumoje, pvz., RRRR, GGGG, BBBB ir kt.

Suspaudimo būdai:

0 – Raw Vaizdo duomenys

1 – RLE suspaustas

2 – užtrauktukas be numatymo

3 – užtrauktukas su numatymu

## Nuoroda ##

* [PSB failo formatas – pateikė „Adobe“](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)

* [PSB – Vikipedija](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)


