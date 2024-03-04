{
  "date": "2021-06-24",
  "keywords": [
"bat failą",
"kas yra šikšnosparnio failas",
"failą",
"bat failo pavyzdys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie BAT failo formatą ir API, kurios gali kurti ir atidaryti BAT failus.",
  "title": "BAT – paketinio failo formatas",
  "linktitle": "BAT",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ba-ltt"
}
},
  "lastmod": "2021-06-24"
}

## Kas yra BAT failas?
BAT failas yra žinomas kaip paketinis failas, veikia su DOS ir visomis Windows versijomis, naudojant cmd.exe. Jį sudaro eilutės komandų paprastu tekstu, kurias turi vykdyti komandų eilutės vertėjas, kad galėtų atlikti įvairias užduotis, pvz., paleisti priežiūros paslaugų programas sistemoje Windows arba paleisti įprastas programas. Paketiniame faile gali būti bet kokia komanda, kurią interpretatorius gali priimti interaktyviai, ir naudoti kodo struktūrą, kuri įgalina sąlyginį šakojimą ir kilpą, kaip parašyta paketiniame faile.
## BAT failo formatas
BAT failo formatas yra tiesiog scenarijus, įtrauktas automatizuoti komandų sekas, kurios yra pasikartojančios. Terminas paketas vartojamas paketiniam apdorojimui, jis gali būti laikomas neinteraktyviu vykdymu. Todėl paketinis failas gali neapdoroti kelių duomenų paketo. Senojoje disko operacinėje sistemoje (DOS) paketinis failas buvo paleistas komandų eilutės sąsajoje įvedant failo pavadinimą ir plėtinį .bat. Ankstesnė Microsoft grafine sąsaja pagrįsta operacinė sistema, tokia kaip Microsoft Windows, priklausė nuo DOS. Vartotojai turėjo naudoti DOS, kad atliktų įprastas operacijas, tokias kaip taisymas, optimizavimas ar iš naujo įdiegimas Windows. Vėliau Microsoft pristatė Windows NT, kuri nepriklausė nuo DOS operacinės sistemos. Todėl paketinius failus galima paleisti naudojant komandų eilutę arba **cmd.exe** šiuolaikinėse Microsoft operacinėse sistemose.
### Paketinio failo parametrai
Komandinė eilutė palaiko daugybę specialių kintamųjų, tokių kaip **%0, %1 iki %9**, kad būtų galima nurodyti paketinės užduoties pavadinimą ir kelią bei devynis iškvietimo parametrus iš paketinės užduoties. Neegzistuojantys parametrai pakeičiami eilute, kurios ilgis lygus nuliui. Nors jie gali būti naudojami panašiai kaip aplinkos kintamieji, bet neišsaugomi aplinkoje. Microsoft ir IBM šiuos kintamuosius vadina pakaitiniais parametrais, o Novell, Digital Research ir Caldera įvedė jiems terminą pakaitiniai kintamieji.

