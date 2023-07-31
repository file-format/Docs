{
  "date" : "2021-07-08",
  "keywords" :[ "SYS", "extensie", "bestand", "format", "systeem", "Driver", "Systeembestand", "programma's", "computer", "toepassing"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SYS - Systeembestandsindeling",
  "description":"Meer informatie over SYS-bestandsindeling en API's die SYS-bestanden kunnen maken en openen.",
  "linktitle" : "SYS",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## Wat is een SYS-bestand? ##

De SYS-bestanden zijn "Systeembestanden" die worden gebruikt in Windows OS- en MS-DOS-toepassingen. Deze bestanden kunnen niet direct worden geopend en bestaan uit de driver en configuratie van het apparaat. De SYS-bestanden zijn verantwoordelijk voor het bevatten van bestanden met kernfuncties van het besturingssysteem. Deze worden beschouwd als kritieke bestanden van de coureur van het apparaat en kunnen ook worden gebruikt wanneer een probleem met de coureur moet worden opgelost. Deze zijn verantwoordelijk voor het goed functioneren van een computersysteem en de .sys-bestanden moeten correct en volledig zijn.


## Technische specificatie ##

De .sys-bestanden zijn eigenlijk de subset van het [BMP](/nl/image/bmp/)-formaat omdat het alleen specifieke combinaties toestaat. Het gebruikelijke formaat van deze bestanden is zoals LOGOS.SYS, LOGOW.SYS en LOGO.SYS. Alle andere bestanden hebben dit formaat niet.

Deze bestanden worden tijdens de installatie meestal gebruikt in de *C*-directory van Windows. De meeste problemen met apparaatstuurprogramma's worden opgelost door het Windows-besturingssysteem bij te werken. De details en informatie van deze bestanden kunnen worden bekeken met behulp van de ingebouwde programma's van Windows OS. Deze omvatten ook de verwijzingen naar verschillende modules in een besturingssysteem.
Enkele voorbeelden van systeembestanden zijn:

* IO.SYS (deze slaan apparaatstuurprogramma's van het schijfbesturingssysteem op)
* MSDOS.SYS (Deze bevatten de kernel of de kerncode van het besturingssysteem)
* CONFIG.SYS (Deze bevatten verschillende configuratie-opties)
* KEYBOARD.SYS (deze bevatten informatie over de toetsenbordindeling)
* COUNTRY.SYS (deze bevatten informatie over land en codepagina's)

## SYS-bestandsindeling ##

Microsoft ontwikkelde de bestanden met de extensie .sys. Variabelen en functies zijn opgenomen in SYS-bestanden. Deze worden meestal gebruikt door het Microsoft-besturingssysteem. Deze bestanden bevinden zich voornamelijk in de hoofdmap van de schijf:

* C:\Windows\system32\drivers
* C:\Windows\WinSxS

Enkele veel voorkomende waarschuwingen over SYS-bestanden zijn als volgt:

* De namen van deze bestanden mogen niet worden gewijzigd, aangezien deze bestanden verantwoordelijk zijn voor de kernfuncties en variabelen van het besturingssysteem
* Deze bestanden mogen niet worden verwijderd omdat het ontbreken van deze bestanden fouten kan veroorzaken
* De .sys-bestanden mogen pas van internet worden gedownload als u zeker bent van de legitimiteit van de bron
* Men moet niet met deze bestanden knoeien, aangezien het veranderen of rommelen hiervan ernstige systeemfouten kan veroorzaken
* Als deze bestanden beschadigd raken door een virus of malware, moeten deze opnieuw worden geïnstalleerd

## SYS Voorbeeld ##

Het volgende is een voorbeeld van een eenvoudig SYS-systeemconfiguratiebestand:

```
DEVICE=C:\Windows\HIMEM.SYS
DOS=HIGH,UMB
DEVICE=C:\Windows\EMM386.EXE NOEMS
FILES=30
STACKS=0,0
BUFFERS=20
DEVICEHIGH=C:\Windows\COMMAND\ANSI.SYS
DEVICEHIGH=C:\MTMCDAI.SYS /D:123
```
