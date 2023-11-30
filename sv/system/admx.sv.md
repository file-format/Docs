{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADMX-fil - filformat för administrativ mall för gruppolicy",
  "description":"Lär dig om ADMX-filformat och hur du öppnar ADMX-filer.",
  "linktitle" : "ADMX",
  "menu" : {
    "docs" : {
      "identifier" : "system-admx",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Vad är ADMX fil?

En ADMX-fil är en policykonfigurationsfil som används av Microsoft Windows Group Policy-programvara som hanterar grupp av datorer i en grupp. Det är en XML-baserad administrativ mallfil och introducerades med Windows Vista Service Pack 1. ADMX-filer innehåller konfigurationsinställningar för användarkonton, operativsystemkonfigurationer och applikationer. ADMX-filer används för att lagra och distribuera konfigurationer för centraliserad hantering av många datorsystem.

Du kan skapa eller redigera ADMX-filer med valfri XML-kompatibel, valfri textredigerare eller Microsoft Group Policy Object Editor.

## ADMX-filformat - Mer information

ADMX-filer lagras i det universella [XML](/sv/web/xml/) filformatet som är läsbart för människor. Det är flerspråkigt filformat och låter systemadministratörer från olika språk arbeta med samma ADMX-filer. ADMX-filer ersatte det gamla [ADM](/sv/system/adm/) filformatet som är ett unicode-formaterat textfilformat. ADMX-filer anger de registernycklar som ändras när en viss grupprincipinställning ändras.

### Vad kan jag göra med ADMX-filen?

ADMX-filer definierar vilka åtgärder som ska tillåtas för användardatorer som ingår i en grupp. Grupppolicyn påtvingar reglerna i kombination med Active Directory-programvaran. ADMX-filer hanteras från det centrala arkivet på Windows OS som är en central plats i domänen.

En ADMX-fil som distribueras i en arbetsmiljö kan låta administratörer implementera policyer som:

* Kontrollera användningen av internet
* Nedladdning av vissa typer av filer
* Användning av flyttbara enheter på systemen

## Referenser

* [Administrativa mallfiler - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - Hantera administrativa mallfiler](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

