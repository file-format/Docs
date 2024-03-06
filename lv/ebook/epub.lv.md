{
  "date": "2019-12-12",
  "keywords": [
"EPUB",
"failu",
"pagarinājumu",
"formātā",
"E-grāmata",
"Digitālā grāmata"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par EPUB failu formātu un API, kas var izveidot un atvērt EPUB failus.",
  "title": "Kas ir EPUB fails?",
  "linktitle": "EPUB",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-epu-lvb"
}
},
  "lastmod": "2019-12-12"
}

## Kas ir EPUB fails?

Faili ar paplašinājumu .epub ir e-grāmatu failu formāts, kas nodrošina standarta digitālās publikācijas formātu izdevējiem un patērētājiem. Formāts līdz šim ir bijis tik izplatīts, ka to atbalsta daudzi e-lasītāji un programmatūras lietojumprogrammas. Piemēram, operētājsistēmā Mac OS iepriekš instalētā **Books** programmatūra nodrošina atbalstu šādu failu atvēršanai. Turklāt viedtālruņiem, planšetdatoriem un datoriem ir pieejama daudz saderīgas programmatūras. EPUB failu standartus uztur [International Digital Publishing Forum](https://idpf.org/epub/30/spec/epub30-publications.html)(IDPF). EPUB 3 versiju ir apstiprinājusi arī Grāmatu nozares izpētes grupa (BISG), kas ir vadošā grāmatu tirdzniecības asociācija standartizētai paraugpraksei, izpētei, informācijai un pasākumiem satura iesaiņošanai.

## Īsa EPUB faila formāta vēsture

* **2007. gada oktobris** — tika apstiprināts EPUB 2.0

* **2010. gada septembris** — tika izlaists apkopes atjauninājums

* **2011. gada oktobris** — stājās spēkā EPUB 3.0 specifikācijas

* **2014. gada jūnijs** — tika izlaists neliels apkopes atjauninājums, lai aizstātu 3.0 versiju.

* **2017. gada janvāris** — stājās spēkā EPUB 3.1


## EPUB faila formāts

EPUB faila formāts ir arhīvs, kuru var pārdēvēt par paplašinājumu [ZIP](/compression/zip/), un tā saturu var skatīt, izvelkot arhīvu ar jebkuru arhīva ekstraktoru. Tas ir atvērts uz XML balstīts formāts, un tas sastāv no HTML failiem, attēliem, CSS stila lapām un citiem elementiem. To var arī pārvērst PDF, Mobi un vairākos citos failu formātos, izmantojot vairākas programmatūras lietojumprogrammas un API.

{{< figure src="../epub.png" alt="EPUB faila formāts" >}}

**EPUB e-grāmata atvērta, izmantojot Mac OS grāmatu lietojumprogrammu**

EPUB faila formāts ir balstīts uz šādiem trīs atvērtiem standartiem.

### Atvērtā publiskā struktūra (OPS) ###

EPUB 2.0 fails izmanto XHTML 1.1, lai izveidotu publikācijas saturu. Būtībā tas nozīmē, ka EPUB fails sastāv no vienas vai vairākām tīmekļa lapām. Pat ja jūs varētu iekļaut visu grāmatas vai laikraksta saturu vienā lapā, labāk, lai šāds fails nepārsniegtu 300 K gan veiktspējas, gan saderības apsvērumu dēļ. Tāpat kā parastajām tīmekļa lapām, stils un izkārtojums tiek definēts, izmantojot kaskādes stila lapas (CSS). EPUB failos ir jāizmanto CSS2 apakškopa (ierobežota komandu sērija). Daudzas no jaunajām CSS3 funkcijām, piemēram, noapaļotās kastes vai krītošās ēnas, vēl nav pieejamas. Lai nodrošinātu atpakaļejošu saderību, satura kodēšanai satura veidotājs var izmantot arī DTBook, nevis XHTML.

### Atvērtais iepakojuma formāts (OPF) ###

Šī specifikāciju daļa attiecas uz strukturālu informāciju, piemēram, metadatiem (kas ir autors un izdevējs, kāds ir nosaukums, ..), manifestu (visu epub failā esošo failu saraksts) un satura rādītāju. Visi šie dati ir iegulti, izmantojot XML.

### Atvērt konteinera formātu (OCF) ###

As the above descriptions should have made it clear an EPUB document consists of a series of files. The OCF specs define how all those files end up being packaged in one single container file. ZIP compression is used for this.

## Atbalstītie attēlu failu formāti ##

EPUB faila formāts atbalsta šādus attēla failu formātus.

* [GIF](/image/gif/)

* [JPG](/image/jpeg/)

* [PNG](/image/png/)

* [SVG](/page-description-language/svg/)

## Atsauces Nr.

* [EPUB — Wikipedia](https://en.wikipedia.org/wiki/EPUB)


