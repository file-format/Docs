{
  "date": "2019-10-11",
  "keywords": [
"ico fails",
"ico faila formāts",
"kas ir ico fails",
"failu",
"ico piemērs",
"ico faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ICO — attēla faila formāts",
  "description": "Uzziniet par ICO failu formātu un API, kas var izveidot un atvērt ICO failus.",
  "linktitle": "ICO",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-ic-lvo"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir ICO fails?

Faili ar ICO paplašinājumu ir attēlu failu tipi, kas tiek izmantoti kā ikona lietojumprogrammas attēlošanai vietnē [Microsoft Windows](https://www.microsoft.com/en-us/windows). Tiem ir dažādi izmēri, krāsu atbalsts un izšķirtspēja, lai tie atbilstu displeja prasībām. Vēl viens līdzīgs attēla faila formāts operētājsistēmā Microsoft Windows ir [CUR](/image/cur/) kursora attēlošanai un definē tīklāju attēla galvenē. Operētājsistēmā MacOS ICNS failu formāti kalpo tam pašam mērķim kā ICO faili. Vairākas tiešsaistes vietnes, kā arī lietojumprogrammas nodrošina iespēju izveidot šādus failus un konvertēt citus attēlu formātus, piemēram, [BMP](/image/bmp/), [PNG](/image/png/) utt., ikonu faila formātā. Oficiālais IANA reģistrētais interneta multivides veids ICO failiem ir image/vnd.microsoft.icon.

## Īsa vēsture ##

Icons were introduced with the launch of Microsoft Windows 1.0. Tie bija 32x32 lieli un vienkrāsaini. Līdz ar win32 ienākšanu tika ieviests atbalsts ikonu attēliem īstās krāsās ar izmēru līdz 256x256 pikseļiem. Windows XP bija pirmā, kas nodrošināja atbalstu 32 bitu krāsu ikonu attēliem, ļaujot ikonai pievienot daļēji caurspīdīgus apgabalus, piemēram, ēnas, pretizlīdzināšanu un stikla efektus. Microsoft ieteica tikai ikonu izmērus līdz 48 × 48 pikseļiem operētājsistēmai Windows XP. Windows Vista programmai Windows Explorer pievienoja 256 × 256 pikseļu ikonu skatu, kā arī saspiestā [PNG](/image/png/) formāta atbalstu. Ja lietotāji izmanto augstāku izšķirtspēju un augstus DPI režīmus, ieteicams izmantot lielākus ikonu formātus (piemēram, 256 × 256).

## ICO faila formāts ##

Viens ICO fails sastāv no viena vai vairākiem maziem dažādu izmēru un krāsu dziļuma attēliem. Vairāku izmēru attēlu klātbūtne ir paredzēta atbilstošai mērogošanai dažādās ekrāna izšķirtspējās. Visas vērtības ICO/CUR failos ir attēlotas [little-endian](https://en.wikipedia.org/wiki/Little-endian) baitu secībā.

ICO fails sastāv no ikonas galvenes, ikonu direktorija,

|Lauks|Apraksts
---|---|
|Icon Header|Saglabā vispārīgu informāciju par ICO failu.
|Directory[1..n]|Saglabā vispārīgu informāciju par katru failu failā.
|Icon #1|Faktiskie dati pirmajam attēlam vecā AND/XOR DIB formātā vai jaunākā PNG formātā
|...|
|Ikona #n|Pēdējā ikonas attēla dati

### Virsraksts ###

|Nobīde|Izmērs (baitos)|Mērķis
---|---|---|
|0|2|Rezervēts. Vienmēr jābūt 0.
|2|2|Norāda attēla veidu: 1 ikonas (.ICO) attēlam, 2 kursora (.CUR) attēlam. Citas vērtības nav derīgas.
|4|2|Norāda attēlu skaitu failā.

### Katalogs ###

ICO failā esošais direktorijs, kas attēlots kā ICONDIR struktūra, satur ICONDIRECTORY struktūru katram faila attēlam. Pēc tam seko visu attēla bitkartes datu blakus bloks. Tas ir kā parādīts zemāk.

|Nobīde|Izmērs|Apraksts
---|---|---|
|0 (0)|1|Platumam jābūt 0, ja 256 pikseļi
|1 (1)|1|Augstums, ir jābūt 0, ja 256 pikseļi
|2 (2)|1|Krāsu skaitam jābūt 0, ja ir vairāk nekā 256 krāsas
|3 (3)|1|Rezervēts, jābūt 0
|4 (4)|2|Krāsu plaknēm .ICO formātā jābūt 0 vai 1, vai X tīklājam, ja formātā .CUR
|6 (6)|2|Biti pikselī, ja tas ir .ICO formātā, vai Y tīklājs, ja tas ir .CUR formātā
|8 (8)|4|Bitkartes datu lielums baitos.
|12 (C)|4|Nobīde failā.

## Atsauces Nr.

* [ICO — Wikipedia](https://en.wikipedia.org/wiki/ICO_(file_format))

* [IANA — vnd.microsoft.icon](http://www.iana.org/assignments/media-types/image/vnd.microsoft.icon)


