{
  "date": "2019-10-11",
  "keywords": [
"txt failu",
"txt faila formātā",
"kas ir txt fails",
"failu",
"txt piemērs",
"txt faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TXT — teksta dokumenta fails",
  "description": "Uzziniet par TXT faila formātu un API, kas var izveidot un atvērt TXT failus.",
  "linktitle": "TXT",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-tx-lvt"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir TXT fails?

Fails ar paplašinājumu .TXT ir teksta dokuments, kas satur vienkāršu tekstu rindiņu veidā. Teksta dokumenta rindkopas tiek atpazītas pēc karietes atgriešanas un tiek izmantotas faila satura labākai sakārtošanai. Standarta teksta dokumentu var atvērt jebkurā teksta redaktorā vai tekstapstrādes lietojumprogrammā dažādās operētājsistēmās. Viss šādā failā esošais teksts ir cilvēkiem lasāmā formātā un attēlots ar rakstzīmju secību.

Teksta faili var uzglabāt lielu datu apjomu, jo satura lielums nav ierobežots. Tomēr teksta redaktoriem, kas atver tik lielus failus, ir jābūt gudriem, lai tos ielādētu un parādītu. Gandrīz visās operētājsistēmās ir teksta redaktori, kas ļauj izveidot un rediģēt teksta failus. Piemēram, šim nolūkam operētājsistēmai Windows OS ir pievienots Notepad un Wordpad. Tāpat MacOS ir aprīkots ar TextEdit teksta dokumentu izveidei un rediģēšanai. Tomēr internetā ir pieejami arī citi bezmaksas teksta redaktori, kas nodrošina iespēju strādāt ar teksta dokumentiem, piemēram, Notepad++, kas ir daudz progresīvāks funkcionalitātes ziņā.

## Faila formāta specifikācijas ##

Teksta faila formātam nav īpašu faila formāta specifikāciju. Teksta failiem ir text/plain MIME tips, un tiem ir maz formatējuma vai vispār nav formatējuma. Tas ļauj teksta redaktoriem atvērt šādus failus bez jebkādām citām prasībām. Teksta failu noklusējuma rakstzīmju kopa ir ASCII, ko izmanto teksta faila satura izveidei un parādīšanai. Rakstzīmes tiek kodētas, izmantojot ASCII rakstzīmju kopu, taču tas ierobežo tādu rakstzīmju kā mārciņas zīme, dolāra un eiro zīme, kuras nevar attēlot, izmantojot ASCII rakstzīmju kopu, izmantošanu. Tādējādi teksta failus var saglabāt arī Unikoda formātā, un visbiežāk tiek izmantots UTF-8.

### Windows teksta faila formāts ###

Teksta faili operētājsistēmā Windows OS sastāv no vairākām rindiņām, kur katra rinda sastāv no rakstzīmju secības. Katra lietotāja norādītā rinda ir definēta ar divu rakstzīmju kombināciju, ti, pārvadājuma atgriešana (CR) un rindas plūsma (LF). Windows teksta faili var būt ANSI, OEM, Unicode vai UTF-8 kodējumā. UTF-16 kodējums palīdz saglabāt informāciju teksta failā, kura attēlošanai nepieciešami divi baiti. Šādi faili parasti sākas ar baitu secības atzīmi (BOM), kas paziņo faila satura endianness. Jāņem vērā, ka citas lietojumprogrammas operētājsistēmā Windows OS var saglabāt informāciju teksta faila formātā, bet ar dažādiem faila paplašinājumiem, lai attēlotu lietojumprogrammas tekstu. Piemēram, programmēšanas valodas parasti saglabā kodu teksta failā, bet ar saviem paplašinājumiem.

### Unix teksta faila formāts ###

Visās šādās sistēmās teksta fails tiek piemērots kā fails, kura rakstzīmes ir sakārtotas nulle vai vairāk rindās. Katra rinda ir nulles vai vairāku rakstzīmju, kas nav jaunas rindiņas rakstzīmes, secība un beigu rindiņas rakstzīme, parasti LF.

## Atsauces Nr.

* [TXT faila formāts](https://en.wikipedia.org/wiki/Text_file)


