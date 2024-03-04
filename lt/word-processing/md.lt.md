{
  "date": "2019-10-11",
  "keywords": [
"md failą",
"md failo formatą",
"kas yra md failas",
"failą",
"md pavyzdys",
"md failo plėtinį",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MD – MarkDown kalbos failas",
  "description": "Sužinokite apie MD failo formatą ir API, kurios gali kurti ir atidaryti MD failus.",
  "linktitle": "MD",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-m-ltd"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra MD failas?

Tekstiniai failai, sukurti naudojant Markdown kalbos dialektus, išsaugomi su **.md** arba **.MARKDOWN** failo plėtiniu. MD failai išsaugomi paprasto teksto formatu, kuriame naudojama Markdown kalba, kurioje taip pat yra įterptųjų teksto simbolių, apibrėžiančių, kaip galima formatuoti tekstą, pvz., įtraukas, lentelės formatavimą, šriftus ir antraštes. MD failus galima konvertuoti į HTML naudojant programą, pavadintą Markdown. Markdown kalbą išleido John Gruber.

MD failai taip pat gali būti klasifikuojami kaip kūrėjo failai, kuriuos dažniausiai naudoja Markdown, kad konvertuotų tekstinius failus į HTML versijas, kad vartotojai galėtų kurti failus, kuriuos būtų lengva skaityti ir rašyti. Toliau pateikiamos programos, kuriomis galima atidaryti .md failą:

* Microsoft Notepad

* Notepad2

* Apple TextEdit

* Microsoft WordPad


Atsargiai nepervardykite .md failų plėtinio. Jei taip, tai nepakeis failo tipo, nes yra speciali konvertavimo programinė įranga, skirta pakeisti failą iš vieno tipo į kitą. Kaip aptarta aukščiau, .MD failai yra failų, sukurtų Markdown kalbos programinės įrangos plėtiniai. **Markdown** yra [lightweight markup language](https://en.wikipedia.org/wiki/Lightweight_markup_language), skirta vienam tikslui, naudojama teksto formatavimui žiniatinklyje naudojant paprasto teksto formatavimo sintaksę. Leiskite suprasti, kad Markdown nėra HTML pakaitalas, nes jo sintaksė yra labai maža, joje yra labai mažas HTML žymų poaibis. Markdown priežastis yra ta, kad būtų lengva skaityti, rašyti ir redaguoti prozą. Kitaip tariant, galime pasakyti, kad HTML yra publikavimo formatas, o Markdown yra rašymo formatas.

Markdown dabar yra viena populiariausių žymėjimo kalbų pasaulyje. Naudojant Microsoft Word, žodžių ir frazių formatavimas atliekamas spustelėjus mygtukus, o pakeitimai iškart matomi. Bet Markdown nėra toks. Kai sukuriamas Markdown formato failas, Markdown sintaksė pridedama prie teksto, kad būtų nurodyta, kurie žodžiai ir frazės gali atrodyti kitaip. Pavyzdžiui, norint parodyti antraštę, prieš ją pridedamas skaičiaus ženklas (pvz., # Heading One). Kad sakinys būtų paryškintas, prieš ir po jo pridedamos dvi žvaigždutės (pvz., **šis tekstas paryškintas**). Pažymėjimo sintaksė gali būti matoma po to, kai esate tekste.

## Trumpa istorija

Johnas Gruberis ir Aaronas Swartzas 2004 m. sukūrė Markdown kalbą, siekdami suteikti žmonėms galimybę rašyti naudojant lengvai skaitomą ir rašomą paprasto teksto formatą ir galimybę konvertuoti jį į XHTML arba HTML. Jos dizaino tikslas yra skaitomumas – kalba yra skaitoma tokia, kokia ji yra, neatrodo, kad ji būtų pažymėta arba pridėta su formatavimo instrukcijomis, kaip tai daroma žymėjimo kalbomis, pvz., RTF arba HTML, kur žymos ir formatavimo instrukcijos yra akivaizdžios. Pagrindinis įkvėpimo šaltinis yra esamų susitarimų naudojimas ženklinant paprastą tekstą el.

Nuo tada Markdown buvo iš naujo įdiegtas kitų, taip pat kaip Perl [module](https://en.wikipedia.org/wiki/Modular_programming), pasiekiamas [CPAN](https://en.wikipedia.org/wiki/CPAN) ir įvairiomis kitomis programavimo kalbomis. Jis platinamas naudojant [BSD-style license](https://en.wikipedia.org/wiki/BSD_license) ir yra įtrauktas į keletą [content-management systems](https://en.wikipedia.org/wiki/Content_management_system) arba yra prieinamas kaip priedas.

## Techninės MD failų specifikacijos

Kai kas nors parašyta Markdown, tekstas pirmiausia išsaugomas paprasto teksto faile, kurio plėtinys yra .md arba .markdown, tada Markdown programa, tokia kaip Dillinger, naudojama Markdown failo apdorojimui, konvertuojant Markdown formatuotą tekstą į HTML, kad jis būtų rodomas žiniatinklyje. naršyklės. Markdown programos naudoja //Markdown procesorių// (taip pat vadinamą analizatoriumi arba diegimu), kad paimtų Markdown formatuotą tekstą ir išvestų jį į HTML formatą. Proceso schema yra tokia:

Trumpai tariant, tai yra keturių etapų procesas:

1. Pirma, Markdown failų kūrimas naudojant teksto rengyklę arba Markdown programą su plėtiniu .md arba .markdown.
1. Tada Markdown failas atidaromas Markdown programoje.
1. Markdown programa naudojama konvertuoti Markdown failą į HTML dokumentą.
1. Tada HTML failas peržiūrimas žiniatinklio naršyklėje arba naudojama Markdown programa, kad jis būtų konvertuojamas į kitą failo formatą, pvz., PDF.

Markdown yra greita ir paprasta užsirašinėti, rašyti turinį svetainei, gaminti spaudai paruoštus dokumentus, išleisti knygas, generuoti pristatymus ir kurti dokumentus.

Kai kurios sumažintos versijos turėjo tiek daug įtakos kitoms versijoms, kad dažnai jos bus cituojamos kaip kitų versijų dalis. Pavyzdžiui, bibliotekos mini CommonMark (GFM) palaikymą. Trumpai apžvelkime juos.

### GFM
Markdown yra toks populiarus kūrėjams, nes atvirojo kodo dalijimosi platforma Github priėmė ir išplėtė kalbą su versija, pavadinta Github Flavoured Markup (GFM), kuri apima aptvertus kodų blokus, URL nuorodas, perbraukimą, lenteles ir užduočių kūrimą.

### CommonMark
Markdown kūrėjai neseniai bandė standartizuoti žymėjimą, jie susijungė, kad sukurtų tvirtesnės kalbos versiją, testus ir dokumentaciją, kuri vadinama CommonMark. Šis formatas yra šiek tiek naujas ir nepalaiko daug funkcijų, tačiau netrukus bus pridėta daug MultiMarkdown funkcijų.

### Daugkartinis žymėjimas
Multi-Markdown į kalbą pridėjo įvairių funkcijų, kurias palaiko kitos versijos. Iš pradžių jis buvo parašytas Perl, bet vėliau perkeltas į C. Jis palaiko aptvertus kodų blokus, sintaksės paryškinimą, lenteles, metaduomenis, fragmentų / kryžminių nuorodų nuorodas, išnašas, perbraukimus, apibrėžimų sąrašus, matematiką.

## Kodėl MarkDown?

MD failai yra populiarus pasirinkimas dėl toliau nurodytų priežasčių.

1. **Paprasta sintaksė:** Markdown naudojama paprasta ir intuityvi sintaksė, kurią lengva išmokti ir rašyti. Sintaksė sukurta taip, kad ją būtų galima skaityti kaip paprastą tekstą, kad ji būtų prieinama vartotojams, kurie nėra susipažinę su HTML ar kitomis sudėtingesnėmis žymėjimo kalbomis.

1. **Nepriklausoma nuo platformos:** Markdown failus galima kurti ir redaguoti bet kurioje platformoje, įskaitant Windows, Mac ir Linux, nes tai tik paprasto teksto failai. Dėl to jie yra populiarus pasirinkimas bendradarbiauti, ypač paskirstytose komandose, kur skirtingi komandos nariai gali naudoti skirtingas operacines sistemas.

1. **Perkeliamumas:** Markdown failai yra nešiojami, o tai reiškia, kad juos galima lengvai konvertuoti į kitus formatus, pvz., HTML, PDF ir Word. Tai daro juos idealiu formatu kuriant dokumentus, tinklaraščio įrašus ir kitokio tipo turinį, kurį gali tekti bendrinti skirtingais formatais.

1. **Versijų valdymas:** Markdown failus galima lengvai sekti ir valdyti naudojant versijų valdymo sistemas, tokias kaip Git. Tai leidžia lengvai bendradarbiauti rengiant dokumentus su kitais komandos nariais, stebėti pokyčius laikui bėgant ir, jei reikia, grįžti į ankstesnes versijas.

1. **Prieinamumas:** Markdown failus gali pasiekti naudotojai su negalia, nes juos galima lengvai konvertuoti į kitus formatus, pvz., Brailio raštą, garso įrašą ir ekrane skaitomą tekstą.

## Nuorodos

 * [Mastering MarkDown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

