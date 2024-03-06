{
  "date": "2021-09-14",
  "keywords": [
"mrc",
"failu",
"pagarinājumu",
"faila formātā",
"mrc ieviešana",
"Programmēšanas rokasgrāmata",
"mrc piemērs",
"mIRC",
"mIRC skriptu valoda",
"INI faili",
"mSL skriptu valoda",
"mIRC valoda",
"mIRC skripti",
"skriptu valoda"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "MRC — mIRC skriptu valodas fails",
  "description": "Uzziniet par MRC faila formātu un API, kas var izveidot un atvērt MRC failus.",
  "linktitle": "MRC",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-mr-lvc"
}
},
  "lastmod": "2021-09-14"
}

## Kas ir MRC fails?

mIRC ir skriptu valoda, kas ir iegulta kā IRC klients (Internet Relay Chat) operētājsistēmā Windows. Tas nodrošina aizsardzību pret surogātpasta sūtīšanu personiskai un kanālu lietošanai. Lai nodrošinātu labāku lietotāju saderības pieredzi, šī mIRC skriptu valoda ļauj izveidot dialoga logus. Faili, kas satur skriptus, galvenokārt vienkārša teksta formātā, tiek glabāti ar paplašinājumu MRC vai kā [INI](/system/ini/) faili. Šīs valodas funkcijas ir zināmas kā komandas un identifikatori (kad tie atgriež vērtību).

mIRC valoda nodrošina vairāku skriptu failu ielādi vienlaikus. No otras puses, viens fails var izraisīt tā, ka otrs vairs netiek izmantots, ja tas tiek ielādēts vienlaikus. Komandas tiek saglabātas, un tās var pastāvēt IRC automātiski. Šajā valodā izmantotajās komandās un aizstājvārdos nav nevienas rakstzīmes prioritātes.

mIRC tiek plaši izmantots, lai roboti automātiski pārvaldītu kanālu, taču to var mainīt arī mSL skriptu valoda. Tas var ieviest daudzas jaunas funkcijas, piemēram, makro, mūzikas atskaņošanas iespējas, mazus makro un funkcijas, pamata spēles vai mazu lietojumprogrammu darbību.


## Īsa vēsture ##

Šo skriptu valodu pirmo reizi 1995. gadā izstrādāja Khaled Adam Bey. Skriptu valodas dizainu arī izveidoja Khalid. Šīs valodas mērķis bija uz notikumu orientēta programmēšana. Sākotnēji šīs programmēšanas valodas failiem izmantotais faila paplašinājums bija .mrc un .ini. Turklāt tas tika izstrādāts saskaņā ar patentētas programmatūras licenci.

## Tehniskā specifikācija Nr.

Dažām funkcijām ir pielāgots skripts, izmantojot šo mIRC valodu, un tās ir pazīstamas kā aizstājvārdi. Kad šie aizstājvārdi atgriež vērtības, tos sauc par pielāgotiem identifikatoriem. Visi šajā mIRC valodā ietvertie mainīgie tiek dinamiski drukāti. Sigilus izmanto mIRC skripti. Vēl viena šīs skriptu valodas iezīme ir uznirstošie logi. Lietotāji var izsaukt uznirstošos logus, vienkārši tos atlasot. Tālvadības pultis ir norādītas noteiktiem notikumiem. Tālvadības pultis tiek izsauktas, kad notiek attiecīgais notikums.

Lai pārtrauktu katru šīs valodas koda rindiņu, tiek izmantoti atstarpi atdalīti marķieri. Ir daži citi populāri paplašinājumi, kas tiek izmantoti mIRC failiem, piemēram, MDX (mIRC Dialog Extension) un DCX (Dialog Control Extension). Abi šie ir dialoga paplašinājumi un ir salīdzinoši populārāki. Uz valodu konstrukcijām attiecas šīs skriptu valodas nomenklatūra. Valoda mIRC ietver dažādus skriptu valodas aspektus, piemēram, lokālos un globālos mainīgos, bināros mainīgos, hash tabulas un failu apstrādi.


## MRC faila formāta piemērs ##

```

;Defines the alias 'hello' in the remote script

;Note: if this is placed in an alias script,
;the 'alias' part must be removed (result: hello {)
;Usage: /hello

alias hello {

  ;Displays(/echo) 'Hello World!' into the active window(-a)
  echo -a Hello World!

}

```

```
;Placed in a remote script

;When a user types Hello! in a channel,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:#:{ msg $chan Hello, $nick $+ ! }

;When a user types Hello! in a private message,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:?: { msg $nick Hello, $nick $+ ! }

;Here is a script which automatically gives voice to a user
;who joins a particular channel (The Bot or user should have HOP)

on *:JOIN:#?: { mode $chan +v $nick }

;A bad word script

on *:Text:die*:#: { .mode $chan +b $nick | kick $chan $nick Dont say that again }

```

## Atsauce Nr.

* [MIRC — Wikipedia](https://en.wikipedia.org/wiki/MIRC_scripting_language)




