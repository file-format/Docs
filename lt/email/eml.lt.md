{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EML – el. pašto žinutė",
  "description": "Sužinokite apie EML failo formatą ir API, kurios gali kurti ir atidaryti EML failus.",
  "linktitle": "EML",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-em-ltl"
}
},
  "lastmod": "2019-09-16"
}

## Kas yra EML failas?

EML failo formatas reiškia el. pašto pranešimus, išsaugotus naudojant Outlook ir kitas susijusias programas. Beveik visos el. pašto programos palaiko šį failo formatą, kad jis atitiktų RFC-822 interneto pranešimų formato standartą. Microsoft Outlook yra numatytoji programinė įranga, skirta atidaryti EML pranešimų tipus. EML failus galima įrašyti į diską ir išsiųsti gavėjams naudojant ryšio protokolus.

## Trumpa EML istorija

EML failo formato specifikacijos pateikiamos pagal [RFC 822](https://www.ietf.org/rfc/rfc0822.txt) standartinį formatą. Prieš RFC-822, RFC-733 valdė tinklo pranešimų mainų taisykles iki 1982 m., pirmasis buvo sukurtas kaip šoninio patobulinimas, nustatant ARPA standartus. Tuo pačiu metu Microsoft sukūrė savo COM modulius savo el. pašto programai, ty Outlook Express, kurti. RFC-822 buvo sukurtas kaip patentuotas formatas, kai Microsoft nukrypo nuo atvirojo standarto ir sukūrė [PST](/email/pst/) failo formatą, kuriame el. laiškai išsaugomi labai struktūrizuotu duomenų bazės formatu. Dėl to ne Microsoft el. pašto programų naudotojams kilo problemų, kai el. laiškai buvo persiunčiami iš Microsoft Outlook.

Tai buvo 2001 m., kai 822 standartas buvo patobulintas iki 2822 – interneto pranešimų formato, kuris šiuo metu naudojamas kuriant, nuskaitant ir siunčiant EML pranešimus MIME RFC-822 formatu.

## EML failo formato specifikacijos

EML failus sudaro dvi atskiros dalys:

* **Antraštės** – yra informacijos apie pranešimo antraštę

* **Pranešimo turinys** – yra informacijos, kuri gali apimti pranešimo turinį, įterptus vaizdus ir priedus


### Antraštės informacija ###

EML failą sudaro antraščių informacija ir, pasirinktinai, pranešimo turinys. Kiekvieną EML antraštės eilutę sudaro dvi dalys, atskirtos dvitaškiu :. Pirmasis vadinamas antraštės pavadinimu, o kitas po dvitaškis yra antraštės tekstas. Pavyzdžiui, tokios antraštės apima:

* Siuntėjo el. pašto adresas

* Gavėjo el. pašto adresas

* El. pašto tema

* Pranešimo laiko ir datos antspaudas


**Antraštės pavyzdys**

```
From: <John@bmw.eml.light.com>

To: <Andy@fileformat.com>

Date: Thu, 8 Mar 2018 10:43:37 +0100

Subject: bmw eml light
```

### Pranešimo tekstas ###

EML pranešimo korpuse yra pagrindinė el. pašto informacija teksto, hipersaitų ir priedų pavidalu. El. laiško tekste gali būti paprasto skaitomo teksto, bet tai nėra būtina. Tokiu atveju pranešimo tekstas gali būti tuščias arba jame gali būti užkoduotų priedų duomenų.

Pranešimo turinys apibūdinamas jo turinio tipu, kuris leidžia skaitymo programoms skaityti informaciją atitinkamais formatais. Tai iš tikrųjų atspindi dokumento pobūdį ir formatą. MIME tipo arba turinio tipo struktūra yra labai paprasta; jį sudaro tipas ir potipis, dvi eilutės, atskirtos /. Neleidžiama vietos. Tipas nurodo kategoriją ir gali būti atskiras arba kelių dalių tipas. Potipis yra būdingas kiekvienam tipui. Tipų, patenkančių į turinio tipo kategoriją, sąrašas yra ilgas, tačiau kai kurie svarbūs turinio tipai yra tokie:


|**Tipas**|**Aprašymas**|**Potipų pavyzdys**
---|---|---|
|text|Nurodo formatą, kuris yra skaitomas žmogui|tekstas/paprastas, tekstas/html, tekstas/css, tekstas/javascript
|image|Nurodo bet kokio tipo vaizdą, išskyrus vaizdo įrašus|vaizdas/bmp, vaizdas/png, vaizdas/jpg, vaizdas/gif
|audio|Nurodo bet kokį garso failo formatą|audio/mdi, audio/wav
|application|Nurodo bet kokius dvejetainius duomenis|application/octet-stream, application/vnd.mspowerpoint, application/xhtml+xml, application/xml, application/pdf

### Prisirišimo vaizdavimas EML korpuse

EML korpuse yra kiekvieno jame esančio turinio tipo ribos. Priedas pranešimo tekste identifikuojamas pagal jo turinio tipą ir turinio išdėstymą, kaip parodyta šiame pavyzdyje:

Turinio tipas: tekstas/paprastas; simbolių rinkinys #langai-1252; pavadinimas#Apple App Store.txt
Turinys-Dispozicija: prisirišimas; failo pavadinimas#Apple App Store.txt
Turinio perdavimas-kodavimas: base64
X-Attachment-Id: f_jkhztmd02

Kaip matote, turinio išdėstymas, nustatytas prie priedo, leidžia nuskaityti programas, kad gautų priedo informaciją, pvz., priedo failo pavadinimą ir perdavimo kodavimą. Po priedo antraštės informacijos pateikiamas užkoduotas priedo turinys, kurį reikia perskaityti.

#### Skaičiuoklės kaip priedo pavyzdys

Turinio tipas: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet; pavadinimas#anglų_spodr.xlsx
Turinys-Dispozicija: prisirišimas; failo pavadinimas#english_spodr.xlsx
Turinio perdavimas-kodavimas: base64
X-Attachment-ID: f_jkhztmd43

## Kaip atidaryti EML failą

EML failus galite atidaryti naudodami įvairias el. pašto programas, tokias kaip:

 * **Apple Mail sistemoje macOS**
 * **Mozilla Thunderbird**
 * **Microsoft Outlook**

EML failai išsaugomi paprasto teksto formatu, o šiuos EML failus taip pat galite atidaryti naudodami populiarias teksto rengykles, tokias kaip **TextEdit** MacOS ir **Microsoft Notepad** Windows OS.

## Kaip konvertuoti EML failą

Galite konvertuoti EML failus į kelis kitus formatus naudodami tokias programas kaip Apple Mail ir Microsoft Outlook.

Pavyzdžiui, Microsoft Outlook gali konvertuoti EML failą į šiuos formatus:

**[.MSG](/eml/msg/)** – Microsoft Outlook pranešimo formatas
**[.PDF](/pdf/)** – Protable dokumento formatas

## Nuorodos

* [RFC 822](https://www.ietf.org/rfc/rfc0822.txt)


