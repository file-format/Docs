{
  "date" : "2021-07-29",
  "keywords" :[ "soubor gpkg", "formát souboru gpkg", "co je soubor gpkg", "soubor", "příklad gpkg", "přípona souboru gpkg", "přípona", "formát" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPKG - GeoPackage Format Files",
  "description":"Další informace o formátu souborů GPKG a rozhraních API, která mohou vytvářet a otevírat soubory GPKG.",
  "linktitle" : "GPKG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## Co je soubor GPKG?
Soubor s příponou .gpkg se skládá z geografického informačního systému implementovaného jako databázový kontejner SQLite obsahující tabulky dat a metadat s typickými definicemi, omezeními formátu, tvrzeními o integritě a omezeními obsahu. Vyšlo v roce 2014; definované OGC (Open Geospatial Consortium) jménem americké armády. Různé vládní, komerční a open source organizace široce podporují GeoPackage.

## Formát souboru GPKG
GeoPackage je vytvořen jako rozšířený databázový soubor SQLite 3; standard definuje sadu pravidel (požadovaných konvencí) pro:
- Ukládání sad snímků s dlaždicovou matricí
- Vektorové funkce
- Rastrové mapy v různých měřítcích
- Metadata a schéma

GeoPackage můžete rozšířit pomocí pravidel rozšíření definovaných v článku 2.3 standardu. Účelem návrhu GeoPackage bylo vytvořit co nejvíce odlehčenou databázi a zahrnout ji do jednoho souboru připraveného k použití. Díky tomu je ideální pro mobilní aplikace v off-line režimu a rychlé sdílení na cloudovém úložišti nebo úložných zařízeních USB atd.

### Obsah GPKG
GeoPackages obsahují řadu tabulek, stejně jako jiné relační databáze. Tyto tabulky mohou být buď uživatelem definované, nebo tabulky metadat. GeoPackages se skládají ze dvou povinných tabulek metadat:

#### gpkg_contents
Obsah pro GeoPackage. Povinné sloupce v této tabulce jsou:

- **název_tabulky**: skutečný název uživatelsky definované datové tabulky;
- **data_type**: typ dat, např. názvy, vlastnosti a atributy;
- **identifikátor a popis**: text čitelný pro člověka ;
- **last_change**: informační datum poslední změny ve formátu ISO 8601;
- **min_x, min_y, max_x a max_y**: prostorové rozsahy obsahu. ;
- **srs_id**: prostorový referenční systém .

#### gpkg_spatial_ref_sys
Pro prostorový referenční obsah; včetně, ale bez omezení na dlaždice a prvky, každý řádek v obsahu musí odkazovat na souřadnicový referenční systém; uloženy v tabulce **gpkg_spatial_ref_sys**. Povinné sloupce v této tabulce jsou:

- **srs_name, description**: lidsky čitelný název a popis SRS;
- **srs_id**: jedinečný identifikátor pro SRS; také primární klíč pro tabulku;
- **organizace**: Název definující organizace bez ohledu na malá a velká písmena.
- **organization_coordsys_id**: číselné ID SRS přidělené organizací;
- **definice**: Definice dobře známého textu SRS.


## Reference

* [GeoPackage – od Wikipedie)](https://en.wikipedia.org/wiki/GeoPackage)
* [Začínáme s GeoPackage] (http://www.geopackage.org/guidance/getting-started.html)

