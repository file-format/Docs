{
  "date": "2021-07-07",
  "keywords": [
"INI",
"pagarinājumu",
"failu",
"formātā",
"sistēma",
"Iniciācija",
"direktorija paplašinājums",
"programmas",
"dators",
"pieteikumu"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "INI — iniciācijas faila formāts",
  "description": "Uzziniet par INI faila formātu un API, kas var izveidot un atvērt INI failus.",
  "linktitle": "INI",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-in-lvi"
}
},
  "lastmod": "2021-07-07"
}

## Kas ir INI fails? ##

INI fails ir ziņojumu konfigurācijas dokuments datorprogrammām, kurās ir publiskās atslēgas raksturlielumiem un sadaļām, kas organizē atribūtus ietvarā un gramatikā. Šie sistēmas faila formāta konfigurācijas dokumenti savu nosaukumu iegūst no MS-DOS operētājsistēmas direktorija paplašinājuma INI, kas apzīmē iniciāciju. Tā popularizēja šo programmatūras iestatīšanas veidu. Daudzas programmas citās lietojumprogrammās izmanto dažādus failu nosaukumu papildinājumus, piemēram, CONF un [CFG](/system/cfg/), lai gan formāts daudzās konfigurācijas situācijās ir izveidojis neoficiālu standartu.

## Īsa INI failu vēsture ##

Sākotnēji Windows galvenā programmas konfigurācijas metode bija teksta faila formāts, kas sastāvēja no teksta rindiņām ar vienu būtisku pāri katrā rindā, kas sadalīta sadaļās. Šajā formātā tika saglabāti ierīču draiveri, burtveidoli un palaišanas programmas. Atsevišķus iestatījumus lietotnes parasti saglabāja arī INI failos.
Līdz operētājsistēmai Windows 3.1x šis formāts tika atbalstīts 16 bitu Microsoft Windows platformās. Sākot ar Windows 95, Microsoft sāka mudināt izstrādātājus konfigurēšanai izmantot Windows reģistru, nevis INI failus.

## INI fails — faila formāta specifikācijas

### Taustiņi/īpašības ###

Atslēga/īpašums ir visvienkāršākais INI faila elements. Vienādības simbols (=) atdala katras atslēgas nosaukumu un vērtību. Pa kreisi no vienādības zīmes ir vieta, kur tiek parādīts nosaukums. Vienādības simbols un semikols ir diskrēti burti Windows sistēmā, tāpēc tos nevar izmantot atslēgā. Vērtībā var izmantot jebkuru rakstzīmi.

```
name=value
```

### Sadaļas ###

Sadaļas komentārs tiek parādīts kvadrātiekavās ([]) savā rindā. Pēc sadaļas definīcijas visas atslēgas ir saistītas ar šo sadaļu. Sadaļas beidzas pie nākamā sadaļas apzīmējuma vai dokumenta beigām; nav īpaša sadaļas beigu atdalītāja. Sadaļas nevar sakraut; tos var nosaukt tikai vienreiz, un tie nav jāsaista.

```
[section]
a=a
b=b
```

### Funkcijas maiņa ###

INI faila formātam nav globāli pieņemtas definīcijas. Daudzas datoru lietojumprogrammas ietver funkcijas papildus jau minētajām. Tālāk esošajā sarakstā ir iekļauti daži izplatīti raksturlielumi, kas var būt vai nebūt iekļauti jebkurā atsevišķā programmā.

* Komentāri

* Bēgšanas varoņi 

* Dublēti vārdi 



## INI piemērs ##

INI faila paraugs izskatās šādi:

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

## Atsauce Nr.

* [DMP — Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)


