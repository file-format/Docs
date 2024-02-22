{
  "date" : "2023-01-16",
  "keywords" : [ "DLIS", "what is a DLIS file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Přečtěte si o formátu souboru DLIS a rozhraních API, která mohou vytvářet a otevírat soubory DLIS.",
  "title" : "Formát souboru DLIS – datový soubor Well Log",
  "linktitle" : "DLIS",
  "menu" : {
    "docs" : {
      "identifier":"database-dlis-cs",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-16"
}

## Co je soubor DLIS?

Formát souboru .dlis je standardní formát souboru pro ukládání a výměnu dat z vrtů v ropném a plynárenském průmyslu. Formát byl vyvinut výborem Logging Industry Data Standard (LIDS) a znamená Digital Log Information Standard. Formát je navržen tak, aby dobře ukládal data protokolů způsobem, který lze snadno číst, zapisovat a vyměňovat mezi různými systémy.

Soubory DLIS obsahují sadu logických záznamů, které popisují data protokolu z vrtu a jeho charakteristiky, jako je typ dat protokolu (např. měrný odpor, gama záření), jednotky měření a umístění dat ve vrtu. Skutečná data protokolu jsou uložena v samostatných binárních souborech a odkazují se na ně logické záznamy v souboru DLIS.

## Stručné informace o datech záznamu studny

Data z vrtů jsou záznamem měření provedených v různých hloubkách vrtu, obvykle během procesu vrtání nebo po vyvrtání vrtu. Tato měření mohou zahrnovat různé fyzikální, chemické a/nebo geofyzikální vlastnosti horniny a tekutin ve vrtu. Některé příklady dat protokolu studní zahrnují:

- Elektrický odpor: míra schopnosti horniny odolávat toku elektrického proudu
- Gama záření: míra přirozené radioaktivity horniny
- Pórovitost: míra množství otevřených prostorů nebo pórů v hornině
- Sonic: měřítko času, který potřebuje zvuková vlna, aby prošla skálou
- Hustota: míra hmotnosti horniny na jednotku objemu
- Litologie: měřítko typu horniny nebo útvaru

Data z vrtů se používají pro různé účely v ropném a plynárenském průmyslu, jako jsou:

- Identifikace umístění a kvality formací obsahujících uhlovodíky
- Vyhodnocení produkčního potenciálu vrtu
- Plánování a sledování dokončení a stimulace studny
- Monitorování chování studny v průběhu času

## Vztah s PPDM

PPDM (Professional Petroleum Data Management) je standard pro správu dat ropného a plynárenského průmyslu, který poskytuje společný datový model pro správu dat o vrtech a těžbě. Datový model PPDM definuje sadu standardních datových objektů a vztahů, které lze použít k organizaci a správě dobře logovaných dat, včetně dat DLIS.

Datový model PPDM zahrnuje datové objekty pro vrtná a produkční data, jako jsou studny, hlavičky vrtů, protokoly vrtů a produkční data. Zahrnuje také vztahy mezi těmito datovými objekty, jako je vztah mezi studnou a protokoly studny, které jsou s ní spojeny.

Datový model PPDM poskytuje konzistentní, průmyslově standardní způsob organizace a správy protokolovaných dat, včetně dat DLIS. Umožňuje různým organizacím sdílet a vyměňovat si data pomocí společného datového modelu, což zlepšuje interoperabilitu dat a snižuje náklady na integraci dat.

Použití datového modelu PPDM a dat DLIS společně umožňuje ukládat a spravovat dobře logovaná data způsobem, který je v souladu s průmyslovými standardy a snadno dostupný pro jiné systémy a aplikace.


