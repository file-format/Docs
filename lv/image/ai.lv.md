{
  "date": "2021-01-21",
  "keywords": [
"ai fails",
"ai faila formātā",
"kas ir ai fails",
"failu",
"ai piemērs",
"ai faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "AI — Adobe Illustrator mākslas darbu fails",
  "description": "Uzziniet par AI failu formātu un API, kas var izveidot un atvērt AI failus.",
  "linktitle": "AI",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-a-lvi"
}
},
  "lastmod": "2021-01-21"
}

## Kas ir AI fails?

A file with an .ai extension is an Adobe Illustrator Artwork file that contains vector graphics in a single page. it uses points to create paths for displaying the image data, thus making it safe from losing image quality if it is enlarged. AI file format is base don the PGF file format which are similar to AI files. AI format finds its major usage for logos and print media, and its initial versions were considered similar to that of [EPS](/page-description-language/eps/) files. AI files can be opened with Adobe Illustrator, Adobe Acrobat DC, PaintShop Pro, and CorelDraw Graphics tools.

## AI faila formāts

AI ir Adobe Illustrator patentēts faila formāts, un ar EPS saderīgu failu saglabāšanai tiek izmantota divu ceļu pieeja, kas līdzīga PGF. [Adobe Illustrator File Format specifications](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf) sniedz detalizētu izstrādātāja atsauci, lai iegūtu iekšējo informāciju par šo faila formātu. Visi Adobe Illustrator izveidotie dokumenti (faili) ir PostScript valodas dokumenti, un tiem ir divas galvenās daļas, kas atbilst dokumentu strukturēšanas konvencijām: prologs un skripts.

### Prolog

Prolog sadaļā ir ietverta informācija, kas nepieciešama faila interpretācijai. Piemērs varētu būt ierobežojošais lodziņš, kurā ir visas lapas atzīmes. Tajā ir arī informācija par resursiem, piemēram, fonti un procedūru definīcijas. Šie resursi ir loģiski sagrupēti kopās, ko sauc par procsetiem, un satur skaidras metodes to procedūru inicializācijai un pārtraukšanai.

### Skripts

Grafiskos elementus lapā apraksta skripts. Skripts satur atsauces uz operatoriem un procedūrām prologā, kā arī operandus un datus. Trīs skripta loģiskās sadaļas ietver:

 * Setup Sequence — kas inicializē un aktivizē prologā definētos resursus
 * Aprakstošo operatoru secība
 * Reklāmkadri, kas deaktivizē resursus

Operatori skriptā ir grafisko elementu secības, kas rakstītas valodā, ko nosaka procsets prologā. Šīs secības sastāv no datu elementu kolekcijām, grafiskām atribūtu definīcijām un procsetās definēto procedūru izsaukumiem.

### Objektu tagi

Objektu tagus izmanto, lai Adobe Illustrator mākslas objektam pievienotu pielāgotu informāciju. Tagi sastāv no:

 * Atzīmes identifikators
 * Atzīmes veids
 * Dati

## Atsauces
* [Adobe Illustrator faila formāta specifikācijas](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf)

* [AI faila formāts, ko nodrošina PaintShopPro](https://www.paintshoppro.com/en/pages/ai-file/)


