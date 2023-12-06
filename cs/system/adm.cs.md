{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Soubor ADM - Formát souboru šablony pro správu",
  "description":"Další informace o formátu souboru ADM a jak otevřít soubory ADM.",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Co je soubor ADM?

Soubor ADM je soubor šablony používaný softwarem Microsoft Group Policy k určení umístění nastavení zásad založených na registru v souboru registru. Používají jej správci systému k definování zásad pro správu skupiny počítačů, které jsou součástí skupiny. Tyto informace se stanou součástí objektů zásad skupiny (GPO), které jsou vytvářeny pro správu skupiny.

Soubory ADM můžete otevřít pomocí Microsoft Group Policy Object Editor.

## Formát souboru ADM – Další informace

Soubory ADM jsou uloženy jako textové soubory ve formátu Unicode. Ty byly primárně použity k popisu umístění nastavení zásad založených na registru v registru Windows Vista a Windows 7.

Soubory ADM již nejsou podporovány a byly nahrazeny soubory [ADMX](/cs/system/admx/). GPA ignoruje následující výchozí soubory ADM v počítačích se systémem Microsoft Windows Vista Service Pack 1 nebo novějším.

* system.adm
* inetres.adm
* conf.adm
* wmplayer.adm
* wuau.adm

## Reference

* [Soubory šablon pro správu – ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ – Správa souborů šablon pro správu](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

