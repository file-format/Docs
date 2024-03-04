{
  "date": "2019-10-11",
  "keywords": [
"rtf failą",
"rtf failo formatas",
"kas yra rtf failas",
"failą",
"rtf pavyzdys",
"rtf failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RTF – raiškiojo teksto formatas",
  "description": "Sužinokite apie RTF failo formatą ir API, kurios gali kurti ir atidaryti RTF failus.",
  "linktitle": "RTF",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-rt-ltf"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra RTF failas?

Microsoft įdiegtas ir dokumentuotas raiškiojo teksto formatas (**RTF**) yra suformatuoto teksto ir grafikos kodavimo metodas, skirtas naudoti programose. Formatas palengvina kelių platformų dokumentų keitimąsi su kitais Microsoft produktais ir taip tarnauja sąveikos tikslui. Dėl šios galimybės tai yra duomenų perdavimo tarp teksto apdorojimo programinės įrangos standartu, todėl turinį galima perkelti iš vienos operacinės sistemos į kitą neprarandant dokumento formatavimo. Failo formato specifikacijas Microsoft siūlo viešai [download](https://interoperability.blob.core.windows.net/files/Archive_References/%5bMSFT-RTF%5d.pdf) ir jas galima remtis kūrėjo požiūriu.

## Trumpa RTF failo formato ## istorija

RTF file format has underwent several revisions since its publication. Its official version for read/write was published as part of Microsoft Word 3.0 for Macintosh with version 1.0 specifications. The final version of specifications, 1.9.1 was published by Microsoft in Mar 2008. Po to specifikacijos netobulinamos. Šiuo metu beveik visose operacinėse sistemose yra daugiau funkcijų turinčių programų, kurios sumažino / panaikino RTF failo formato naudojimą.

## RTF failo formato specifikacijos ##

RTF serves as a standard of data transfer between word processing software and transfer of content from one operating system to another. This is achieved using control words that were introduced by Microsoft Office Word up through 2007. Standartinis RTF failas susideda iš ASCII, skirto raiškiajam tekstui pavaizduoti, ir su ne ASCII simboliais, kurie konvertuojami į atitinkamas kodo reikšmes. Naujesnės Word versijos gali skaityti RTF failus, sukurtus naudojant ankstesnes versijas, o senesnėse versijose nepaisoma nesuprantamų kontrolinių žodžių ir grupių.

### RTF pagrindų supratimas ###

RTF failuose naudojamas 7 bitų ASCII paprastas tekstas, kurį sudaro:

* kontroliniai žodžiai

* valdymo simboliai ir

* grupės.


Jie veikia kaip RTF duomenų vaizdavimo kaip suprantamo teksto ir simbolių kodavimo elementai.

#### Valdymo žodis ####

Tai yra specialiai suformatuota komanda, naudojama rodyti simbolius ir negali būti ilgesnė nei 32 raidės. Kontrolinis žodis apibrėžiamas taip:

\<ASCII Letter Sequence> //<//Delimiter//> //

Kiekvienas kontrolinis žodis yra didžiosios ir mažosios raidės ir prasideda pasviruoju brūkšniu. ASCII raidžių sekoje gali būti ASCII abėcėlės (nuo a iki z ir nuo A iki Z). The<Delimite> žymi kontrolinio žodžio pavadinimo pabaigą ir gali būti vienas iš šių:

* Erdvė. Tai skirta tik kontrolinio žodžio ribojimui ir vėlesnio apdorojimo metu nepaisoma.

* Skaitmeninis skaitmuo arba ASCII minuso ženklas, nurodantis, kad skaitmeninis parametras susietas su kontroliniu žodžiu. Tolesnė skaitmeninė seka yra atskirta bet kokiu simboliu, išskyrus ASCII skaitmenį (dažniausiai tai yra kitas kontrolinis žodis, prasidedantis pasviruoju brūkšniu). Parametras gali būti teigiamas arba neigiamas dešimtainis skaičius. Skaičiaus reikšmių diapazonas nominaliai yra nuo –32768 iki 32767, ty 16 bitų sveikasis skaičius. Nedidelis kontrolinių žodžių skaičius įgyja reikšmes diapazone‌ –2 147 483 648–2 147 483 647 (32 bitų sveikasis skaičius). Šie valdymo žodžiai apima **\binN**, **\revdttmN//**, **\rsidN** susijusius valdymo žodžius ir kai kurias paveikslėlio ypatybes, pvz., **\bliptagN**. Čia **N** reiškia skaitinį parametrą. RTF analizatorius turi leisti iki 10 skaitmenų, prieš kuriuos pasirinktinai yra minuso ženklas. Jei skyriklis yra tarpas, jis atmetamas, tai yra, jis neįtraukiamas į tolesnį apdorojimą.

* Bet koks simbolis, išskyrus raidę ar skaitmenį. Šiuo atveju skiriamasis simbolis baigia kontrolinį žodį ir nėra kontrolinio žodžio dalis. Pavyzdžiui, pasvirasis brūkšnys „\“, reiškiantis, kad po jo pateikiamas naujas kontrolinis žodis arba valdymo simbolis.


#### Valdymo simbolis ####

Valdymo simbolis reiškia ypatingą įvykį, kuris turi specifinę reikšmę, priklausomai nuo jo turinio. Jį sudaro pasvirasis brūkšnys, po kurio eina specialus simbolis (neabėcėlinis simbolis) ir neturi jokių skiriamųjų ženklų.

#### Grupė ####

Grupę gali sudaryti tekstas, kontroliniai žodžiai arba valdymo simboliai, įterpti skliaustuose (**{ }**). Pradžios skliaustas (**{** ) rodo grupės pradžią, o baigiamasis skliaustas (**}**) rodo grupės pabaigą. Kiekviena grupė nurodo tekstą, kurį paveikė grupė, ir skirtingus to teksto požymius.

### RTF failo struktūra ###

RTF failas turi tokią standartinę sintaksę:

Microsoft įdiegtas ir dokumentuotas raiškiojo teksto formatas (**RTF**) yra suformatuoto teksto ir grafikos kodavimo metodas, skirtas naudoti programose. Formatas palengvina kelių platformų dokumentų keitimąsi su kitais Microsoft produktais ir taip tarnauja sąveikos tikslui. Dėl šios galimybės tai yra duomenų perdavimo tarp teksto apdorojimo programinės įrangos standartu, todėl turinį galima perkelti iš vienos operacinės sistemos į kitą neprarandant dokumento formatavimo. Failų formato specifikacijas Microsoft teikia viešai [download](https://interoperability.blob.core.windows.net/files/Archive_References/%5bMSFT-RTF%5d.pdf) ir jas galima remtis kūrėjo požiūriu.

#### RTF antraštė ####

RTF antraštė turi tokį vaizdą.

|Laukas|Aprašymas
---|---|
|\<header> |**\rtf1\fbidis**? \<character set> \<from> ? \<deffont> \<deflang> \<fonttbl> ? \<filetbl> ? \<colortbl> ? \<stylesheet> ? \<stylerestrictions> ? \<listtables> ? \<revtbl> ? \<rsidtable> ? \<mathprops> ? \<generator> ?

Antraštės lentelės turi būti rodomos tokia tvarka, jei jos yra. RTF faile gali būti šriftų, stilių, ekrano spalvų, paveikslėlių, išnašų, komentarų (komentarų), antraščių ir poraštių, santraukos informacijos, laukų, žymių, dokumento, skyriaus, pastraipos ir simbolių formatavimo ypatybių, matematikos, grupes. vaizdai ir objektai. Jei šriftas, failas, stilius, spalva, peržiūros ženklas ir santraukos-informacijos grupės bei dokumento formatavimo ypatybės yra įtrauktos į failą, jie turi būti rodomi RTF antraštėje, kuri yra prieš RTF turinį. Jei kurios nors grupės turinys nenaudojamas, grupę galima praleisti. Bet kuri grupė, kuri naudoja kitoje grupėje apibrėžtas ypatybes, turi būti rodoma po grupės, kuri apibrėžia tas ypatybes. Pavyzdžiui, prieš stilių grupę turi būti pateiktos spalvos ir šrifto ypatybės.

#### RTF versija ####

RTF dokumentas turi prasidėti šiais šešiais simboliais:

```
{\rtf1
```
kur 1 rodo RTF versijos numerį.

#### Simbolių rinkinys ####

Po {\rtf1 dokumentas turi deklaruoti, kokį simbolių rinkinį jis naudoja. Simbolių rinkinį galima deklaruoti naudojant vieną iš šių komandų:

`\ansi` – dokumentas yra ANSI simbolių rinkinyje, taip pat žinomas kaip Code Page 1252, įprastas MSWindows simbolių rinkinys.

\mac – dokumentas yra MacAscii simbolių rinkinyje, įprastas simbolių rinkinys senose (iki 10) Mac OS versijose.

`\pc` – dokumentas yra DOS kodo puslapyje 437, numatytasis MS-DOS simbolių rinkinys. Rašytojai, turintys gerą raumenų atmintį, pastebės, kad tai yra simbolių rinkinys, kuris vis dar naudojamas interpretuojant Alt skaitinius kodus, ty kai laikote nuspaudę Alt ir įvedate 130 skaičių klaviatūroje, atsiranda é, nes simbolis 130 CP437 yra é. Tai yra vienintelis naudojimas, kurį CP437 mato šiomis dienomis.

`\pca` – dokumentas yra DOS kodo puslapyje 850, taip pat žinomas kaip MS-DOS daugiakalbis kodo puslapis.

#### Šrifto komanda ####

Po simbolių rinkinio apibrėžimo seka komanda \deffN. Tai apibrėžia, kad šrifto numeris N yra numatytasis šio dokumento šriftas. Šrifto numeris N nurodytas iš šriftų lentelės. Komanda \deffN yra techniškai neprivaloma, tačiau ji turėtų būti saugi kaip įprastas prologas, pavyzdžiui, kaip numatytąjį šriftą pasirenkamas 0 šriftas.

{\rtf1\ansi\deff0.

#### Šriftų lentelė ####

Visi šriftai, kuriuos galima naudoti dokumente, yra išvardyti šriftų lentelėje, kur kiekvienas šriftas yra pavaizduotas šrifto numeriu. Dokumente turi būti šriftų lentelė, nors kai kurios programos veiks ir be jos.

Šriftų lentelės sintaksė yra {\fonttbl //...declarations//...}, kurioje kiekviena deklaracija turi šią pagrindinę sintaksę:

{\fnumber\familycommand Fontname;}.

Šriftų lentelė su keturiomis deklaracijomis yra tokia:

```
{\fonttbl
{\f0\froman Times;}
{\f1\fswiss Arial;}
{\f2\fmodern Courier New;}
}
```

Dokumente su ta šrifto lentele {\f2 stuff} Courier New spausdintų stuff. Šriftas negali būti naudojamas dokumente, kol jis nėra įtrauktas į šriftų lentelę.

### Dokumento pabaiga ###

Kiekvienas RTF dokumentas turi baigtis }, kad būtų uždaryta grupė, atidaryta {, kuris yra pirmasis dokumento simbolis. Niekas negali sekti galutinio }, išskyrus galbūt naują eilutę.

## Nuorodos Nr.

* [RTF 1.9.1 specifikacijos](https://interoperability.blob.core.windows.net/files/Archive_References/%5bMSFT-RTF%5d.pdf)

* [Raiškiojo teksto formatas](https://en.wikipedia.org/wiki/Rich_Text_Format)


