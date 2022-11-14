{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LOCK File Format - Wat is een Lock-bestand?",
  "description":"Meer informatie over het LOCK-bestandsformaat en zijn .",
  "linktitle" : "LOCK",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## Wat is een LOCK-bestand?

Een **LOCK**-bestand is een hernoemd bestand dat door toepassingen en besturingssystemen wordt gebruikt om een bestand of een apparaat als vergrendeld te markeren. Dit vertelt andere applicaties om het bestand niet te gebruiken, tenzij het vrij is van de applicatie die het gebruikt. In de meeste gevallen zijn deze vergrendelingsbestanden leeg, maar in andere gevallen kunnen ze informatie bevatten met betrekking tot de vergrendeling, zoals eigenschappen en instellingen.

Soms wordt het .lock-bestand gebruikt door Microsoft's .NET Framework om **lockeed**-kopieën van een databasebestand te maken. In een dergelijk geval wordt een kopie van het databasebestand geopend met de extensie .lock. Hierdoor kan de gebruiker geen wijzigingen aanbrengen in het bestand terwijl het door een andere gebruiker wordt gebruikt.

## LOCK-bestandsindeling - Meer informatie

Elke toepassing maakt een LOCK-bestand aan en het bestandsformaat is specifiek voor de toepassing. Deze lock-bestanden kunnen zowel in tekst als in binair bestandsformaat worden opgeslagen.

De aanwezigheid van vergrendelingsbestanden verhindert gelijktijdige toegang van een bron tot meerdere bestanden die toegang proberen te krijgen tot die bron. Er wordt een kopie van het originele bestand gemaakt met de extensie .lock achter de naam. Dit vertelt andere toepassingen om alleen-lezen toegang tot het bestand te hebben. Resource.dat wordt bijvoorbeeld resource.data.lock.

Voor de programmeertaal Ruby kun je het bestand **gemfile.lock** tegenkomen. Dit is waar Bundler de exacte versies bijhoudt die zijn geïnstalleerd. Dus wanneer een project/bibliotheek naar een andere machine wordt verplaatst, zal de actieve bundel naar de Gemfile kijken voor de exacte relevante versie.

## Bestand vergrendelen in Linux

Linux ondersteunt twee soorten bestandsvergrendelingen: adviserende vergrendelingen en verplichte vergrendelingen.

* **Adviesvergrendelingen**: Type vergrendeling dat niet wordt afgedwongen. In dit geval werken deelnemende processen met elkaar samen om expliciet sloten te verwerven. Als dit niet mogelijk is, worden adviesvergrendelingen genegeerd.

* **Verplichte vergrendelingen**: in het geval van verplichte vergrendeling dwingt het besturingssysteem de bestandsvergrendeling af door te voorkomen dat andere processen het bestand lezen of schrijven. Hiervoor is geen samenwerking tussen de processen nodig.

verplichte vergrendeling vereist geen samenwerking tussen de deelnemende processen. Zodra een verplichte vergrendeling van een bestand is geactiveerd, voorkomt het besturingssysteem dat andere processen het bestand kunnen lezen of schrijven.

## Referenties

* [GemFile en Gemfile.lock in Ruby](https://medium.com/never-hop-on-the-bandwagon/gemfile-and-gemfile-lock-in-ruby-65adc918b856)
* [Linux vergrendelen](https://www.baeldung.com/linux/file-locking#:~:text=File%20locking%20is%20a%20mechanism,very%20dangerous%20command%20in%20Linux.)

