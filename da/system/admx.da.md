{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ADMX-fil - filformat til administrativt gruppepolitikskabelon",
  "description":"Lær om ADMX filformat og hvordan du åbner ADMX filer.",
  "linktitle" : "ADMX",
  "menu" : {
    "docs" : {
      "identifier" : "system-admx-da",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Hvad er en ADMX fil?

An ADMX file is a policy configuration file used by Microsoft Windows Group Policy software that manages group of computers in a group. It is an XML-based administrative template file and was introduced with Windows Vista Service Pack 1. ADMX-filer indeholder konfigurationsindstillinger for brugerkonti, operativsystemkonfigurationer og applikationer. ADMX-filer bruges til at gemme og implementere konfigurationerne til centraliseret styring af mange computersystemer.

Du kan oprette eller redigere ADMX-filer ved hjælp af enhver XML-kompatibel, enhver teksteditor eller Microsoft Group Policy Object Editor.

## ADMX-filformat - flere oplysninger

ADMX-filer er gemt i det universelle [XML](/web/xml/)-filformat, der kan læses af mennesker. Det er flersproget filformat og giver systemadministratorer fra forskellige sprog mulighed for at arbejde med de samme ADMX-filer. ADMX-filer erstattede det gamle [ADM](/system/adm/)-filformat, som er et unicode-formateret tekstfilformat. ADMX-filer angiver de registreringsnøgler, der ændres, når en bestemt gruppepolitik-indstilling ændres.

### Hvad kan jeg gøre med ADMX-filen?

ADMX-filer definerer, hvilke handlinger der skal tillades til brugercomputere, der er en del af en gruppe. Gruppepolitikken pålægger reglerne i kombination med Active Directory-software. ADMX-filer administreres fra det centrale lager på Windows OS, som er en central placering i domænet.

En ADMX-fil installeret i et arbejdsmiljø kan lade administratorer implementere politikker som:

 * Styr brugen af internettet
 * Download af visse typer filer
 * Brug af flytbare enheder på systemerne

## Referencer

* [Administrative skabelonfiler - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)

* [NetIQ - Håndtering af administrative skabelonfiler](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)

* [SSDT](https://wiki.osdev.org/SSDT)


