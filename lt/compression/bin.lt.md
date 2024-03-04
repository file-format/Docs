{
   "date":"2023-07-20",
   "keywords":[
"BIN",
"BIN failas",
"failą",
"BIN failo plėtinys",
"pratęsimas",
"failą"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"BIN failo formatas – MacBinary koduotas failas",
   "description":"Sužinokite apie BIN formatą ir API, kurios gali kurti ir atidaryti BIN failus.",
   "linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"compression-bin-lt",
         "parent":"compression"
}
},
   "lastmod":"2023-07-20"
}

## Kas yra BIN failas?

Macintosh kompiuterių kontekste BIN failas gali reikšti failą, išsaugotą MacBinary formatu. MacBinary yra failo formatas, specialiai sukurtas perkelti Macintosh failus internetu, el. paštu, FTP ar nešiojamomis laikmenomis. MacBinary tikslas yra išsaugoti visą Macintosh failų struktūrą ir atributus, įskaitant duomenų šakutę ir išteklių šakutę, viename faile.

MacBinary formatu tai pasiekiama įtraukiant Macintosh hierarchinės failų sistemos (HFS) išteklių šakutę ir duomenų šakutę į suglaudintą failą. Jame taip pat yra ieškiklio antraštė, kurioje yra svarbūs failo metaduomenys. Sujungdama visus šiuos komponentus į vieną failą, MacBinary užtikrina, kad failas išlaikys vientisumą ir gali būti lengvai perkeltas bei bendrinamas skirtingose platformose.

Tobulėjant Apple failų sistemoms ir failų perdavimo protokolams, BIN failų ir MacBinary formato naudojimas tapo retesnis. Įdiegus tokius failų formatus kaip ZIP ir perėjus prie modernesnių failų sistemų, tokių kaip HFS+ ir APFS, sumažėjo MacBinary koduotų failų poreikis. Šios naujesnės failų sistemos suteikia veiksmingesnius būdus tvarkyti failų atributus, išteklių šakutes ir duomenų šakutes, todėl MacBinary formatas yra mažiau reikalingas šiandienos skaičiavimo aplinkoje.

## BIN failo formatas – daugiau informacijos 

Pirmosiomis Macintosh kompiuterių dienomis failai buvo saugomi dviejose atskirose šakėse dėl duomenų apribojimų. Išteklių šakutėje buvo struktūrizuoti duomenys, o duomenų šakoje buvo nestruktūrizuoti duomenys. Nors klasikinė Mac OS šias šakes traktavo kaip vieną failą, failų perkėlimas į ne Mac sistemas lėmė duomenų praradimą, nes jos neatpažino šakių kaip vieno objekto. Norėdami tai išspręsti, MacBinary formatą sukūrė tokie asmenys kaip Dennis Brothers, Harry Chesley ir Yves Lempereur. MacBinary suspaudė ir sujungė šakutes į vieną failą, žinomą kaip BIN failas, skirtas perkelti į ne Mac sistemas. Grįžus prie Mac OS, šakės vėl bus atskirtos. 2000-aisiais atsisakius šakėmis pagrįsto HFS, MacBinary formato naudojimas labai sumažėjo. Šiandien MacBinary koduotą BIN failą aptinkate retai, nebent aptinkate seną failą ne Mac sistemoje arba atsisiunčiate jį iš interneto.

The MacBinary format has gone through several versions over time to accommodate changes in Macintosh systems and file handling. Here are some of the different versions of the MacBinary format:

- **MacBinary I:** pradinė MacBinary versija, pristatyta devintojo dešimtmečio pabaigoje. Jis sujungė išteklių šakutę ir duomenų šakutę į vieną dvejetainį failą, leidžiantį perkelti Macintosh failus į kelias platformas.

- **MacBinary II:** ši versija, išleista 1990-ųjų pradžioje, patobulino pradinį MacBinary formatą, į dvejetainio failo antraštę įtraukdama papildomos informacijos, pvz., failo tipą ir kūrėjo kodus. Šie kodai padėjo išlaikyti Macintosh failų vientisumą ir identifikavimą perdavimo metu.

- **MacBinary III:** The MacBinary III format, introduced in the mid-1990s, further enhanced the previous versions by including additional metadata, such as file name and file creation and modification dates, in the binary file's header. This allowed for more comprehensive preservation of Macintosh file attributes during transfer.

