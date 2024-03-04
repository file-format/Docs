{
  "date": "2019-10-11",
  "keywords": [
"dng failą",
"dng failo formatas",
"kas yra dng failas",
"failą",
"dng pavyzdys",
"dng failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DNG – skaitmeninio fotoaparato vaizdo failo formatas",
  "description": "Sužinokite apie DNG failo formatą ir API, kurios gali kurti ir atidaryti DNG failus.",
  "linktitle": "DNG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-dn-ltg"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra DNG failas?

DNG is a digital camera image format used for the storage of raw files. It has been developed by Adobe in September 2004. Iš esmės jis buvo sukurtas skaitmeninei fotografijai. DNG yra [TIFF](/image/tiff/)/EP standartinio formato plėtinys ir daug naudoja metaduomenis. Norėdami lengvai lanksčiai ir meniškai valdyti neapdorotus skaitmeninių fotoaparatų duomenis, fotografai pasirenka neapdorotus fotoaparato failus. JPEG ir TIFF formatuose saugomi fotoaparato apdorojami vaizdai, todėl tokiuose formatuose nėra daug vietos keisti.

## DNG failo formato istorija ir versijos

Till now there have been 5 versions of DNG specification so far. Version 1.0.0.0 was launched in September 2004 along with the release of "2.3" (ACR and DNG Converter). In February 2005 version 1.1.0.0 was published.  In May 2008 version 1.2.0.0 was released and was used in "4.4". Version 1.3.0.0 was published in June 2009. 1.4.0.0 versija pasirodė 2012 m.

## DNG failo formatas

Tuo tarpu fotoaparato neapdoroti failai fiksuoja neapdorotus arba mažai apdorotus duomenis tiesiai iš jutiklio. Kadangi jie yra panašūs į filmų negatyvus, neapdoroti fotoaparato formatai taip pat žinomi kaip skaitmeniniai negatyvai. Neapdorotų formatų pranašumas yra didesnė galutinio vartotojo meninė kontrolė. Vartotojas gali reguliuoti įvairius parametrų diapazonus pagal reikalavimus, tokius kaip baltos spalvos balansas, tonų atvaizdavimas, triukšmo mažinimas, ryškinimas ir pan. Kita vertus, fotoaparato neapdorotas failas turi būti apdorotas bet kokiam naudojimui naudojant bet kokią programinę įrangą arba per keitiklį.

Kadangi nebuvo standartinio fotoaparato neapdorotų failų formato, galutiniam vartotojui kilo daug problemų. Šias problemas išsprendė Adobe ir nustatė nepatentuotą fotoaparato neapdorotų failų formatą. Formatas žinomas kaip Digital Negative arba DNG. DNG gali būti naudojamas įvairioje aparatinėje ir programinėje įrangoje neapdorotiems failams apdoroti. Be to, DNG taip pat gali būti naudojamas kaip tarpinis formatas vaizdams, kurie iš pradžių buvo užfiksuoti fotoaparatu, turinčiu savo patentuotus neapdorotus formatus, saugoti.

### DNG failo formato specifikacijos

Šiame skyriuje apibūdinsime DNG formatą kaip TIFF 6.0 plėtinį.

* **Failo plėtiniai**: DNG naudoja plėtinius „.DNG“ arba „.TIF“.

* **SubIFD medžiai**: DNG nepalaiko SubIFD grandinių, vietoj to DNG rekomenduoja naudoti SubIFD medžius, kaip nurodyta TIFF-EP specifikacijose. Aukščiausiai kokybei ir skyrai gali būti naudojamas NewSubFileType 0, o žemesnės kokybės miniatiūrose NewSubFileType turėtų būti lygi 1. Taip pat rekomenduojama, nors ir nebūtina, kad pirmasis IFD būtų žemos kokybės arba raiškos miniatiūra.

* **Baitų tvarka**: baitų tvarką turi palaikyti DNG skaitytuvai, taip pat ir failams iš konkretaus fotoaparato modelio.

* **Maskuoti pikseliai**: dauguma fotoaparato jutiklių apskaičiuoja visiškai užmaskuotus pikselius jutiklio krašte naudodami juodą kodavimą. Šie pikseliai gali būti įtraukti arba apkarpyti prieš išsaugant vaizdą DNG formatu. Jei užmaskuoti pikseliai nėra apkarpyti, šių pikselių plotas turi būti nurodytas ActiveArea žymoje. Informacija, surinkta iš šių pikselių apie juodos spalvos kodavimo lygį, turėtų būti naudojama prieš išsaugant neapdorotus duomenis arba gali būti įtraukta į DNG failą, nurodant juodos spalvos lygį.

* **Defektuoti pikseliai**: prieš išsaugant neapdorotus duomenis kaip DNG, defektiniai pikseliai turėtų būti neįtraukti.

* **Metaduomenys**: metaduomenys gali būti įtraukti į DNG bet kuriuo iš šių būdų:  

** Naudojant TIFF-EP arba EXIF metaduomenų žymas
** Per IPTC metaduomenų žymą (33723)
** Naudojant XMP metaduomenų žymą (700)
* **Patentuoti duomenys**: paprastai pardavėjai į neapdorotą failą įtraukia nuosavybės teise priklausančius duomenis, kuriuos naudos jų pačių konverteriai. DNG saugo savo patentuotus duomenis privačiose žymose, privačiuose IFD ir privačioje MakerNote. Pardavėjai turi naudoti DNGPrivateData ir MakerNoteSafety žymas, kad įsitikintų, jog DNG failus redaguojančios programos išsaugo šiuos nuosavybės duomenis.


Toliau pateikiami keli svarbūs TIFF žymų apribojimai ir plėtiniai.

**BitsPerSample**

Palaikomi nuo 8 iki 32 bitų/pavyzdžiui. Kiekvieno mėginio gylis turi būti toks pat, kai SamplesPerPixel nėra lygus 1. Bet jei BitsPerSample nėra lygus 8, 16 ar 32, bitai turi būti supakuoti į baitus, naudojant TIFF numatytąjį FillOrder 1 (big-endian).

**Suspaudimas**

Palaikomos dvi suspaudimo žymų reikšmės:

* 1 reikšmė: nesuspausti duomenys.

* Vertė Nr. 7: JPEG suspausti duomenys, bazinis DCT JPEG arba be nuostolių JPEG glaudinimas.


**Fotometrinis aiškinimas**

Šios reikšmės palaikomos tik miniatiūroms ir peržiūros IFD:

* 1 = BlackIsZero. Manoma, kad yra gama 2.2 spalvų erdvėje.

* 2 = RGB. Manoma, kad yra sRGB spalvų erdvėje.

* 6 = YCbCr. Naudojamas JPEG koduotiems peržiūros vaizdams.


Šios neapdoroto IFD reikšmės palaikomos ir laikomos natūralia fotoaparato spalvų erdve:

* 32803 # CFA (spalvų filtrų masyvas).

* 34892 # LinearRaw.


**Orientacija**

Orientacinė žyma naudojama failų naršyklėms, kad jos galėtų be nuostolių sukti DNG failus. DNG skaitytuvai turi palaikyti visas įmanomas orientacijas, įskaitant veidrodines orientacijas.

## Naujausios DNG versijos funkcijos

DNG 1.4 versija 2012 m. spalio mėn. turi šias išplėstines funkcijas.

* Numatytasis vartotojo apkarpymas

* Skaidrumas

* Slankaus kablelio (HDR)

* Prarasta kompresija

* Įgaliotieji serveriai


## Nuorodos Nr.

* [DNG specifikacijos – pateikė „Adobe“](https://web.archive.org/web/20170829200857/http://wwwimages.adobe.com/content/dam/Adobe/en/products/photoshop/pdfs/dng_spec_1.4.0 .0.pdf)

* [Skaitmeninis neigiamas elementas – Vikipedija](https://en.wikipedia.org/wiki/Digital_Negative)

* [DNG – viešas archyvinis skaitmeninių fotoaparatų neapdorotų duomenų formatas](https://helpx.adobe.com/camera-raw/digital-negative.html)


