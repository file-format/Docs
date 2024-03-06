{
  "date": "2019-10-11",
  "keywords": [
"rtf fails",
"rtf faila formāts",
"kas ir rtf fails",
"failu",
"rtf piemērs",
"rtf faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RTF — bagātināta teksta formāts",
  "description": "Uzziniet par RTF failu formātu un API, kas var izveidot un atvērt RTF failus.",
  "linktitle": "RTF",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-rt-lvf"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir RTF fails?

Microsoft ieviestais un dokumentētais bagātinātā teksta formāts (**RTF**) ir metode formatēta teksta un grafikas kodēšanai lietošanai lietojumprogrammās. Formāts atvieglo starpplatformu dokumentu apmaiņu ar citiem Microsoft produktiem, tādējādi kalpojot sadarbspējas mērķim. Šī iespēja padara to par standartu datu pārsūtīšanai starp tekstapstrādes programmatūru, un tādējādi saturu var pārsūtīt no vienas operētājsistēmas uz citu, nezaudējot dokumenta formatējumu. Faila formāta specifikācijas ir pieejamas Microsoft publiskai lietošanai [download](https://interoperability.blob.core.windows.net/files/Archive_References/%5bMSFT-RTF%5d.pdf), un tās var atsaukties no izstrādātāja viedokļa.

## Īsa RTF faila formāta vēsture ##

RTF file format has underwent several revisions since its publication. Its official version for read/write was published as part of Microsoft Word 3.0 for Macintosh with version 1.0 specifications. The final version of specifications, 1.9.1 was published by Microsoft in Mar 2008. Pēc tam vairs netiks veikti nekādi uzlabojumi specifikācijās. Pašlaik gandrīz visās operētājsistēmās ir daudz funkcijām bagātākas lietojumprogrammas, kas ir samazinājušas/izskausušas RTF failu formāta izmantošanu.

## RTF faila formāta specifikācijas ##

RTF serves as a standard of data transfer between word processing software and transfer of content from one operating system to another. This is achieved using control words that were introduced by Microsoft Office Word up through 2007. Standarta RTF fails sastāv no ASCII, lai attēlotu bagātinātu tekstu, un ar rakstzīmēm, kas nav ASCII un kas tiek pārveidotas atbilstošās koda vērtībās. Jaunākās Word versijās var lasīt RTF failus, kas ģenerēti ar iepriekšējām versijām, savukārt vecākās versijas ignorē kontroles vārdus un grupas, kuras tās nesaprot.

### Izpratne par RTF pamatiem ###

RTF faili izmanto 7 bitu ASCII vienkāršu tekstu, kas sastāv no:

* kontroles vārdi

* vadības simboli un

* grupas.


Tie darbojas kā pamatelementi RTF datu attēlošanai saprotamā teksta un rakstzīmju kodējuma veidā.

#### Vadības vārds ####

Tie ir īpaši formatētas komandas, ko izmanto, lai atzīmētu rakstzīmes displejam, un tās nedrīkst būt garākas par 32 burtiem. Kontroles vārdu definē:

\<ASCII Letter Sequence> //<//Delimiter//> //

Katrs kontroles vārds ir reģistrjutīgs un sākas ar slīpsvītru. ASCII burtu secībā var būt ASCII alfabēts (no a līdz z un no A līdz Z). The<Delimite> apzīmē kontroles vārda nosaukuma beigas un var būt viens no šiem:

* Telpa. Tas kalpo tikai kontroles vārda norobežošanai un tiek ignorēts turpmākajā apstrādē.

* Ciparu cipars vai ASCII mīnusa zīme, kas norāda, ka ar vadības vārdu ir saistīts skaitlisks parametrs. Nākamā ciparu secība tiek norobežota ar jebkuru rakstzīmi, kas nav ASCII cipars (parasti cits kontroles vārds, kas sākas ar slīpsvītru). Parametrs var būt pozitīvs vai negatīvs decimālskaitlis. Skaitļa vērtību diapazons nomināli ir no –32768 līdz 32767, ti, 16 bitu vesels skaitlis ar zīmi. Nelielam skaitam kontroles vārdu ir vērtības diapazonā‌ -2 147 483 648 līdz 2 147 483 647 (32 bitu vesels skaitlis). Šie kontroles vārdi ietver **\binN**, **\revdttmN//**, **\rsidN** saistītos kontroles vārdus un dažus attēla rekvizītus, piemēram, **\bliptagN**. Šeit **N** apzīmē skaitlisko parametru. RTF parsētājam ir jāatļauj līdz 10 cipariem, pirms kuriem pēc izvēles pievieno mīnusa zīmi. Ja norobežotājs ir atstarpe, tas tiek atmests, tas ir, tas netiek iekļauts turpmākajā apstrādē.

* Jebkura rakstzīme, kas nav burts vai cipars. Šajā gadījumā norobežojošā rakstzīme pārtrauc kontroles vārdu un nav daļa no kontroles vārda. Piemēram, atpakaļvērstā slīpsvītra “\”, kas nozīmē, ka seko jauns vadības vārds vai vadības simbols.


#### Vadības simbols ####

Vadības simbols apzīmē īpašu notikumu, kam ir īpaša nozīme atkarībā no tā satura. Tas sastāv no atpakaļvērstās slīpsvītras, kam seko īpaša rakstzīme (rakstzīme, kas nav alfabēta), un tajā nav atdalītāju.

#### Grupa ####

Grupa var sastāvēt no teksta, vadības vārdiem vai vadības simboliem, kas ietverti iekavās (**{ }**). Sākuma iekava (**{** ) norāda grupas sākumu, bet beigu iekava (**}**) norāda grupas beigas. Katra grupa norāda tekstu, kuru ietekmē grupa, un dažādus šī teksta atribūtus.

### RTF faila struktūra ###

RTF failam ir šāda standarta sintakse:

Microsoft ieviestais un dokumentētais bagātinātā teksta formāts (**RTF**) ir metode formatēta teksta un grafikas kodēšanai lietošanai lietojumprogrammās. Formāts atvieglo starpplatformu dokumentu apmaiņu ar citiem Microsoft produktiem, tādējādi kalpojot savietojamības mērķim. Šī iespēja padara to par standartu datu pārsūtīšanai starp tekstapstrādes programmatūru, un tādējādi saturu var pārsūtīt no vienas operētājsistēmas uz citu, nezaudējot dokumenta formatējumu. Faila formāta specifikācijas ir pieejamas Microsoft publiskai lietošanai [download](https://interoperability.blob.core.windows.net/files/Archive_References/%5bMSFT-RTF%5d.pdf), un tās var atsaukties no izstrādātāja viedokļa.

#### RTF galvene ####

RTF galvenei ir šāds attēlojums.

|Lauks|Apraksts
---|---|
|\<header> |**\rtf1\fbidis**? \<character set> \<from> ? \<deffont> \<deflang> \<fonttbl> ? \<filetbl> ? \<colortbl> ? \<stylesheet> ? \<stylerestrictions> ? \<listtables> ? \<revtbl> ? \<rsidtable> ? \<mathprops> ? \<generator> ?

Galvenes tabulām, ja tādas pastāv, ir jāparādās šādā secībā. RTF failā var iekļaut grupas fontiem, stiliem, ekrāna krāsām, attēliem, zemsvītras piezīmēm, komentāriem (anotācijām), galvenēm un kājenēm, kopsavilkuma informācijai, laukiem, grāmatzīmēm, dokumenta, sadaļas, rindkopas un rakstzīmju formatēšanas rekvizītiem, matemātikai, attēlus un objektus. Ja failā ir iekļauts fonts, fails, stils, krāsa, pārskatīšanas zīme un kopsavilkuma informācijas grupas un dokumenta formatēšanas rekvizīti, tiem ir jāparādās RTF galvenē, kas atrodas pirms RTF pamatteksta. Ja netiek izmantots kādas grupas saturs, grupu var izlaist. Jebkurai grupai, kas izmanto citā grupā definētos rekvizītus, ir jāparādās aiz grupas, kas definē šos rekvizītus. Piemēram, krāsu un fontu rekvizītiem ir jābūt pirms stilu grupas.

#### RTF versija ####

RTF dokumentam jāsākas ar šīm sešām rakstzīmēm:

```
{\rtf1
```
kur 1 norāda RTF versijas numuru.

#### Rakstzīmju kopa ####

Pēc {\rtf1 dokumentam ir jādeklarē, kādu rakstzīmju kopu tas izmanto. Rakstzīmju kopas deklarēšanas veids ir ar vienu no šīm komandām:

`\ansi` — dokuments atrodas ANSI rakstzīmju kopā, kas pazīstama arī kā Code Page 1252, parastajā MSWindows rakstzīmju kopā.

`\mac` — dokuments ir ietverts MacAscii rakstzīmju kopā, kas ir parastā rakstzīmju kopa vecajās (pirms 10) Mac OS versijām.

`\pc` — dokuments atrodas DOS koda lappusē 437, kas ir noklusējuma rakstzīmju kopa MS-DOS. Mašīnrakstītāji ar labu muskuļu atmiņu ievēros, ka šī ir rakstzīmju kopa, kas joprojām tiek izmantota Alt ciparu” kodu interpretēšanai, ti, turot nospiestu Alt un ierakstot 130” uz ciparu tastatūras, tiek parādīta é, jo rakstzīme 130 CP437 ir é. Tas ir vienīgais lietojums, ko CP437 redz šajās dienās.

`\pca` — dokuments atrodas DOS koda lapā 850, kas pazīstama arī kā MS-DOS daudzvalodu kodu lapa.

#### Fontu komanda ####

Rakstzīmju kopas definīcijai seko komanda `\deffN`. Tas nosaka, ka fonta numurs N ir šī dokumenta noklusējuma fonts. Fonta numurs N ir norādīts no fontu tabulas. Komanda `\deffN' tehniski nav obligāta, taču tai ir jābūt drošai kā parastam prologam, piemēram, kā noklusējuma fontu izvēlas fontu 0.

{\rtf1\ansi\deff0.

#### Fontu tabula ####

Visi fonti, ko var izmantot dokumentā, ir uzskaitīti fontu tabulā, kur katrs fonts ir attēlots ar fonta numuru. Dokumentam ir jābūt fontu tabulai, lai gan dažas programmas darbosies arī bez tās.

Fontu tabulas sintakse ir {\fonttbl //...declarations//...}, kurā katrai deklarācijai ir šāda pamata sintakse:

`{\fnumber\familycommand Fontname;}`

Fontu tabula ar četrām deklarācijām ir šāda:

```
{\fonttbl
{\f0\froman Times;}
{\f1\fswiss Arial;}
{\f2\fmodern Courier New;}
}
```

Dokumentā ar šo fontu tabulu `{\f2 stuff}` drukātu stuff” programmā Courier New. Fontu nevar izmantot dokumentā, kamēr tas nav norādīts fontu tabulā.

### Dokumenta beigas ###

Katram RTF dokumentam ir jābeidzas ar }, lai aizvērtu grupu, ko atver {, kas ir pirmā rakstzīme dokumentā. Nekas nevar sekot finālam }, izņemot, iespējams, jaunu rindiņu.

## Atsauces Nr.

* [RTF 1.9.1 specifikācijas](https://interoperability.blob.core.windows.net/files/Archive_References/%5bMSFT-RTF%5d.pdf)

* [bagātināta teksta formāts](https://en.wikipedia.org/wiki/Rich_Text_Format)