- **MacBinary IV:** MacBinary IV buvo sukurtas siekiant išspręsti suderinamumo problemas su besiformuojančia Mac OS X operacine sistema 2000-ųjų pradžioje. Į jį įtraukti pakeitimai, siekiant prisitaikyti prie naujos failų sistemos struktūros ir atributų, įdiegtų Mac OS X.

## Kaip atidaryti BIN failą?

MacBinary Encoded BIN failus galima atidaryti naudojant įvairias glaudinimo priemones. MacOS naudotojams tinka **Apple Archive Utility**. Windows vartotojai gali naudoti programinę įrangą, pvz., **Smith Micro StuffIt Deluxe**, norėdami išgauti MacBinary Encoded BIN failo turinį. Kita MacOS naudotojų parinktis yra **The Unarchiver**, kuri yra universalus įrankis, galintis tvarkyti kelis failų formatus, įskaitant MacBinary.

Svarbu pažymėti, kad .bin failo plėtinį naudoja įvairūs failų formatai, ne tik MacBinary. Todėl, jei susiduriate su BIN failu, kurio negalima atidaryti naudojant anksčiau minėtas priemones, jis gali būti išsaugotas kitu formatu. Tokiais atvejais gali tekti nustatyti konkretų failo formatą ir naudoti atitinkamą programinę įrangą arba programinę įrangą, sukurtą tam formatui, kad pasiektumėte failo turinį.

## Kas yra „Macbinary“ archyvas?

MacBinary archyvas yra failo formatas, skirtas ankstyviesiems Macintosh kompiuteriams, skirtas Macintosh failų dviejų šakių struktūrai. Macintosh failų sistemas sudaro duomenų šakutė ir išteklių šakutė, kurioje duomenys ir metaduomenys laikomi atskirai. Siekiant palengvinti kelių sistemų suderinamumą ir tinklo perdavimą, MacBinary užkoduoja abi šakutes į vieną dvejetainį failą. Šis formatas išsaugo duomenų ir susijusių išteklių vientisumą perkeliant į ne Macintosh sistemas.

## Ar galiu ištrinti Macbinary archyvą?

Taip, galite ištrinti MacBinary archyvo failus, jei jums jų nebereikia arba jei ištraukėte turinį ir išsaugojote juos kitu formatu. MacBinary archyvai yra tiesiog būdas supakuoti Macintosh failus konkretiems tikslams, pvz., perkėlimui iš kelių sistemų ar saugojimui. Archyvo ištrynimas neturi įtakos jame esantiems failams.

## Kaip atidaryti „Macbinary“ archyvą „iPhone“?

Norint atidaryti MacBinary archyvą iPhone, gali reikėti naudoti trečiųjų šalių programas, nes iOS nepalaiko šio formato.

## „Macbinary“ archyvo ištrauka – kaip ištraukti „Macintosh Bin“ failus?

Norėdami išgauti MacBinary (bin) failus šiuolaikiniame kompiuteryje, paprastai naudokite failų išskleidimo priemonę arba programinę įrangą, kuri palaiko šį formatą.

Sistemoje Windows naudokite failų archyvavimo įrankį, kuris palaiko MacBinary failus. Populiarios parinktys yra WinRAR, 7-Zip arba WinZip.

Mac OS yra su integruota archyvavimo programa, galinčia tvarkyti įvairius archyvo formatus, įskaitant MacBinary. Raskite MacBinary failą Finder. Dukart spustelėkite MacBinary failą. Archyvavimo programa turėtų automatiškai paleisti ir išskleisti turinį. Kai išskyrimas bus baigtas, ištrauktus failus galėsite rasti toje pačioje vietoje kaip ir originalus MacBinary failas arba nurodytoje paskirties vietoje.

## Kiti BIN failai

Štai kiti failų tipai, kuriuose naudojamas **.bin** failo plėtinys.

- [BIN - Binary Disc Image File](/disc-and-media/bin/)
- [BIN - Unix Executable File](/executable/bin/)
- [BIN - BlackBerry IT Policy File](/settings/bin/)
- [BIN - Sega Genesis Game ROM](/game/bin/)
- [BIN - PSX PlayStation BIOS Image](/game/bin-pcsx/)

## Nuorodos

* [MacBinary](https://en.wikipedia.org/wiki/MacBinary)


