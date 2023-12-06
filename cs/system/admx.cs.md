{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Soubor ADMX - Formát souboru šablony pro správu zásad skupiny",
  "description":"Další informace o formátu souboru ADMX a o tom, jak otevřít soubory ADMX.",
  "linktitle" : "ADMX",
  "menu" : {
    "docs" : {
      "identifier" : "system-admx",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Co je soubor ADMX?

Soubor ADMX je konfigurační soubor zásad používaný softwarem zásad skupiny Microsoft Windows, který spravuje skupinu počítačů ve skupině. Jedná se o soubor šablony pro správu založený na XML a byl zaveden s aktualizací Windows Vista Service Pack 1. Soubory ADMX obsahují nastavení konfigurace pro uživatelské účty, konfigurace operačního systému a aplikace. Soubory ADMX se používají k ukládání a nasazení konfigurací pro centralizovanou správu mnoha počítačových systémů.

Soubory ADMX můžete vytvářet nebo upravovat pomocí libovolného textového editoru kompatibilního s XML nebo editoru objektů Microsoft Group Policy.

## Formát souboru ADMX – Další informace

Soubory ADMX jsou uloženy v univerzálním formátu souborů [XML](/cs/web/xml/), který je čitelný pro člověka. Jedná se o vícejazyčný formát souborů a umožňuje správcům systému z různých jazyků pracovat se stejnými soubory ADMX. Soubory ADMX nahradily starý formát souboru [ADM](/cs/system/adm/), což je formát textového souboru ve formátu Unicode. Soubory ADMX určují klíče registru, které se změní, když se změní určité nastavení zásad skupiny.

### Co mohu dělat se souborem ADMX?

Soubory ADMX definují, jaké akce mají být povoleny uživatelským počítačům, které jsou součástí skupiny. Zásady skupiny ukládají pravidla nastavená v kombinaci se softwarem Active Directory. Soubory ADMX jsou spravovány z centrálního úložiště v operačním systému Windows, což je centrální umístění v doméně.

Soubor ADMX nasazený v pracovním prostředí může správcům umožnit implementovat zásady, jako jsou:

* Kontrolujte používání internetu
* Stahování určitých typů souborů
* Použití vyměnitelných zařízení v systémech

## Reference

* [Soubory šablon pro správu – ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ – Správa souborů šablon pro správu](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

