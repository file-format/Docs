{
  "date": "2019-10-11",
  "keywords": [
"h",
".hh",
"kas ir .hh fails",
"kā atvērt .hh failu",
"pagarinājumu",
"failu",
".hh failu",
".hh faila formāts",
".hh faila paplašinājums",
".HH faila piemērs"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HH — C++ galvenes faila formāts",
  "description": "Uzziniet par HH faila formātu un API, kas var izveidot un atvērt HH failu.",
  "linktitle": "HH",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-h-lvh"
}
},
  "lastmod": "2021-06-20"
}

## Kas ir HH fails?

Fails ar paplašinājumu .hh ir C++ galvenes fails, kas ietver mainīgo, konstantu un funkciju deklarāciju. Šīs deklarācijas izmanto atbilstošie C++ ieviešanas faili, kas parasti tiek saglabāti kā [.cpp](/programming/cpp/) faili, kas satur faktisko lietotāja loģikas ieviešanu. Uz .hh galvenes failiem ir atsauces ieviešanas CPP failos, izmantojot direktīvu #include. C++ projektam varat pievienot pēc iespējas vairāk galvenes failu, lai iekļautu projekta līmeņa deklarācijas.

## .HH faila formāts

.hh fails ir vienkārša teksta fails, kas tiek izveidots, ievērojot galvenes faila definīcijas noteikumus. Visbiežāk sastopamā informācija, kas tiek deklarēta .hh failā, ir šāda.

**`Mainīgie`** — objektorientētas programmēšanas (OOP) gadījumā klases galvenes failā ir visu klases līmeņa mainīgo definīcijas, kas ir pieejamas ieviešanas avota koda failos.
**`Metožu deklarācija`** — visas metožu deklarācijas ir iekļautas .h galvenes failos, lai tās būtu pieejamas vairākos ieviešanas failos.
**`Neiekļauto funkciju definīcijas`** — galvenes faili var saturēt arī neiekļauto metožu definīcijas.
**`Ziņojumu kartes`** — MFC pirmkoda ieviešanas gadījumā galvenes failā var būt arī ziņojumu kartes. Šādā gadījumā ziņojumu kartes ir saistītas ar funkcionalitātes ieviešanu, kas ir saistīta ar UI elementiem, piemēram, pogai, izvēles rūtiņai, radio pogām utt.

## Atšķirība starp .H un .HH failiem

Acīmredzot starp .h un .hh galvenes failiem nav šādas atšķirības, izņemot ieteicamo veidu, kā tos izmantot attiecīgajām valodām, piemēram, [C](/programming/c/) vai C++. Galvenes failu nosaukšana atbilstoši šīm valodām palīdz tos atšķirt lielā projektā, kas var būt C un C++ ieviešanas kombinācija.

Turklāt, ja galvenes ir atdalītas ar paplašinājumu, jūsu redaktors var automātiski lietot atbilstošu formatējumu.

Kopumā šo divu failu formātu nošķiršana nenodarīs nekādu kaitējumu, bet būs izdevīga, un ir ieteicams ievērot C un C++ atšķiršanu.

### Galvenes sargi

Galvenes faili var radīt sarežģītas kļūdas, ja vienā failā ir iekļautas vairākas deklarācijas, pievienojot citus galvenes failus. Šīs dublētās definīcijas rada kompilatora kļūdas. No šīs problemātiskās situācijas var izvairīties, izmantojot mehānismu, ko sauc par galvenes aizsargu, kas ir nosacījuma kompilācijas direktīvas, kā parādīts tālāk.

```
#ifndef ANY_UNIQUE_NAME_HERE_HPP
#define ANY_UNIQUE_NAME_HERE_HPP

// your declarations (and certain types of definitions) here

#endif
```
Izmantojot šo galveni, priekšapstrādātājs pārbauda, vai ANY_UNIQUE_NAME_HERE_HPP jau ir definēts. Ja galvene tiek atkārtoti iekļauta vienā failā, galvenes saturs tiks ignorēts.

## Atsauces

* [Header Filers — Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

* [Atšķirība starp .h un .hh failu formātiem](https://stackoverflow.com/questions/10354321/c-reason-why-using-hh-as-extension-for-c-header-files)


