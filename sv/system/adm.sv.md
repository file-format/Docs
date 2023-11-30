{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADM-fil - filformat för administrativa mallar",
  "description":"Läs mer om ADM-filformat och hur du öppnar ADM-filer.",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Vad är en ADM-fil?

En ADM-fil är en mallfil som används av programvaran Microsoft Group Policies för att ange platsen för registerbaserade policyinställningar i registerfilen. Den används av systemadministratörer för att definiera policyn för hantering av en grupp datorer som ingår i gruppen. Denna information blir en del av de grupprincipobjekt (GPO) som skapas för hantering av gruppen.

Du kan öppna ADM-filer med Microsoft Group Policy Object Editor.

## ADM-filformat - Mer information

ADM-filer lagras som unicode-formaterade textfiler. Dessa användes främst för att beskriva platsen för registerbaserade policyinställningar i Windows Vista och Windows 7-registret.

ADM-filer stöds inte längre och har ersatts av filerna [ADMX](/sv/system/admx/). GPA ignorerar följande ADM-standardfiler på datorer som kör Microsoft Windows Vista Service Pack 1 eller senare.

* system.adm
* inetres.adm
* konf.adm
* wmplayer.adm
* wuau.adm

## Referenser

* [Administrativa mallfiler - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - Hantera administrativa mallfiler](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

