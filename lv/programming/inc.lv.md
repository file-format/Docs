{
  "date": "2022-07-14",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "INC faila paplašinājums — kas ir INC fails?",
  "description": "Uzziniet par INC Iekļaut faila formātu un API, kas var izveidot un atvērt INC failus.",
  "linktitle": "INC",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-in-lvc"
}
},
  "lastmod": "2022-07-14"
}

## Kas ir INC fails?

INC fails ir iekļauts fails, ko programmatūras programmas pirmkods izmanto, lai atsauktos uz informāciju par galvenēm. Tas ir līdzīgs [.h file format](/programming/h/) un satur deklarācijas, funkcijas, galvenes vai makro, ko var atkārtoti izmantot avota koda failos, piemēram, C++. INC failus izmanto dažādas programmēšanas valodas, piemēram, C, [C++](/programming/cpp/), Pascal, [PHP](/programming/php/) un [Java](/programming/java/). INC failu atvēršanai var izmantot teksta redaktorus, piemēram, Microsoft Notepad, Notepad++ un TextEdit.

## INC faila formāts — vairāk informācijas

INC fails tiek saglabāts kā vienkārša teksta fails ar visām deklarācijām, kas iekļautas saskaņā ar deklarācijas sintakse. Viens INC fails var atsaukties arī uz citiem INC failiem. Kad INC fails ir izveidots, tas kļūst par projekta daļu, un uz to var atsaukties no avota failiem, piemēram, C++. Uz to var atsaukties vairāki avota faili, lai izvairītos no dublēšanās.

## INC faila saturs

INC faili var ietvert šādu informāciju.

**`Mainīgie`** — objektorientētas programmēšanas (OOP) gadījumā klases galvenes failā ir visu klases līmeņa mainīgo definīcijas, kas ir pieejamas ieviešanas avota koda failos.

**`Metožu deklarācija`** — visas metožu deklarācijas ir iekļautas .h galvenes failos, lai tās būtu pieejamas vairākos ieviešanas failos.

**`Neiekļautās funkciju definīcijas`** — galvenes faili var saturēt arī neiekļauto metožu definīcijas.

## INC faila izmantošanas trūkums PHP

PHP ir servera puses skripti, kas darbojas serverī un atgriež rezultātus izsaucošajām tīmekļa lapām. Ja PHP fails atsaucas uz INC failu un serveris nav konfigurēts .inc failu parsēšanai (kas ir ļoti bieži), lietotājs var skatīt php avota kodu .inc failā, apmeklējot URL direktoriju. Tāpēc, izmantojot INC failus, jābūt uzmanīgiem, jo iekļauj failus PHP.

## Atsauces

* [INC izmantošana PHP valodā](https://stackoverflow.com/questions/7129842/what-is-an-inc-and-why-use-it)


