{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TEX faila formāts",
  "description": "Uzziniet par TEX failu formātu un API, kas var izveidot un atvērt TEX failus.",
  "linktitle": "TEX",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-te-lvx"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir TEX fails? ##

**TeX** ir valoda, kas ietver programmēšanu, kā arī iezīmēšanas funkcijas, ko izmanto dokumentu salikšanai. Donalds Knuts no Stenfordas universitātes ir šīs atjautīgās salikšanas sistēmas radītājs. Visā pasaulē TeX ir labākā autoru un izdevēju izvēle augstas kvalitātes tehnisko dokumentu sagatavošanai. TeX veic izcilu darbu sarežģītu matemātisku izteiksmju formatēšanā. Savienojumā ar augstas kvalitātes fotosalikumu TeX konkurē ar rezultātiem, ko rada labākās tradicionālās salikšanas sistēmas. Tāpēc tās tiek uzskatītas par visklasīgākajām digitālajām tipogrāfiskajām sistēmām.

TeX ievades faili ir balstīti uz ASCII kodu, tādējādi ļaujot koplietot manuskriptus starp rakstniekiem, izdevniecības vadītājiem un kritiķiem. Plašs skaitļošanas vidi klāsts, gandrīz visas modernās platformas un daudzas vecākas platformas atbalsta TeX. Turklāt TeX ir bezmaksas programmatūra, kas pieejama plašam patērētāju lokam. Daudzas UNIX instalācijas izmanto gan UNIX troff, gan TeX kā formatēšanas sistēmu dažādiem mērķiem. Citi salikšanas uzdevumi tiek veikti ārkārtīgi daudz LaTeX, ConTeXt un citu makro pakotņu veidā.

## Īsa vēsture ##

TeX was designed and written by Donald Knuth in 1978. Gajs Stīls no Masačūsetsas Tehnoloģiju institūta pārskatīja TeX ievadi/izvadi, lai tas darbotos ar nesaderīgu operētājsistēmu, piemēram, laika dalīšanas sistēmu (ITS). Pirmā TeX versija tika izstrādāta Stenfordas WAITS operētājsistēmā programmēšanas valodā (SAIL) un pārbaudīta, lai tā darbotos ar PDP-10. Knuts iepazīstināja ar ideju par izglītotu programmēšanu iepriekšējām versijām. Literate programmēšana ir veids, kā ģenerēt kompilējamu avota kodu un salikumu (TeX valodā) savstarpēji saistītai dokumentācijai, izmantojot oriģinālo failu. Valoda, ko izmanto, lai izstrādātu šīs uzlabotās TeX versijas, tiek saukta par WEB — DEC PDP-10 Pascal programmu sajaukumu, lai nodrošinātu pārnesamību.

A revised new version of TeX published in 1982 and was called TeX82. Galvenās izmaiņas ir sākotnējā defises algoritma aizstāšana ar Frenka Lianga tikko uzrakstīto algoritmu. Lai nodrošinātu pārnesamību dažādās platformās, TeX82 peldošā komata izmantošanas vietā izmanto fiksētā komata aritmētiku kopā ar īstu, Tūringa pilnu programmēšanas valodu. 1989. gadā tika izlaistas jaunas TeX un Metafont versijas. Tātad TeX versija 3.0 atvieglo 8 bitu ievadi, ļaujot tekstā izmantot 256 dažādas rakstzīmes. Pēc 3. versijas atjauninājumi tiek apzīmēti, pievienojot papildu ciparu decimāldaļas beigās, piemēram, pašreizējā TeX versija tiek norādīta kā 3.14159265. Šī versija pēdējo reizi tika atjaunināta 12-1-2014.

## TeX ievade ##

TEX ievades failu var sagatavot ar teksta redaktoru, izmantojot parasto tekstu. Atšķirībā no parasta Word procesora, šis ievades fails neļauj izmantot neredzamas vadības rakstzīmes. Vienu failu var iegult citā failā, kas satur makro definīcijas un palīgdefinīcijas, kas uzlabo TeX iespējas. Ja TeX instalācijā ir iekļauti makro faili, vietējā informācija par TeX parāda makro failu izmantošanu. TeX standarta forma integrē makro un citu definīciju kombināciju, kas pazīstama kā vienkāršais TEX.

Pamatojoties uz precīzām zināšanām par visu rakstzīmju un simbolu izmēriem, tā aprēķina optimālo burtu izvietojumu vienā rindiņā un rindu vienā lapā. Dokumentu apstrādes laikā tiek izveidots .dvi fails, kur dvi” nozīmē atkarīgs no ierīces”. Lai drukātu vai priekšskatītu dokumentu ar paplašinājumu dvi, ir nepieciešamas ierīces draiveru programmas. Mūsdienās dvi ģenerēšanu apiet parasti izmanto pdf-TeX. TeX instalācijā nav pieejamas iepriekšējas zināšanas par fontiem, tāpēc dokumenta informācijas iegūšanai tiek izmantoti ārējie fontu faili, kas ir daļa no vietējās TeX vides.

## Salikšanas sistēma ##

Ar bāzes TeX sistēmu var saprast aptuveni 300 primitīvus (komandas). Primitīvas ir zema līmeņa komandas, tāpēc parasts lietotājs tās reti izmanto tieši un lielāko daļu funkcionalitātes veic formāta faili. Šie formāta faili ir iepriekš ielādēti TeX atmiņas attēli, kam seko lielu makro kolekciju ielāde. Sākotnējais valodas noklusējuma formāts, ti, vienkāršais TeX, pievieno apmēram 600 komandas.

Slīpssvītra, kas sagrupēta ar krokainajām iekavām, apzīmē TeX komandu sākumu. Tā kā TeX ir valoda, kuras pamatā ir makro un marķieri, gandrīz visas TeX sintaktiskās īpašības var mainīt izpildes laikā, tostarp lietotāja definētās, izņemot nepaplašināmus marķierus, kas pēc tam tiek izpildīti. Pati paplašināšana ir praktiski bez problēmām. Dažām komandām jānāk aiz argumentiem, kas palīdz izskaidrot komandas funkciju. Piemēram, komanda \vskip liek TEX izlaist lapu uz leju/augšup, kam seko arguments, kas nosaka, cik daudz vietas izlaist.

## Versijas ##

LaTeX ir visbiežāk izmantotais formāts, kuru sākotnēji izstrādāja Leslija Lamporta. LaTeX integrē dažādus dokumentu stilus failiem, vēstulēm, grāmatām un slaidiem un piedāvā atsauces un automātisku numerāciju dažādām sadaļām un matemātiskām izteiksmēm. AMS-TeX ir vēl viens populārs formāts, ko izstrādājusi Amerikas Matemātikas biedrība.

AMS-TeX piedāvā daudz lietotājam draudzīgākas komandas, kuras žurnāli var no jauna definēt, lai tās atbilstu viņu vietējam stilam. LaTeX var izmantot AMS-TeX priekšrocības, izmantojot AMS paketes, kuras pēc tam sauc par AMS-LaTeX. ConTeXt ir vēl viens Hansa Hāgena uzrakstīts formāts, ko galvenokārt izmanto darbvirsmas publicēšanai.

TeX programmatūra piedāvā vairākas funkcijas, kas tās izveides laikā nebija pieejamas vai bija zemākas kvalitātes citās salikšanas sistēmās. Dažas šīs valodas novatoriskās iezīmes ir balstītas uz interesantiem algoritmiem, kas iegūti no Knuta studentu tēzēm. Lai gan citas salikšanas programmas tagad savās programmās iekļauj noderīgas TeX funkcijas.

## Atsauces Nr.

* [TeX rakstīšanas sistēma](https://en.wikipedia.org/wiki/TeX)


