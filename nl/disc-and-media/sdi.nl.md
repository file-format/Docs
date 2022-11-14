{
  "date" : "2021-08-13",
  "keywords" :[ "sdi-bestand", "sdi-bestandsformaat", "wat is een sdi-bestand", "bestand", "sdi-voorbeeld", "sdi-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Meer informatie over SDI-bestandsindeling en API's die SDI-bestanden kunnen maken en openen.",
  "title" :"SDI - Windows-systeemimplementatie-imagebestand",
  "linktitle" : "SDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-13"
}

## Wat is een SDI-bestand?
Het bestand met de extensie .sdi bevat een laad-blob, boot-blob en een deel-blob; vaak gebruikt door Windows Embedded Studio om RAM-schijven of opstartschijven te maken voor het laden en installeren van Windows. De SDI wordt afgekort voor System Deployment Image. De Windows Embedded Studio is een programma dat wordt gebruikt voor het maken van schijfkopieën voor Windows. Dit programma bevat eigenlijk het SDI-bestandsbeheerprogramma en een opdrachtregelprogramma genaamd **sdimgr.exe**, beide kunnen worden gebruikt om SDI-afbeeldingen te implementeren, te maken en te bewerken.

## SDI-bestandsindeling
Het SDI-bestandsformaat wordt veel gebruikt om het gebruik van een virtuele schijf voor het opstarten van een systeem mogelijk te maken. Sommige versies van Microsoft Windows maken **RAM-opstarten** mogelijk, wat belangrijk is om een SDI-bestand in het geheugen te laden en er vervolgens van op te starten. Het SDI-bestandsformaat stelt zichzelf ook in staat om via het netwerk op te starten met behulp van de PXE (Preboot Execution Environment). Het wordt ook gebruikt voor beeldvorming op de harde schijf.
### SDI-bestandssecties
Het SDI-bestand zelf kan worden onderverdeeld in de volgende secties:
- **Boot BLOB**: dit bevat het eigenlijke opstartprogramma, STARTROM.COM. Dit is analoog aan de opstartsector van een harde schijf.
- **BLOB laden**: dit bevat meestal NTLDR en wordt gestart door de opstart-BLOB.
- **Deel BLOB**: dit bevat de daadwerkelijke opstarttijd; bevat ook de bestanden boot.ini en ntdetect.com die zich in de hoofdmap van de runtime zouden moeten bevinden.
- **Schijf-BLOB**: dit is een platte HDD-afbeelding die begint met een MBR. Het wordt gebruikt voor beeldvorming op de harde schijf in plaats van op te starten. Ook kunnen alleen schijf-BLOB's worden aangekoppeld met de hulpprogramma's van Microsoft.


## Referenties

* [Systeemimplementatieafbeelding - door Wikipedia](https://en.wikipedia.org/wiki/System_Deployment_Image)


