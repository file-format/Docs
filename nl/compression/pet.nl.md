{
  "date" : "2022-06-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PET-bestandsindeling - Puppy Linux-installatiepakketbestand",
  "description":"Meer informatie over PET-bestandsindelingen en API's die PET-bestanden kunnen maken en openen.",
  "linktitle" : "PET",
  "menu" : {
    "docs" : {
      "identifier":"compression-pet",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-23"
}

## Wat is een Linux PET-bestand?

Een PET-bestand is een applicatie-installatiepakketbestand dat is gemaakt en gebruikt met de PuppyLinux-variant van het Linux-besturingssysteem. Het is gemaakt als een gecomprimeerd [TGZ](/nl/compression/tgz/)-bestand dat de bestandsgrootte van het gecomprimeerde archief verkleint. De integriteit van het PET-bestandsformaat wordt gewaarborgd door de md5sum-controlesom die aan het einde van het bestand wordt toegevoegd voor verificatie aan de externe kant. PET-bestanden kunnen worden uitgepakt met behulp van de standaard TGZ-bestandsextractor en WinRAR. PET-bestanden vervingen de oude [PUP](/nl/compression/pup/) pakketinstallatiebestanden.

## PET-bestandsindeling

PET-bestanden worden op schijf opgeslagen als gecomprimeerde archieven in binaire bestandsindeling. De details van het interne bestandsformaat van het PET-bestandsformaat zijn echter niet bekend. Net als bij [.exe](/nl/executable/exe/) en [.msi](/nl/executable/msi/) pakketinstallatiebestanden, starten de PET-bestanden een installatie wanneer ze worden uitgevoerd.

## Referenties

* [PuppyLinux](https://en.wikipedia.org/wiki/Puppy_Linux)
* [Index van PuppyLinux PET-pakketten](https://distro.ibiblio.org/puppylinux/pet-packages-lucid/)

