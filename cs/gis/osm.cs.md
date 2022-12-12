{
  "date" : "2019-10-11",
  "keywords" :[ "soubor osm", "co je soubor osm", "soubor", "příklad osm", "přípona souboru osm", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OSM - OpenStreetMap File Format",
  "description":"Další informace o formátu souborů OSM a rozhraních API, která mohou vytvářet a otevírat soubory OSM.",
  "linktitle" : "OSM",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor OSM?

OpenStreetMap (OSM) je obrovská sbírka dobrovolných úložišť geografických informací v různých typech souborů s použitím různých schémat kódování k převodu těchto dat na bity a bajty. OSM je společné úsilí o vytvoření volně upravitelné mapy světa. Primárním výstupem tohoto společného úsilí jsou spíše geografická data než samotná mapa. Omezení používání nebo dostupnosti geografických informací ve velké části světa vyvolává potřebu vytvořit OSM. Data dostupná z OSM jsou připravena nahradit Google Maps pro klasické aplikace (Facebook, Craigslist atd.) a výchozí data pro aplikace GPS přijímače.^^ ^^I když je kvalita dat po celém světě různorodá, data OpenStreetMap lze pohodlně porovnat s patentem zdroje dat.

## Stručná historie ##

Britský podnikatel Steve Coast, inspirovaný úspěchem Wikipedie, vytvořil v roce 2004 tento komunitní projekt mapování světa ve Spojeném království. Zpočátku se zaměřil na mapování Spojeného království. OpenStreetMap Foundation byla poprvé založena v dubnu 2006 na podporu vývoje, expanze a oběhu bezplatného geoprostoru pro kohokoli. V prosinci 2006 společnost Yahoo pomohla OpenStreetMap se svým leteckým snímkováním pro tvorbu map. Kompletní údaje o silnicích pro Nizozemsko a údaje o hlavních silnicích pro Indii a Čínu byly do OSM poskytnuty v dubnu 2007 společností Automotive Navigation Data (AND). V prosinci 2007 byla Oxfordská univerzita nejvýznamnější organizací, která integrovala data OpenStreetMap do své hlavní webové stránky. Od té doby více než 2 miliony registrovaných uživatelů přispívají do tohoto projektu daty pomocí zařízení GPS, leteckého snímkování a ručních průzkumů. Tato data přidaná komunitou jsou zpřístupněna pod licencí Open Database License. Nezisková organizace OpenStreetMap Foundation registrovaná v Anglii udržovala stránky OSM.

## Formát souboru OSM ##

Existuje mnoho způsobů a formátů souborů pro ukládání geografických dat, ale formát souboru **OSM** je omezen na OpenStreetMap. OSM je speciálně navržený standardní formát určený pro snadný přenos přes internet. Strukturovaný uspořádaný formát kódovaný v XML tvoří soubor .osm. V OpenStreetMap jsou čtyři hlavní prvky pro uložení topologické datové struktury:

{{< figure src="../OSM.png" alt="Formát souboru OSM" >}}


|Uzly|Způsoby|Vztahy|Značky
---|---|---|---|
|<ul><li> Představuje zeměpisnou polohu uloženou jako dvojice zeměpisné šířky a délky.</li><li> Používá se k zobrazení mapových prvků bez velikosti, jako jsou horské štíty.</li></ul> |<ul><li> Seřazené seznamy uzlů označující křivku nebo mnohoúhelník</li><li> Představují lineární prvky, jako jsou silnice a řeky, a zóny, jako jsou parkovací plochy, džungle a parky.</li></ul> |<ul><li> Seřazené seznamy uzlů a cest představují jejich vztah, jako jsou bariéry a odbočky u na silnicích, dálnice překlenují různé stávající cesty a oblasti s dírami.</li></ul> |<ul><li> Ukládejte metadata o objektech mapy.* Vždy připojené k jakémukoli uzlu, způsobu nebo relaci</li></ul>


Tagy se používají k charakterizaci fyzických prvků na zemi (budovy a silnice atd.) v OpenStreetMap. Každá značka souvisí s geografickou charakteristikou prvku reprezentovaného tímto konkrétním uzlem nebo vztahem. V tomto bezplatném značkovacím systému lze k popisu funkce zahrnout do mapy neomezený počet atributů. Specifické kombinace klíčů a hodnot schválené registrovanými uživateli fungují jako neformální standardy pro často používané značky. Nové značky však lze vytvořit, kdykoli nové aspekty vyžadují analýzu dříve nezmapovaných atributů prvků. Většina funkcí používá pro popis pouze malý počet značek.

OSM používá k ukládání hlavních dat tři typy souborů.

OSM zpracovává všechny tyto soubory s informacemi o podrobnostech jejich formátování. Tyto soubory však vytvářejí stejné vnitřní objekty. U datových souborů je viditelný příznak na objektech OSM vždy pravdivý, což neplatí pro soubory historie a změn.

V běžném používání existuje rozmanitost formátů souborů OSM. Formáty souborů definují kódování obsahu na disku nebo drátu v bitech a bajtech. OSM je schopen číst a zapisovat maximálně z těchto formátů.

**XML**

Původní formát OSM je založen na XML. Návratová data hlavního API OSM databáze jsou ve formátu XML.

**PBF**

Kódování Protocol Buffers je založeno na binárním formátu a je jedním z nejkompaktnějších formátů.

**O5M/O5C**

Jednodušší formát založený na binárním formátu, ale relativně méně používaný. OSM umí tento formát číst, ale nemůže zapisovat.

**OPL**

Jednoduchý formát navržený pro použití se standardními nástroji příkazového řádku systému UNIX. V blízkosti souborů CSV, umožňuje jednu entitu OSM na jednom řádku.

**LADIT**

Textový formát určený k vytvoření pro ladění. OSM může zapisovat tento formát, ale nemůže číst.

**ČERNÁ DÍRA**

Falešný formát, který odstraňuje všechna data. OSM může zapisovat tento formát, ale nemůže číst.

## Úložiště dat OSM ##

Hlavní databáze OSM **PostgreSQL** uchovává hlavní kopii dat OSM s rozšířením PostGIS. Pro každé datové primitivum udržuje hlavní databáze tabulku, jejíž řádky ukládají jednotlivé objekty. Všechny úpravy aktualizují tuto databázi a všechny ostatní formáty jsou vytvářeny pomocí této databáze. Pro přenos dat z jednoho místa na druhé jsou vytvořeny četné databáze ke stažení. Tyto fondy definují dva formáty, jeden využívající XML a druhý využívající Binární formát vyrovnávací paměti protokolu (PBF). Kompletní data jsou uložena v souboru planet.osm

## Komprese v souborech OSM ##

Textové formáty (XML, OPL a Debug) volitelně používají kompresi gzip nebo bzip2.

## Reference ##

* [Příručka k formátům souborů OSM](https://osmcode.org/file-formats-manual/#file-types)
* [OpenStreetMap](https://en.wikipedia.org/wiki/OpenStreetMap#History)
* [Naučte se OSM](https://learnosm.org/en/osm-data/getting-data/)

