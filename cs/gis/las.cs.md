{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAS - Lidar LASer File Format",
  "description":"Další informace o formátu souboru LAS a rozhraních API, která mohou vytvářet a otevírat soubory LAS.",
  "linktitle" : "LAS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## Co je soubor LAS?

Formát souboru LAS (Lidar LASer) je binární formát souboru speciálně navržený pro ukládání dat mračna bodů lidar. Byl vyvinut a je udržován Americkou společností pro fotogrammetrii a dálkový průzkum (ASPRS) jako standardizovaný formát pro výměnu dat lidar a interoperabilitu.

Soubory LAS ukládají podrobné informace o jednotlivých lidarových bodech, včetně jejich 3D souřadnic (x, y a z), hodnot intenzity, klasifikačních kódů a dalších atributů. Formát podporuje jak diskrétní návrat, tak lidarová data s plným průběhem, což umožňuje uložení více návratů na laserový pulz.

## Formát souboru LAS

Struktura souboru LAS se skládá ze tří hlavních částí: hlavičky souboru, záznamů s proměnnou délkou (VLR) a záznamů bodových dat.

1. Záhlaví souboru: Záhlaví souboru obsahuje základní informace o souboru LAS, jako je verze formátu dat, formát dat bodů, počet bodů, souřadnice ohraničujícího rámečku, souřadnicový referenční systém (CRS) a další metadata. Poskytuje souhrn lidarových dat obsažených v souboru.

2. Záznamy s proměnnou délkou (VLR): VLR jsou volitelné a mohou ukládat další metadata a vlastní informace o lidarových datech. VLR umožňují flexibilitu při rozšiřování formátu tak, aby vyhovoval specifickým požadavkům uživatelů. Příklady VLR zahrnují informace o senzorovém systému, parametrech zpracování dat nebo klasifikační schémata.

3. Bodové datové záznamy: Bodové datové záznamy ukládají aktuální lidarová měření. Každý datový záznam bodu představuje jeden lidarový bod a obsahuje atributy, jako jsou souřadnice x, yaz, hodnoty intenzity, klasifikační kódy (např. půda, vegetace, budovy) a další uživatelem definované atributy. Záznamy bodů mohou také ukládat časové značky, počty návratů a úhly skenování.

Soubory LAS podporují různé datové formáty (0 až 10), aby vyhovovaly různým typům lidarových dat a úrovni potřebných informací. Například formát 0 představuje jednoduchý bodový formát se základními informacemi, zatímco formáty 1 až 3 poskytují komplexnější data včetně informací o tvaru vlny pro každý návrat.

Soubory LAS jsou široce podporovány softwarem lidar a nástroji pro zpracování, což z nich činí standardní formát pro výměnu a analýzu dat lidaru. Kromě toho lze soubory LAS komprimovat pomocí technik bezztrátové komprese, aby se zmenšila velikost souboru při zachování původní věrnosti dat. Komprimovaná verze souborů LAS je často označována jako LAZ, která nabízí efektivní možnosti ukládání a přenosu dat.

## Reference

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
