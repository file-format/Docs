{
  "date": "2021-06-24",
  "keywords": [
"bat fails",
"kas ir sikspārņu fails",
"failu",
"bat faila piemērs",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par BAT failu formātu un API, kas var izveidot un atvērt BAT failus.",
  "title": "BAT — sērijveida faila formāts",
  "linktitle": "BAT",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ba-lvt"
}
},
  "lastmod": "2021-06-24"
}

## Kas ir BAT fails?
BAT fails ir pazīstams kā sērijveida fails, kas darbojas ar DOS un visām Windows versijām, izmantojot cmd.exe. Tas sastāv no virknes rindu komandu vienkāršā tekstā, kas jāizpilda komandrindas tulkam, lai veiktu dažādus uzdevumus, piemēram, palaistu apkopes utilītas sistēmā Windows vai palaistu tipiskas programmas. Pakešdatnē var būt ietverta jebkura komanda, ko tulks var pieņemt interaktīvi, un izmantot koda struktūru, kas nodrošina nosacītu sazarojumu un cilpu, kā rakstīts sērijveida failā.
## BAT faila formāts
BAT faila formāts ir vienkārši skripts, kas iekļauts, lai automatizētu komandu secības, kurām ir atkārtots raksturs. Termins partija tiek izmantots pakešu apstrādei, to var uzskatīt par neinteraktīvu izpildi. Tāpēc sērijveida fails var neapstrādāt vairāku datu partiju. Vecajā diska operētājsistēmā (DOS) sērijveida fails tika palaists zem komandrindas saskarnes, ierakstot faila nosaukumu un paplašinājumu .bat. Iepriekšējā Microsoft grafiskā interfeisa operētājsistēma, piemēram, Microsoft Windows, bija atkarīga no DOS. Lietotājiem bija jāizmanto DOS, lai veiktu tipiskas darbības, piemēram, labotu, optimizētu vai pārinstalētu Windows. Vēlāk Microsoft ieviesa Windows NT, kas nebija atkarīga no DOS operētājsistēmas. Tāpēc sērijveida failus var palaist, izmantojot komandu uzvedni vai **cmd.exe** mūsdienu Microsoft operētājsistēmās.
### Pakešfaila parametri
Komandu uzvedne atbalsta vairākus īpašus mainīgos, piemēram, **%0, %1 līdz %9**, lai atsauktos uz pakešdarba nosaukumu un ceļu un deviņiem izsaukšanas parametriem no pakešdarba. Neesošie parametri tiek aizstāti ar virkni, kuras garums ir nulle. Lai gan tos var izmantot līdzīgi kā vides mainīgajiem, taču tie netiek saglabāti vidē. Microsoft un IBM atsaucas uz šiem mainīgajiem kā aizvietošanas parametriem, savukārt Novell, Digital Research un Caldera tiem ieviesa terminu aizstāšanas mainīgie.

