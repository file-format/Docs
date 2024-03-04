{
  "date": "2023-07-12",
  "keywords": [
"exp",
"exp failą",
"kas yra exp mpeg failas",
"Kaip atidaryti exp failą",
"failą",
"exp failo plėtinys",
"pratęsimas"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "EXP failo formatas – simbolių eksporto failas",
  "description": "Sužinokite apie EXP formatą ir API, kurios gali kurti ir atidaryti EXP failus.",
  "linktitle": "EXP",
  "menu": {
    "docs": {
      "identifier": "programming-exp-lt",
      "parent": "programming"
}
},
  "lastmod": "2023-07-12"
}

## Kas yra EXP failas?

EXP failą, kuris reiškia simbolių eksporto failą, generuoja integruota kūrimo aplinka (IDE) arba kompiliatorius. Šiame faile yra dvejetainė informacija apie eksportuotus duomenis ir funkcijas. Jos tikslas – sukurti ryšį tarp programos, iš kurios ji kilo, ir kitos programos, padedant jas susieti. EXP failai atlieka lemiamą vaidmenį palengvinant sklandų skirtingų programinės įrangos programų integravimą ir bendradarbiavimą.

## EXP failo formatas – daugiau informacijos

Kai programai reikia sąveikauti su kita programa importuojant ir eksportuojant duomenis, būtina sukurti ryšį naudojant importavimo biblioteką ir eksporto failą. Šis ryšys yra labai svarbus sprendžiant apykaitines importo priklausomybes, kurios gali atsirasti tarp programų.

Apvalus importavimas vyksta, kai programa A priklauso nuo tam tikrų duomenų arba funkcijų iš programos B, o programa B taip pat priklauso nuo duomenų arba funkcijų iš programos A. Ši abipusė priklausomybė gali sukelti problemų programinės įrangos kūrimo proceso susiejimo etape.

Norint išspręsti cirkuliacinį importą, įprastas būdas yra naudoti .LIB failą (importo biblioteką) ir EXP failą (eksporto failą), kai susiejamos programos. LIB failas naudojamas kaip importavimo biblioteka, teikianti reikiamą informaciją, kad programa A galėtų pasiekti reikiamus duomenis arba funkcijas iš programos B. Kita vertus, EXP failas veikia kaip eksporto failas, kuriame yra atitinkama simbolių informacija, kurią eksportuoja programa B. vartoti pagal programą A.

Susiejimo proceso metu naudojant LIB failą ir EXP failą, galima išspręsti žiedinio importavimo priklausomybes. Programa A gali sėkmingai importuoti reikiamus elementus iš programos B per importavimo biblioteką, o programa B gali eksportuoti reikiamus simbolius, kuriuos programa A gali pasiekti per eksportavimo failą.

## EXP failų paskirtis ir naudojimas programinės įrangos kūrime

EXP failai pirmiausia yra susiję su programinės įrangos kūrimu ir yra naudojami kartu su įvairiomis programavimo kalbomis ir kūrimo įrankiais. Kai kurios įprastos programinės įrangos ir įrankių, susijusių su EXP failais, yra:

– **Kompiliatoriai:** Kompiliatoriaus programinė įranga, pvz., GCC (GNU Compiler Collection) arba Microsoft Visual C++, gali generuoti EXP failus kaip kompiliavimo proceso dalį. EXP failuose yra simbolių informacijos, kuri padeda susieti ir derinti.
- **Linkers:** Linkeriai, tokie kaip GNU ld (Linker) arba Microsoft Linker, naudoja EXP failus, kad išspręstų simbolių nuorodas ir užmegztų ryšius tarp skirtingų kodo modulių susiejimo proceso metu.
– **Integruotos kūrimo aplinkos (IDE):** IDE, pvz., Visual Studio, Eclipse arba Xcode, dažnai turi integruotą palaikymą darbui su EXP failais. Jie suteikia simbolių informacijos valdymo, derinimo ir susiejimo funkcijų, naudojant EXP failus užkulisiuose.
– **Debuggers:** Derinimo įrankiai, tokie kaip GDB (GNU Debugger) arba WinDbg, naudoja EXP failus, kad susietų atminties adresus su šaltinio kodo simboliais, kad kūrėjai galėtų efektyviai derinti savo programas.
– **Profiliai:** Profiliavimo įrankiai, pvz., Intel VTune arba Visual Studio Profiler, gali naudoti EXP failus, kad profiliavimo proceso metu susietų našumo duomenis su konkrečiomis funkcijomis arba kodo regionais.

## Kaip atidaryti EXP failą?

EXP failai, kurie yra simbolių eksporto failai, paprastai nėra skirti tiesiogiai atidaryti ar peržiūrėti galutiniams vartotojams. Jas pirmiausia naudoja kūrėjai ir kuria įrankius kompiliavimo, susiejimo ir derinimo procesų metu.

EXP failai paprastai apdorojami automatiškai kūrimo įrankiais arba integruojami į kūrimo sistemą. Jie naudojami kaip nuoroda kompiliatoriui, susiejimui, derintuvui ar profiliuotojui, siekiant išspręsti simbolių nuorodas, susieti atminties adresus su šaltinio kodo elementais ir palengvinti kodo modulių susiejimą.

Jei esate kūrėjas, dirbantis su EXP failu, jums paprastai nereikia rankiniu būdu atidaryti paties failo ar su juo sąveikauti. Vietoj to turėtumėte pasikliauti kūrimo įrankiais arba programavimo aplinkomis, kurios viduje naudoja EXP failą atitinkamiems tikslams, pvz., susiejimui, derinimui ar profiliavimui.

## Nuorodos
* [.Exp Files as Linker Input](https://learn.microsoft.com/en-us/cpp/build/reference/dot-exp-files-as-linker-input?view=msvc-170)


