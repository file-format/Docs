{
  "date" : "2019-10-11",
  "keywords" :[ "soubor vrml", "formát souboru vrml", "co je soubor vrml", "soubor", "příklad vrml", "přípona souboru vrml", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru VRML",
  "description":"Další informace o formátu souboru VRML a rozhraních API, která mohou otevírat a vytvářet soubory VRML.",
  "linktitle" : "VRML",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor VRML?
Jazyk modelování virtuální reality (VRML) je formát souboru pro reprezentaci interaktivních [3D](/cs/3d/) objektů světa přes World Wide Web (www). Své využití nachází při vytváření trojrozměrných reprezentací složitých scén, jako jsou ilustrace, definice a prezentace virtuální reality. Formát byl nahrazen formátem [X3D](/cs/3d/x3d/). Mnoho aplikací pro 3D modelování může ukládat objekty a scény ve formátu VRML.

## Formát souboru VRML

VRML je formát textového souboru, který specifikuje informace, jako jsou vrcholy a hrany 3D polygonu, spolu s informacemi, jako je barva povrchu, UV mapované textury, lesk, průhlednost a tak dále. Má schopnost reprezentovat statické a animované objekty a navíc má hypertextové odkazy na jiná média, jako je zvuk, filmy a obrázky. To umožňuje otevírání prvků s hypertextovými odkazy, když uživatel na tyto objekty klikne.

Soubory TVRML se v běžné terminologii nazývají „světy“ a mají příponu .wrl. Textová povaha těchto souborů umožňuje zmenšit velikost souboru pomocí kompresních formátů, jako je gzip, což je činí výhodnějšími pro rychlý přenos přes internet. Specifikace formátu souborů pro [VRML v 2.0](http://gun.teipir.gr/VRML-amgem/spec/index.html) slouží jako reference pro vývojáře pro vytváření aplikací kompatibilních pro čtení/zápis těchto souborů.

## Kritérium designu ##

Cíl a návrh VRML se točí kolem následujících požadavků.

* **Oprávnění** – Umožňuje vyvíjet generátory aplikací a editory a importovat data z jiných průmyslových formátů
* **Úplnost** – Poskytuje všechny informace potřebné pro implementaci a řeší kompletní sadu funkcí pro širokou průmyslovou akceptaci
* **Složitelnost** - Schopnost používat prvky VRML v kombinaci a umožnit tak opětovnou použitelnost.
* **Rozšiřitelnost** - Možnost přidávat nové prvky.
* **Implementovatelnost** -Možnost implementace na širokou škálu systémů.
* **Potenciál pro více uživatelů** – Nemělo by bránit implementaci prostředí pro více uživatelů.
* **Ortogonalita** – Prvky VRML by měly být na sobě nezávislé nebo by jakékoli závislosti měly být strukturované a dobře definované.
* **Výkon** – Prvky by měly být navrženy s důrazem na interaktivní výkon na různých počítačových platformách.
* **Škálovatelnost** – Prvky VRML by měly být navrženy pro nekonečně velké kompozice.
* **Standardní praxe** – Standardizovány by měly být pouze ty prvky, které odrážejí stávající praxi, které jsou nezbytné pro podporu stávající praxe nebo které jsou nezbytné pro podporu navrhovaných norem.
* **Dobře strukturovaný** – Prvek by měl mít dobře definované rozhraní a jednoduše stanovený bezpodmínečný účel. Je třeba se vyvarovat víceúčelových prvků a vedlejších účinků.

## Reference ##

* [VRML – podle Wikipedie](https://en.wikipedia.org/wiki/VRML)
* [Specifikace formátu souboru VRML v 2.0](http://gun.teipir.gr/VRML-amgem/spec/index.html)

