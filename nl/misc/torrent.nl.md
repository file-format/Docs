{
  "date" : "2022-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Torrent-bestandsindeling - BitTorrent-bestand",
  "description":"Meer informatie over TORRENT-bestanden en API's die TORRENT-bestanden kunnen maken en openen.",
  "linktitle" : "TORRENT",
  "menu" : {
    "docs" : {
      "identifier":"misc-torrent",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Wat is een TORRENT-bestand?

Een TORRENT-bestand is een tekstbestand dat door BitTorrent en andere P2P-programma's (peer-to-peer) wordt gebruikt voor het downloaden en uitwisselen van inhoud. De downloadbare inhoud kan documenten, video's, games, films en andere media bevatten die op internet beschikbaar zijn. Het bevat metadata-informatie over de inhoud en locatie van de te downloaden media. Software zoals BitTorrent gebruikt informatie uit dit bestand, zoals naam, bestandsgrootte en mapstructuur voor het downloaden van gegevens. Torrent-bestanden kunnen online worden geconverteerd naar andere bestandsindelingen zoals [PDF](/nl/pdf/).

## Wat is torrenting? Het TORRENT-bestandsformaat voor gegevensuitwisseling

Torrenting is het concept van het uitwisselen (downloaden en uploaden) van gegevensbestanden met behulp van het BitTorrent-netwerk. In tegenstelling tot conventionele servers waar gegevens worden geüpload zodat anderen ze kunnen openen en downloaden, worden torrent-bestanden opgehaald en verzonden via het torrent-netwerk. Wanneer een gebruiker een .torrent-bestand opent in toepassingen zoals BitTorrent, begint de software de inhoud van het bestand bitsgewijs te downloaden. Als meerdere gebruikers hetzelfde bestand hebben, verdeelt BitTorrent de downloads over alle gebruikers om het downloadproces te versnellen. Tegelijkertijd wordt de computer van de gebruiker die het bestand downloadt ook de bron van het bestand om het naar andere gebruikers te sturen die hetzelfde bestand downloaden.

### Structuur van een TORRENT-bestand

Een torrent-bestand is een combinatie van een lijst met bestanden en metadata-informatie over alle delen van het bestand die moeten worden gedownload. Het bevat de volgende informatie in de vorm van sleutels.

- `aankondigen` — De URL van de tracker die wordt aangekondigd aan andere peers om te informeren over de beschikbaarheid van het bestand
- `info` — Dit verwijst naar een woordenboek waarvan de sleutels afhankelijk zijn van het feit of een of meer bestanden worden gedeeld:
  - files—a list of dictionaries each corresponding to a file (only when multiple files are being shared). Each dictionary has the following keys:
- `lengte` — grootte van het bestand in bytes.
- `pad` — een lijst met strings die overeenkomen met namen van subdirectory's, waarvan de laatste de daadwerkelijke bestandsnaam is
- `length` — de grootte van het bestand in bytes (alleen wanneer één bestand wordt gedeeld)
- `naam` — bestandsnaam waar het bestand moet worden opgeslagen
- `stuklengte` — aantal bytes per stuk. Dit is gewoonlijk 28 KiB = 256 KiB = 262.144 B.
- `pieces` — een hashlijst die een aaneenschakeling is van de SHA-1-hash van elk stuk.

## Is torrenting veilig en legaal?

Het Torrenting-protocol voor de uitwisseling van gegevens tussen P2P-gebruikers is veilig, omdat het gewoon de manier is om elk type bestand te delen. Het protocol zelf is dus niet onveilig of illegaal. De inhoud die via het netwerk wordt gedeeld, kan echter bestanden of media bevatten die de juridische status van de gedeelde documenten kunnen schenden. In een dergelijk geval kan de uitwisseling van dergelijke gegevens leiden tot juridische stappen tegen de partijen die betrokken zijn bij het openbaar delen van dergelijke bestanden.

## Referenties

* [TORRENT-bestand - wikipedia](https://en.wikipedia.org/wiki/Torrent_file)

