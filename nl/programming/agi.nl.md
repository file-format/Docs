{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AGI-bestand - Asterisk Gateway Interface-bestandsindeling",
  "description":"Meer informatie over wat AGI-bestandsindeling is met voorbeelden en API's die AGI-bestanden kunnen maken en openen.",
  "linktitle" : "AGI",
  "menu" : {
    "docs" : {
      "identifier": "programming-agi",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Wat is een AGI-bestand?

Een AGI-bestand is een scriptbestand dat wordt gebruikt door het open source-telefoniesysteem Asterisk. Het bevat informatie die kan worden gebruikt om processen en Asterisk dialplan te automatiseren. Met behulp van AGI-scriptbestanden kunnen verbindingen tot stand worden gebracht met relationele databases zoals PostgreSQL of MySQL. Bovendien kunnen AGI-scripts ook worden gebruikt om toegang te krijgen tot andere externe bronnen. AGI-scripts kunnen de controle over het dialplan overdragen aan een extern AGI-script, waardoor Asterisk complexe taken kan uitvoeren.

## AGI-bestandsindeling - Meer informatie

AGI-scriptbestanden worden opgeslagen als tekstbestanden en kunnen in elke teksteditor worden geopend om wijzigingen aan te brengen.

### Standaardpatroon van AGI-communicatie

Het AGI-script laadt de variabelen en hun waarden die door Asterisk zijn verzonden. Een algemeen beeld van deze variabelen is als volgt.

```
agi_request: test.py
agi_channel: Zap/1-1
agi_language: en
agi_callerid:
agi_context: default
agi_extension: 123
agi_priority: 2
```

Deze variabelen worden gevolgd door een lege regel die door Asterisk is verzonden, waaruit blijkt dat het AGI-script nu de controle over het dialplan kan overnemen.

### Programmeertaal voor AGI-scriptbestanden

AGI-scripts kunnen doorgaans worden geschreven in Perl, [PHP](/nl/programming/php/), [C](/nl/programming/c/), Pascal of Bourne Shell.

## Referenties

* [Asterisk AGI-script](https://www.oreilly.com/library/view/asterisk-the-future/9780596510480/ch09.html)

