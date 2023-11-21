{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADM Bestand - Beheersjabloon Bestandsformaat",
  "description":"Leer meer over het ADM-bestandsformaat en hoe u ADM-bestanden opent.",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Wat is een ADM-bestand?

Een ADM-bestand is een sjabloonbestand dat door Microsoft Group Policies-software wordt gebruikt om de locatie van registergebaseerde beleidsinstellingen in het registerbestand op te geven. Het wordt door systeembeheerders gebruikt om het beleid te definiëren voor het beheer van een groep computers die deel uitmaken van de groep. Deze informatie wordt onderdeel van de groepsbeleidsobjecten (GPO's) die zijn gemaakt voor het beheer van de groep.

U kunt ADM-bestanden openen met de Microsoft Group Policy Object Editor.

## ADM-bestandsindeling - Meer informatie

ADM-bestanden worden opgeslagen als Unicode-geformatteerde tekstbestanden. Deze werden voornamelijk gebruikt om de locatie van registergebaseerde beleidsinstellingen in het Windows Vista- en Windows 7-register te bepalen.

ADM-bestanden worden niet meer ondersteund en zijn vervangen door de [ADMX](/nl/system/admx/) bestanden. GPA negeert de volgende standaard ADM-bestanden op computers met Microsoft Windows Vista Service Pack 1 of hoger.

* systeem.adm
* inetres.adm
* conf.adm
* wmplayer.adm
* wuau.adm

## Referenties

* [Beheersjabloonbestanden - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - Beheersjabloonbestanden beheren](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

