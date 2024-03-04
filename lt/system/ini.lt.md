{
  "date": "2021-07-07",
  "keywords": [
"INI",
"pratęsimas",
"failą",
"formatu",
"sistema",
"Iniciacija",
"katalogo plėtinys",
"programas",
"kompiuteris",
"taikymas"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "INI – inicijavimo failo formatas",
  "description": "Sužinokite apie INI failo formatą ir API, kurios gali kurti ir atidaryti INI failus.",
  "linktitle": "INI",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-in-lti"
}
},
  "lastmod": "2021-07-07"
}

## Kas yra INI failas? ##

INI failas yra pranešimų konfigūracijos dokumentas, skirtas kompiuterinėms programoms, kuriose yra viešieji charakteristikų raktai ir skyriai, kurie tvarko atributus sistemoje ir gramatikoje. Šie sistemos failo formato konfigūracijos dokumentai gavo pavadinimą iš MS-DOS operacinės sistemos katalogo plėtinio INI, kuris reiškia inicijavimą. Ji išpopuliarino šią programinės įrangos sąrankos formą. Daugelis kitų programinės įrangos programų naudoja įvairius failų pavadinimų papildymus, pvz., CONF ir [CFG](/system/cfg/), nors formatas daugelyje konfigūravimo situacijų nustatė neoficialų standartą.

## Trumpa INI failų istorija##

Iš pradžių pagrindinė Windows programos konfigūravimo technika buvo tekstinio failo formatas, kurį sudarė teksto eilutės su viena svarbia pora eilutėje, suskirstytų į skyrius. Įrenginių tvarkyklės, šriftai ir paleidimo priemonės buvo saugomos šiuo formatu. Atskiri nustatymai taip pat dažniausiai buvo saugomi programų INI failuose.
Iki Windows 3.1x šis formatas buvo palaikomas 16 bitų Microsoft Windows platformose. Pradedant nuo Windows 95, Microsoft pradėjo skatinti kūrėjus konfigūruoti naudoti Windows registrą, o ne INI failus.

## INI failas – failo formato specifikacijos

### Raktai / ypatybės ###

Raktas / ypatybė yra pagrindinis INI failo elementas. Lygybės simbolis (=) atskiria kiekvieno rakto pavadinimą ir reikšmę. Kairėje lygybės ženklo pusėje rodomas vardas. Lygybės simbolis ir kabliataškis yra diskretiškos raidės Windows sistemoje, todėl jų negalima naudoti rakte. Vertėje gali būti naudojamas bet koks simbolis.

```
name=value
```

### Skyriai ###

Skilties komentaras rodomas laužtiniuose skliaustuose ([]) atskiroje eilutėje. Po skyriaus apibrėžimo visi klavišai yra susieti su tuo skyriumi. Skyriai baigiami prie kito skyriaus žymėjimo arba dokumento pabaigos; nėra konkretaus skyriklio skyrio pabaigos. Sekcijos negali būti sukrautos; jie gali būti pavadinti tik vieną kartą ir neprivalo būti susieti.

```
[section]
a=a
b=b
```

### Keičiamos funkcijos ###

INI failo formatas neturi visuotinai priimto apibrėžimo. Daugelyje kompiuterių programų yra be jau paminėtų funkcijų. Toliau pateiktame sąraše yra keletas bendrų ypatybių, kurios gali būti įtrauktos arba neįtrauktos į bet kurią atskirą programą.

* Komentarai

* Pabėgimo personažai 

* Pasikartojantys vardai 



## INI pavyzdys Nr.

INI failo pavyzdys atrodo taip:

```
[Settings]
 
#======================================================================
 
# Set detailed log for additional debugging info
 
DetailedLog=1
 
RunStatus=1
 
StatusPort=6090
 
StatusRefresh=10
 
Archive=1
 
# Sets the location of the MV_FTP log file
 
LogFile=/opt/ecs/mvuser/MV_IPTel/log/MV_IPTel.log
 
#======================================================================
 
Version=0.9 Build 4 Created July 11 2004 14:00
 
ServerName=Unknown

```

## Nuoroda ##

* [DMP – „Microsoft“](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)


