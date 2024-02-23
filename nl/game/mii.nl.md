{
  "date" : "2023-01-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Leer meer over de Age of Empires 2 Expansion Replay MGX-bestandsindeling en API's waarmee MGX-bestanden kunnen worden gemaakt en geopend.",
  "title" : "MII-bestand - Wii-bestandsindeling voor virtuele avatar",
  "linktitle" : "MII",
  "menu" : {
    "docs" : {
      "identifier":"game-mii-nl",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-15"
}

## Wat is een MII-bestand?

Een MII-bestand is een virtueel avatarbestandsformaat dat wordt gebruikt om virtuele avatars op de Nintendo Wii-spelcomputer op te slaan. Deze bestanden bevatten informatie zoals het uiterlijk, de bewegingen en animaties van de avatar. Ze kunnen worden gebruikt in games, sociale netwerktoepassingen en andere software op de Wii. Een MII-bestand bevat ook andere kenmerken van de avatar, zoals het geslacht, de haarkleur, de huidskleur, gelaatstrekken en het oogtype.

U kunt een MII-bestand openen met behulp van de [My Avatar Editor](https://rc24.xyz/goodies/mii/).

## MII-bestandsformaat

Het MII-bestandsformaat wordt gedetailleerd gedefinieerd op [Wii Brew](https://wiibrew.org/wiki/Mii_data). Tekenreeksen in een MII-bestand worden opgeslagen in Unicode-formaat (UTF-16), big-endian.

### MI-blok

MII-bestandsgegevens worden in twee blokken op de Wiimote opgeslagen. Elk blok is 750 bytes lang, met 2 bytes CRC, wat het totaal op 752 bytes brengt. Elk blok begint met een waarde van 4 bytes ('RNCD') die het magische getal lijkt te zijn voor het MII-bestandsformaat.

## Hoe MII-bestanden maken?

Er zijn een paar verschillende manieren om avatars voor de Nintendo Wii te maken:

1. `Het ingebouwde Mii-kanaal op de Wii gebruiken:` Met dit kanaal kun je aangepaste avatars maken met behulp van een verscheidenheid aan hulpmiddelen, waaronder gezichtskenmerken, lichaamsvorm en kleding. Nadat je je avatar hebt gemaakt, kun je deze opslaan als een Mii-bestand en gebruiken in games en andere software op de Wii.

1. `De Mii Maker-app gebruiken op de Nintendo 3DS:` Met de Mii Maker-app kun je aangepaste avatars maken met behulp van het aanraakscherm en de camera op je Nintendo 3DS. Nadat je je avatar hebt gemaakt, kun je deze opslaan als Mii-bestand en via een draadloze verbinding naar je Wii overbrengen.

1. `Software van derden gebruiken:` Sommige ontwikkelaars hebben software gemaakt waarmee je aangepaste avatars voor de Wii kunt maken. Deze software is doorgaans ontworpen voor gebruik op een computer en vereist mogelijk extra stappen om de avatar naar je Wii over te zetten.

1. `Vooraf gemaakte avatars gebruiken:` Sommige games en andere software op de Wii worden geleverd met vooraf gemaakte avatars die je kunt gebruiken.

In alle gevallen heb je een Nintendo-account nodig om je avatar op de Wii te kunnen maken en opslaan.

## Referenties

* [Mijn Avatar-editor](https://rc24.xyz/goodies/mii/)

* [Wii Brew](https://wiibrew.org/wiki/Mii_data)