Štai keletas naudingų paketinio failo komandų:
| Komanda | Aprašymas |
------|------------|
| VER | Ši paketinė komanda rodo jūsų naudojamą MS-DOS versiją. |
|ASSOC| Tai paketinė komanda, kuri susieja plėtinį su failo tipu (FTYPE), rodo esamas sąsajas arba ištrina susiejimą. |
|CD| Ši paketinė komanda padeda keisti kitą katalogą arba rodo dabartinį katalogą. |
|CLS| Ši paketo komanda išvalo ekraną. |
|KOPIJA| Ši paketinė komanda naudojama failams kopijuoti iš vienos vietos į kitą. |
|DEL| Ši paketinė komanda ištrina failus, o ne katalogus. |
|DIR| Ši paketinė komanda išvardija katalogo turinį. |
|DATE| Ši paketinė komanda padeda rasti sistemos datą. |
|ECHO| Ši paketinė komanda rodo pranešimus arba įjungia arba išjungia komandų aidą. |
|IŠĖJIMAS| Ši paketinė komanda išeina iš DOS konsolės. |
|MD| Ši paketinė komanda sukuria naują katalogą dabartinėje vietoje. |
|JUDĖTI| Ši paketinė komanda perkelia failus arba katalogus iš vieno katalogo į kitą. |
|KELIAS| Ši paketo komanda rodo arba nustato kelio kintamąjį. |
|PAuzė| Ši paketinė komanda paragins vartotoją ir laukia, kol bus įvesta įvesties eilutė. |
|PROMPT| Šią paketinę komandą galima naudoti norint pakeisti arba iš naujo nustatyti cmd.exe eilutę. |
|RD| Ši paketinė komanda pašalina katalogus, tačiau norint juos pašalinti, jie turi būti tušti. |
|REN| Pervardija failus ir katalogus |
|REM| Ši paketų komanda naudojama pastaboms paketiniuose failuose, neleidžiant vykdyti pastabos turinio. |
|START| Ši paketinė komanda paleidžia programą naujame lange arba atidaro dokumentą. |
|LAIKAS| Ši paketo komanda nustato arba rodo laiką. |
|TIPAS| Ši paketinė komanda išspausdina failo ar failų turinį į išvestį. |
|VOL| Ši partijos komanda rodo tomo etiketes. |
|ATTRIB| Rodo arba nustato failų atributus esamame kataloge |
|CHKDSK| Ši paketo komanda patikrina, ar diske nėra problemų. |
|PASIRINKIMAS| Ši paketinė komanda vartotojui pateikia parinkčių sąrašą. |
|CMD| Ši paketinė komanda iškviečia kitą komandų eilutės egzempliorių. |
|COMP| Ši paketinė komanda palygina 2 failus pagal failo dydį. |
|KONVERT.| Ši paketinė komanda konvertuoja tomą iš FAT16 arba FAT32 failų sistemos į NTFS failų sistemą. |
|DRIVERQUERY| Ši paketinė komanda rodo visas įdiegtas įrenginių tvarkykles ir jų savybes. |
|IŠPLĖSTI| Ši paketinė komanda ištraukia failus iš suspaustų .cab kabineto failų. |
|RASTI| Ši paketinė komanda ieško eilutės failuose arba įvestyje, išvesdama atitinkančias eilutes. |
|FORMATAS| Ši paketo komanda formatuoja diską, kad būtų galima naudoti Windows palaikomą failų sistemą, pvz., FAT, FAT32 arba NTFS, taip perrašant ankstesnį disko turinį. |
|PAGALBA| Ši paketinė komanda rodo Windows pateiktų komandų sąrašą. |
|IPCONFIG| Ši paketinė komanda rodo Windows IP konfigūraciją. Rodo konfigūraciją pagal ryšį ir to ryšio pavadinimą. |
|LABEL| Ši paketo komanda prideda, nustato arba pašalina disko etiketę. |
|DAUGIAU| Ši paketinė komanda rodo failo ar failų turinį po vieną ekraną. |
|NET| Teikia įvairias tinklo paslaugas, priklausomai nuo naudojamos komandos. |
|PING| Ši paketinė komanda siunčia ICMP/IP echo paketus tinkle nurodytu adresu. |
|IŠJUNGTI| Ši paketinė komanda išjungia kompiuterį arba išjungia dabartinį vartotoją. |
|RŪšiuoti| Ši paketinė komanda paima įvestį iš šaltinio failo ir surūšiuoja jos turinį abėcėlės tvarka nuo A iki Z arba Z iki A. Išvestis išspausdinama konsolėje. |
|SUBST| Ši paketinė komanda priskiria disko raidę vietiniam aplankui, rodo dabartinius priskyrimus arba pašalina priskyrimą. |
|SISTEMINFO| Ši paketinė komanda rodo kompiuterio ir jo operacinės sistemos konfigūraciją. |
|TASKKILL| Ši paketinė komanda užbaigia vieną ar daugiau užduočių. |
|UŽDUOTŲ SĄRAŠAS| Šioje paketinėje komandoje pateikiamos užduotys, įskaitant užduoties pavadinimą ir proceso ID (PID). |
|XCOPY| Ši paketinė komanda kopijuoja failus ir katalogus pažangesniu būdu. |
|MEDIS| Ši paketinė komanda rodo visų dabartinio katalogo pakatalogių medį iki bet kokio rekursijos ar gylio lygio. |
|FC |Ši paketinė komanda pateikia faktinius dviejų failų skirtumus. |
|DISKPART |Ši paketinė komanda rodo ir sukonfigūruoja disko skaidinių ypatybes. |
|TITLE |Ši paketo komanda nustato pavadinimą, rodomą konsolės lange. |
|SET | Rodo esamos sistemos aplinkos kintamųjų sąrašą. |

## BAT failo pavyzdys
Paketiniai scenarijai paprastai išsaugomi kaip paprasti tekstiniai failai; su komandomis, kurios vykdomos seka. Šie failai išsaugomi su plėtiniu .bat; atpažįstamas ir vykdomas naudojant **Command Interpreter** programinę įrangą. Ši programinė įranga iš pradžių galima Microsoft Windows pavadinimu **cmd.exe**.

Čia yra paketinio scenarijaus pavyzdys, kuris ištrina visus dabartinio katalogo failus:
```
:: Deletes All files in the Current Directory With Prompts and Warnings
::(Hidden, System, and Read-Only Files are Not Affected)
:: @ECHO OFF
DEL . DR
```


## Nuorodos 

* [Paketinis scenarijus – trumpas vadovas](https://www.tutorialspoint.com/batch_script/batch_script_quick_guide.htm)

* [Paketinis failas – pateikė Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)


