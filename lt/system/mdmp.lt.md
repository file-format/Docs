{
  "date": "2022-08-19",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MDMP failas – „Windows Minidump“ failo formatas",
  "description": "Sužinokite apie MDMP failo formatą ir API, kurios gali kurti ir atidaryti MDMP failus.",
  "linktitle": "MDMP",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-mdm-ltp"
}
},
  "lastmod": "2022-08-19"
}

## Kas yra MDMP failas?

MDMP failas yra programos Microsoft Windows atminties iškrova, kuri sukuriama, kai programa užsidaro neįprastai arba sugenda. Jame yra informacijos ir duomenų išklotinės, kurios gali būti naudojamos gedimo priežasčiai derinti. MDMP failai taikomi programoms, sukurtoms bet kurios platformos, pvz., Java, C++, .NET ir kt. Be MDMP,

Programos, kurios gali atidaryti MDMP failus, apima Microsoft Visual Studio Debugger.

## MDMP failo formatas

MDMP failai išsaugomi kaip dvejetainiai failai diske ir gali būti atidaryti naudojant Microsoft Visual Studio derinimo programą. Jame pateikiama ši informacija, padedanti nustatyti avarijos priežastį.

 * Išsami informacija apie sustabdymo pranešimą, jo parametrus ir kitus duomenis
 * Įkeltų tvarkyklių sąrašas
 * Procesoriaus kontekstas (PRCB), skirtas procesoriaus, kuris nustojo veikti
 * Proceso informacija ir branduolio kontekstas (EPROCESS), skirtas sustabdytam procesui
 * Apdorokite sustojusios gijos informaciją ir branduolio kontekstą (ETHREAD).
 * Branduolio režimo skambučių krūva, skirta gijai, kuri sustojo

Ši informacija padeda išsiaiškinti, kas atsitiko, išspręsti problemą ir išvengti jos pasikartojimo.

### Analizuoti Minidump

Windows reikalauja, kad įkrovos tome būtų ieškos failas, kad būtų sukurtas atminties iškelties failas. Puslapio failas sukuriamas įkrovos tome ir turi būti bent 2 megabaitų (MB) dydžio. Iškelties failas sukuriamas, kai programa užstringa. Iškilus antrai problemai, sukuriamas antras mažas atminties iškelties failas, o ankstesnis išsaugomas. Iškelties failo pavadinimas yra skirtingas, kad būtų išvengta perrašymo.

Windows saugo visų atminties ištrynimo failų sąrašą aplanke %SystemRoot%\Minidump. Galite analizuoti MDMP failus paleisdami juos Visual Studio Debugger, kaip nurodyta toliau nurodytuose veiksmuose.

## Kaip atidaryti MDMP failą „Visual Studio“?

Norėdami atidaryti MDMP failą Visual Studio, galite atlikti šiuos veiksmus.

 * Visual Studio meniu Failas pasirinkite Atidaryti | Avarijos sąvartynas.
 * Eikite į iškelties failą, kurį norite atidaryti.
 * Pasirinkite Atidaryti.

## Nuoroda

* [Kaip nuskaityti nedidelį „Windows“ sukurtą atminties išklotinės failą, jei įvyksta strigtis](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump -failas)