Šeit ir dažas noderīgas pakešfaila komandas:
| Komanda | Apraksts |
------|------------|
| VER | Šī pakešu komanda parāda izmantoto MS-DOS versiju. |
|ASSOC| Šī ir pakešu komanda, kas saista paplašinājumu ar faila tipu (FTYPE), parāda esošās asociācijas vai dzēš saiti. |
|CD| Šī pakešu komanda palīdz veikt izmaiņas citā direktorijā vai parāda pašreizējo direktoriju. |
|CLS| Šī pakešu komanda notīra ekrānu. |
|KOPIJA| Šo pakešu komandu izmanto failu kopēšanai no vienas vietas uz otru. |
|DEL| Šī pakešu komanda dzēš failus, nevis direktorijus. |
|DIR| Šī pakešu komanda uzskaita direktorija saturu. |
|DATE| Šī pakešu komanda palīdz atrast sistēmas datumu. |
|ECHO| Šī pakešu komanda parāda ziņojumus vai ieslēdz vai izslēdz komandu atbalsi. |
|IZIET| Šī pakešu komanda iziet no DOS konsoles. |
|MD| Šī pakešu komanda izveido jaunu direktoriju pašreizējā atrašanās vietā. |
|PĀRVIETOT| Šī pakešu komanda pārvieto failus vai direktorijus starp direktorijiem. |
|PATH| Šī partijas komanda parāda vai iestata ceļa mainīgo. |
|PAAUZE| Šī pakešu komanda pieprasa lietotājam un gaida, līdz tiks ievadīta ievades rinda. |
|PROMPT| Šo pakešu komandu var izmantot, lai mainītu vai atiestatītu uzvedni cmd.exe. |
|RD| Šī pakešu komanda noņem direktorijus, taču pirms to noņemšanas direktorijiem ir jābūt tukšiem. |
|REN| Pārdēvē failus un direktorijus |
|REM| Šo pakešu komandu izmanto piezīmēm pakešdatnēs, neļaujot izpildīt piezīmes saturu. |
|SĀKT| Šī pakešu komanda palaiž programmu jaunā logā vai atver dokumentu. |
|TIME| Šī pakešu komanda iestata vai parāda laiku. |
|TIPS| Šī pakešu komanda izdrukā faila vai failu saturu izvadē. |
|VOL| Šī partijas komanda parāda sējuma etiķetes. |
|ATTRIB| Parāda vai iestata failu atribūtus pašreizējā direktorijā |
|CHKDSK| Šī pakešu komanda pārbauda, vai diskā nav problēmu. |
|IZVĒLE| Šī pakešu komanda nodrošina lietotājam opciju sarakstu. |
|CMD| Šī pakešu komanda izsauc citu komandu uzvednes gadījumu. |
|COMP| Šī pakešu komanda salīdzina 2 failus, pamatojoties uz faila lielumu. |
|KONVERTĒT| Šī pakešu komanda konvertē sējumu no FAT16 vai FAT32 failu sistēmas uz NTFS failu sistēmu. |
|DRIVERQUERY| Šī pakešu komanda parāda visus instalētos ierīču draiverus un to rekvizītus. |
|IZPLATĪT| Šī pakešu komanda izvelk failus no saspiestiem .cab kabineta failiem. |
|ATKLĀT| Šī pakešu komanda meklē virkni failos vai ievadē, izvadot atbilstošas rindas. |
|FORMAT| Šī pakešu komanda formatē disku, lai izmantotu Windows atbalstīto failu sistēmu, piemēram, FAT, FAT32 vai NTFS, tādējādi pārrakstot iepriekšējo diska saturu. |
|PALĪDZĪBA| Šī pakešu komanda parāda Windows nodrošināto komandu sarakstu. |
|IPCONFIG| Šī pakešu komanda parāda Windows IP konfigurāciju. Parāda konfigurāciju pēc savienojuma un šī savienojuma nosaukumu. |
|LABEL| Šī pakešu komanda pievieno, iestata vai noņem diska etiķeti. |
|VAIRĀK| Šī pakešu komanda parāda faila vai failu saturu pa vienam ekrānam. |
|NET| Nodrošina dažādus tīkla pakalpojumus atkarībā no izmantotās komandas. |
|PING| Šī pakešu komanda nosūta ICMP/IP atbalss paketes tīklā uz norādīto adresi. |
|IZSLĒGT| Šī pakešu komanda izslēdz datoru vai izslēdz pašreizējo lietotāju. |
|ŠĶIROT| Šī pakešu komanda ņem ievadi no avota faila un sakārto tā saturu alfabētiskā secībā no A līdz Z vai Z līdz A. Tā izdrukā izvadi konsolē. |
|SUBST| Šī pakešu komanda piešķir diska burtu vietējai mapei, parāda pašreizējos uzdevumus vai noņem uzdevumu. |
|SISTĒMA| Šī pakešu komanda parāda datora un tā operētājsistēmas konfigurāciju. |
|TASKKILL| Šī pakešu komanda pabeidz vienu vai vairākus uzdevumus. |
|UZDEVUMU SARAKSTS| Šajā pakešu komandā ir uzskaitīti uzdevumi, tostarp uzdevuma nosaukums un procesa ID (PID). |
|XCOPY| Šī pakešu komanda kopē failus un direktorijus uzlabotā veidā. |
|KOKS| Šī pakešu komanda parāda visu pašreizējā direktorija apakšdirektoriju koku jebkuram rekursijas vai dziļuma līmenim. |
|FC |Šī pakešu komanda uzskaita faktiskās atšķirības starp diviem failiem. |
|DISKPART |Šī pakešu komanda parāda un konfigurē diska nodalījumu rekvizītus. |
|TITLE |Šī pakešu komanda iestata virsrakstu, kas tiek rādīts konsoles logā. |
|SET | Parāda pašreizējās sistēmas vides mainīgo sarakstu. |

## BAT faila piemērs
Pakešu skripti parasti tiek saglabāti kā vienkārši teksta faili; kas satur komandas, kas tiek izpildītas pēc kārtas. Šie faili tiek saglabāti ar paplašinājumu .bat; atpazīts un izpildīts, izmantojot **Command Interpreter** programmatūru. Šī programmatūra sākotnēji ir pieejama operētājsistēmā Microsoft Windows ar nosaukumu **cmd.exe**.

Šeit ir partijas skripta paraugs, kas izdzēš visus pašreizējā direktorijā esošos failus:
```
:: Deletes All files in the Current Directory With Prompts and Warnings
::(Hidden, System, and Read-Only Files are Not Affected)
:: @ECHO OFF
DEL . DR
```


## Atsauces 

* [Pakešu skripts — Īsā rokasgrāmata](https://www.tutorialspoint.com/batch_script/batch_script_quick_guide.htm)

* [Pakešfails — Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)


