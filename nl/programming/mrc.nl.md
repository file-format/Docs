{
  "date" : "2021-09-14", 
  "keywords" :[ "mrc", "bestand", "extensie", "bestandsindeling", "mrc-implementatie", "Programmeergids", "mrc-voorbeeld", "mIRC", "mIRC-scripttaal", "bestanden van INI", " mSL-scripttaal", "mIRC-taal", "mIRC-scripts", "scripttaal"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MRC - mIRC-scripttaalbestand",
  "description":"Meer informatie over MRC-bestandsindeling en API's die MRC-bestanden kunnen maken en openen.",
  "linktitle" : "MRC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-14"
}

## Wat is een MRC-bestand?

mIRC is een scripttaal die is ingebed als een IRC-client (Internet Relay Chat) in het Windows-besturingssysteem. Het biedt een faciliteit van bescherming tegen spam voor persoonlijk en kanaalgebruik. Om een betere ervaring van gebruikerscompatibiliteit te bieden, maakt deze mIRC-scripttaal het creëren van dialoogvensters mogelijk. De bestanden die scripts bevatten, meestal in platte tekstindeling, worden opgeslagen met de extensie MRC of als de bestanden van [INI](/nl/system/ini/). Functies van deze taal staan bekend als commando's en identifiers (wanneer ze waarde retourneren).

mIRC-taal biedt het laden van meerdere scriptbestanden tegelijk. Aan de andere kant kan het ene bestand ertoe leiden dat het andere niet meer wordt gebruikt wanneer het tegelijkertijd wordt geladen. Commando's worden opgeslagen en kunnen automatisch in IRC voorkomen. De commando's en aliassen die in deze taal worden gebruikt, hebben geen voorrang op een van de tekens.

mIRC wordt veel gebruikt om bots automatisch een kanaal te laten beheren, maar het kan ook worden aangepast door de mSL-scripttaal. Het kan veel nieuwe functies introduceren, zoals macro's, het vermogen om muziek af te spelen, kleine macro's en functies, basisspellen of het bedienen van kleine applicaties.


## Korte geschiedenis ##

Deze scripttaal werd voor het eerst ontwikkeld in 1995 door Khaled Adam Bey. Het ontwerp van de scripttaal is ook gemaakt door Khalid. Het doel van deze taal was gebeurtenisgestuurd programmeren. Aanvankelijk was de bestandsextensie die werd gebruikt voor de bestanden van deze programmeertaal .mrc en .ini. Bovendien is het ontwikkeld onder licentie van propriëtaire software.

## Technische specificatie ##

Sommige functies zijn op maat gemaakt via deze mIRC-taal en staan bekend als aliassen. Wanneer deze aliassen waarden retourneren, staan ze bekend als aangepaste ID's. Alle variabelen in deze mIRC-taal worden dynamisch getypt. Sigils worden gebruikt door de mIRC-scripts. Een ander kenmerk van deze scripttaal zijn pop-ups. De gebruikers kunnen pop-ups oproepen door ze simpelweg te selecteren. Afstandsbedieningen zijn gespecificeerd voor bepaalde gebeurtenissen. De afstandsbedieningen worden aangeroepen wanneer de relatieve gebeurtenis plaatsvindt.

Door spaties gescheiden tokens worden gebruikt om elke regel code van deze taal te breken. Er zijn enkele andere populaire extensies die worden gebruikt voor mIRC-bestanden, zoals MDX (mIRC Dialog Extension) en DCX (Dialog Control Extension). Beide zijn dialoogextensies en zijn relatief populairder. De taalconstructies worden aangeduid met de nomenclatuur van deze scripttaal. De mIRC-taal omvat verschillende aspecten van een scripttaal, zoals lokale en globale variabelen, binaire variabelen, hashtabellen en bestandsverwerking.


## Voorbeeld MRC-bestandsindeling ##

```

;Defines the alias 'hello' in the remote script

;Note: if this is placed in an alias script,
;the 'alias' part must be removed (result: hello {)
;Usage: /hello

alias hello {

  ;Displays(/nl/echo) 'Hello World!' into the active window(-a)
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

## Referentie ##

* [MIRC - door Wikipedia](https://en.wikipedia.org/wiki/MIRC_scripting_language)



