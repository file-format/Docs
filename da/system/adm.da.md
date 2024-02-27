{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ADM-fil - Administrativt skabelonfilformat",
  "description":"Lær om ADM-filformat og hvordan du åbner ADM-filer.",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm-da",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Hvad er en ADM fil?

En ADM-fil er en skabelonfil, der bruges af Microsoft Group Policies-software til at angive placeringen af registreringsdatabasen-baserede politikindstillinger i registreringsdatabasen. Det bruges af systemadministratorer til at definere politikken for styring af en gruppe af computere, der er en del af gruppen. Disse oplysninger bliver en del af de gruppepolitikobjekter (GPO'er), der oprettes til administration af gruppen.

Du kan åbne ADM-filer ved hjælp af Microsoft Group Policy Object Editor.

## ADM-filformat - flere oplysninger

ADM-filer gemmes som unicode-formaterede tekstfiler. Disse blev primært brugt til at beskrive placeringen af registreringsdatabasen-baserede politikindstillinger i Windows Vista og Windows 7 registreringsdatabasen.

ADM-filer understøttes ikke længere og er blevet erstattet af [ADMX](/system/admx/)-filerne. GPA ignorerer følgende standard ADM-filer på computere, der kører Microsoft Windows Vista Service Pack 1 eller nyere.

 * system.adm
 * inetres.adm
 * conf.adm
 * wmplayer.adm
 * wuau.adm

## Referencer

* [Administrative skabelonfiler - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)

* [NetIQ - Håndtering af administrative skabelonfiler](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)

* [SSDT](https://wiki.osdev.org/SSDT)


