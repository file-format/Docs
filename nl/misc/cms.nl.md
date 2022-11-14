{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CMS-bestandsindeling - verbindingsbeheerserviceprofielbestand",
  "description":"Meer informatie over CMS-bestanden en API's die CMS-bestanden kunnen maken en openen.",
  "linktitle" : "CMS",
  "menu" : {
    "docs" : {
      "identifier": "misc-cms",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Wat is een CMS-bestand?

Een CMS-bestand is een gegevensbestand dat profielinformatie bevat die wordt gebruikt door Microsoft Windows Connection Manager. Hiermee kunnen externe gebruikers verbinding maken met een netwerk met behulp van deze profielinformatie. Informatie die is opgeslagen in een CMS-bestand bevat gegevens over het besturingssysteem van de gebruiker en machtigingen die worden gebruikt om een verbinding tot stand te brengen tussen een externe gebruiker en het netwerk. CMS-beheerders gebruiken de Connection Manager Administrator Kit (CMAK) om CMS-bestanden te genereren.

## CMS-bestandsindeling - Meer informatie

CMS-bestanden worden niet vaak gevonden op gebruikersmachines. Aangezien deze specifiek worden gebruikt om externe gebruikers toegang te geven tot een netwerk, vindt u deze op computers die worden gebruikt om verbinding te maken met een bedrijfsnetwerk of een specifiek speciaal gebouwd kantoor. In de meeste gevallen wordt het gebruikt om verbinding te maken met een organisatorisch netwerk zoals Virtual Private Network (VPN) dat alleen aan een bedrijf is toegewezen. Als netwerkbeheerder stelt u met Verbindingsbeheer de toegang tot zo'n netwerk in, zodat hij vanaf een externe locatie toegang heeft tot het bedrijfsnetwerk.

### Wat is indie CMS?

Een CMS-profielbestand wordt gemaakt met Verbindingsbeheer en wordt samen met andere configuratiebestanden geleverd voordat het aan de externe gebruiker wordt verstrekt. Deze extra bestanden kunnen een CMP- en een INF-bestand bevatten die samen met een [EXE](/nl/executable/exe/)-bestand zijn verpakt. Dit complete pakket wordt aan de externe gebruiker geleverd om verbinding te maken met het netwerk.

## Referenties

* [Windows-verbindingsbeheer begrijpen en configureren](https://docs.microsoft.com/en-us/windows-hardware/drivers/mobilebroadband/understanding-and-configure-windows-connection-manager)

