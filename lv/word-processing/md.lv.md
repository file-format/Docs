{
  "date": "2019-10-11",
  "keywords": [
"md failu",
"md faila formātā",
"kas ir md fails",
"failu",
"md piemērs",
"md faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MD — MarkDown valodas fails",
  "description": "Uzziniet par MD failu formātu un API, kas var izveidot un atvērt MD failus.",
  "linktitle": "MD",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-m-lvd"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir MD fails?

Teksta faili, kas izveidoti ar Markdown valodas dialektiem, tiek saglabāti ar faila paplašinājumu **.md** vai **.MARKDOWN**. MD faili tiek saglabāti vienkārša teksta formātā, kurā tiek izmantota Markdown valoda, kurā ir iekļauti arī iekļauti teksta simboli, kas nosaka, kā tekstu var formatēt, piemēram, atkāpes, tabulas formatējumu, fontus un galvenes. MD failus var konvertēt uz HTML, izmantojot programmu Markdown. Markdown valodu izlaida Džons Grubers.

MD failus var arī klasificēt kā izstrādātāju failus, kurus galvenokārt izmanto Markdown, lai pārveidotu teksta failus HTML versijās, lai lietotāji varētu izveidot failus, kurus ir viegli lasīt un rakstīt. Tālāk ir norādītas lietojumprogrammas, ar kurām var atvērt .md failu.

* Microsoft Notepad

* Notepad2

* Apple TextEdit

* Microsoft WordPad


Uzmanību: nepārdēvējiet .md failu paplašinājumus. Ja tā, tas nemainīs faila tipu, jo ir pieejama īpaša konvertēšanas programmatūra, lai mainītu failu no viena veida uz citu. Kā minēts iepriekš, .MD faili ir Markdown valodas programmatūras izveidoto failu paplašinājumi. **Markdown** ir [lightweight markup language](https://en.wikipedia.org/wiki/Lightweight_markup_language), kas paredzēts vienam mērķim, lai formatētu tekstu tīmeklī ar vienkārša teksta formatēšanas sintaksi. Ir skaidrs, ka Markdown neaizstāj HTML, jo tā sintakse ir ļoti maza un satur ļoti mazu HTML tagu apakškopu. Markdown iemesls ir atvieglot prozas lasīšanu, rakstīšanu un rediģēšanu. Citiem vārdiem sakot, mēs varam teikt, ka HTML ir publicēšanas formāts, savukārt Markdown ir rakstīšanas formāts.

Markdown tagad ir viena no pasaulē populārākajām iezīmēšanas valodām. Lietojot Microsoft Word, vārdu un frāžu formatēšana notiek, noklikšķinot uz pogām, un izmaiņas ir uzreiz redzamas. Bet Markdown nav tāds. Kad tiek izveidots Markdown formatēts fails, tekstam tiek pievienota Markdown sintakse, lai norādītu, kuri vārdi un frāzes var izskatīties atšķirīgi. Piemēram, lai parādītu virsrakstu, pirms tā tiek pievienota cipara zīme (piemēram, # Heading One). Lai izveidotu treknrakstu, pirms un pēc tā tiek pievienotas divas zvaigznītes (piem., **šis teksts ir treknrakstā**). Markdown sintaksi var redzēt pēc teksta atrašanās vietas.

## Īsa vēsture

Džons Grūbers un Ārons Svarcs 2004. gadā izveidoja Markdown valodu ar domu ļaut cilvēkiem rakstīt, izmantojot viegli lasāmu un rakstāmu vienkārša teksta formātu un iespēju to pārveidot par XHTML vai HTML. Tās dizaina mērķis ir lasāmība — valoda ir lasāma tāda, kāda tā ir, neizskatās, ka tā ir marķēta vai pievienota ar formatēšanas instrukcijām, kā tas tiek darīts iezīmēšanas valodās, piemēram, RTF vai HTML, kur tagi un formatēšanas norādījumi ir skaidri redzami. Pamata iedvesmas avots ir esošo konvenciju izmantošana vienkārša teksta atzīmēšanai e-pastā.

Kopš tā laika Markdown ir atkārtoti ieviesuši citi, kā arī Perl [module](https://en.wikipedia.org/wiki/Modular_programming), kas pieejams vietnē [CPAN](https://en.wikipedia.org/wiki/CPAN) un dažādās citās programmēšanas valodās. Tas tiek izplatīts ar [BSD-style license](https://en.wikipedia.org/wiki/BSD_license) un ir iekļauts vai pieejams kā spraudnis vairākiem [content-management systems](https://en.wikipedia.org/wiki/Content_management_system).

## MD failu tehniskās specifikācijas

Kad kaut kas tiek rakstīts programmā Markdown, teksts vispirms tiek saglabāts vienkārša teksta failā ar paplašinājumu .md vai .markdown, pēc tam Markdown faila apstrādei tiek izmantota Markdown lietojumprogramma, piemēram, Dillinger, lai pārveidotu Markdown formatētu tekstu par HTML, lai to parādītu tīmeklī. pārlūkprogrammas. Markdown lietojumprogrammas izmanto //Markdown procesoru// (ko parasti dēvē arī par parsētāju” vai ieviešanu”), lai ņemtu Markdown formatētu tekstu un izvadītu to HTML formātā. Procesa plūsmas diagramma ir šāda:

Īsāk sakot, tas ir četru soļu process:

1. Pirmkārt, Markdown failu izveide ar teksta redaktoru vai Markdown lietojumprogrammu ar paplašinājumu .md vai .markdown.
1. Pēc tam Markdown fails tiek atvērts Markdown lietojumprogrammā.
1. Markdown lietojumprogramma tiek izmantota, lai pārvērstu Markdown failu par HTML dokumentu.
1. Pēc tam HTML fails tiek skatīts tīmekļa pārlūkprogrammā vai tiek izmantota lietojumprogramma Markdown, lai to pārveidotu citā faila formātā, piemēram, PDF formātā.

Markdown ir ātra un vienkārša piezīmju veikšana, satura rakstīšana vietnei, drukāšanai gatavu dokumentu sagatavošana, grāmatu publicēšanai, prezentāciju ģenerēšanai un dokumentu veidošanai.

Dažām pazemināšanas versijām bija tik liela ietekme uz citām versijām, ka tās bieži būs citētas kā daļa no citām versijām. Piemēram, bibliotēkas min atbalstu CommonMark (GFM). Īsi tos apskatīsim.

### GFM
Markdown ir tik populāra izstrādātāju vidū, jo atvērtā pirmkoda koplietošanas platforma Github pieņēma un paplašināja valodu ar versiju ar nosaukumu Github Flavored Markup (GFM), kas ietver norobežotus kodu blokus, URL aultlinking, pārsvītrojumus, tabulas un uzdevumu izveidi.

### CommonMark
Markdown izstrādātāji nesen mēģināja standartizēt atzīmes, viņi apvienojās, lai izveidotu versiju, testus un dokumentāciju valodai, kas ir spēcīgāka un tiek saukta par CommonMark. Šis formāts ir nedaudz jauns un neatbalsta daudzas funkcijas, taču drīzumā tiks pievienotas daudzas MultiMarkdown funkcijas.

### Vairāku atzīmju samazināšana
Multi-Markdown valodai pievienoja dažādas funkcijas, kuras atbalsta citas versijas. Sākotnēji tas tika rakstīts Perl, bet vēlāk tika pārvietots uz C. Tā atbalsta norobežotus kodu blokus, sintakses izcelšanu, tabulas, metadatus, fragmentu/krustutsaišu saites, zemsvītras piezīmes, pārsvītrojumus, definīciju sarakstus, matemātiku.

## Kāpēc MarkDown?

MD faili ir populāra izvēle šādu iemeslu dēļ.

1. **Vienkārša sintakse:** Markdown izmanto vienkāršu un intuitīvu sintaksi, kuru ir viegli iemācīties un rakstīt. Sintakse ir izstrādāta tā, lai tā būtu lasāma kā vienkāršs teksts, padarot to pieejamu lietotājiem, kuri nepārzina HTML vai citas sarežģītākas iezīmēšanas valodas.

1. **Atkarīgs no platformas:** Markdown failus var izveidot un rediģēt jebkurā platformā, tostarp Windows, Mac un Linux, jo tie ir tikai teksta faili. Tas padara tos par populāru izvēli sadarbībai, jo īpaši sadalītās komandās, kur dažādi komandas dalībnieki var izmantot dažādas operētājsistēmas.

1. **Pārnesamība:** Markdown faili ir pārnēsājami, kas nozīmē, ka tos var viegli konvertēt citos formātos, piemēram, HTML, PDF un Word. Tas padara tos par ideālu formātu dokumentācijas, emuāra ierakstu un cita veida satura izveidei, kas var būt jākopīgo dažādos formātos.

1. **Versiju kontrole:** Markdown failus var viegli izsekot un pārvaldīt, izmantojot versiju kontroles sistēmas, piemēram, Git. Tādējādi ir viegli sadarboties ar dokumentiem ar citiem komandas locekļiem, izsekot izmaiņām laika gaitā un, ja nepieciešams, atgriezties pie iepriekšējām versijām.

1. **Pieejamība:** Markdown faili ir pieejami lietotājiem ar invaliditāti, jo tos var viegli konvertēt citos formātos, piemēram, Braila rakstā, audio un ekrānā lasāmā tekstā.

## Atsauces

 * [Mastering MarkDown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

