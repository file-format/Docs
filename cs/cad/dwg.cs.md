{
  "date" : "2020-03-16",
  "keywords" :[ "DWG", "Formát souboru", "CAD", "Otevřít", "Vytvořit" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů DWG a rozhraních API, která mohou vytvářet a otevírat soubory DWG.",
  "title" :"Formát souboru DWG",
  "linktitle" : "DWG",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor DWG?

Soubory s příponou DWG představují proprietární binární soubory používané pro uložení 2D a 3D návrhových dat. Stejně jako DXF, což jsou soubory ASCII, představuje DWG binární formát souboru pro výkresy CAD (Computer Aided Design). Obsahuje vektorový obrázek a metadata pro reprezentaci obsahu CAD souborů. Pro prohlížení souborů DWG v operačním systému Windows jsou k dispozici bezplatné prohlížeče, jako je bezplatný DWG TrueView společnosti Autodesk. Existují i další aplikace třetích stran, které podporují dosažení souborů DWG. Soubory DWG obsahují informace vytvořené uživatelem a zahrnují:

* Návrhy
* Geometrické údaje
* Mapy a fotografie

Tento formát je široce používán architekty, inženýry a designéry pro různé účely navrhování.

## Stručná historie ##

Formát souboru DWG se od svého formálního představení v roce 1982 postupem času vyvíjel. Následuje stručný přehled minulých událostí z pohledu historie.

**1982:** Autodesk licencoval formát souborů DWG, který vyvinul Mike Riddle v roce 1970, jako základ pro AutoCAD.

**1998:** S vydáním AutoCAD R14.01 přidal Autodesk ověřování souborů pomocí funkce nazvané DWGCHECK, která do souborů DWG vytvořených programem vložila zašifrovaný kontrolní součet a produktový kód, který Autodesk nazývá WaterMark.

**2006:** Autodesk upravil AutoCAD 2007 tak, aby zahrnoval "technologii TrustedDWG" pro vložení textového řetězce "Autodesk DWG. Tento soubor je důvěryhodný DWG naposledy uložený aplikací Autodesk nebo licencovanou aplikací Autodesk" do souborů DWG. Účelem bylo pomoci uživatelům softwaru Autodesk zajistit, aby tyto soubory byly vytvořeny aplikací Autodesk nebo RealDWG, což by rozhodně mělo pomoci snížit riziko nekompatibility.

## Struktura souboru ##

DWG je jedním z široce používaných formátů souborů v řadě aplikací a má robustní strukturu souborů. Protože DWG je binární formát souboru, není čitelný pro člověka jako prostý formát souboru ASCII [DXF](/cs/cad/dxf/). Soubory DWG obvykle obsahují informace o souřadnicích obrázku a jakýchkoli metadatech s nimi spojených. Kompletní [specifikace](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf) formátu souboru DWG jsou k dispozici ke stažení prostřednictvím OpenDesign. Struktura souboru formátu DWG je shrnuta následovně.

**Header**: Hlavička souboru se skládá z proměnných DWG Header a informací o Cyclic Redundancy Check (CRC), která se používá pro detekci chyb. Každá podsekce je specializovaný vektor, kde se k reprezentaci různých štítků používají různé délky bitů. Například prvních 6 bitů proměnné záhlaví DWG představuje řetězec verze.

**Definice tříd:** Soubor DWG může obsahovat mnoho tříd v závislosti na konkrétním účelu souboru .dwg. Kromě jiných informací, jako je velikost metadat třídy v oblasti dat třídy, číslo třídy a kontrolní součet.

**Šablona**: Toto je volitelné a pro verze R15 a R15 je tato sekce pod sekcí Object Free Space.

**Padding**: Metadata mají příponu a dodatečnou fixaci s určitým počtem bajtů, díky čemuž jsou starší verze softwaru AutoCAD dále kompatibilní s novým formátem souborů DWG.

**Data obrázku**: Metadata pro tuto sekci závisí na konkrétním typu .dwg. Pro uživatele R14 a R15 je tato část volitelná.

**Objektová data**: Objektová data se skládají z kompletního seznamu entit tabulky, slovníkových položek atd. odpovídajících existujícímu seznamu objektů.

**Mapa objektů**: Umístění každého objektu v souboru je specifikováno v této části souboru. Většina metadat v této části jsou popisovače souborů, které hrají roli při identifikaci a opětovném vykreslení objektu.

**Object Free Space**: Tato sekce je volitelná pro všechny uživatele

**Second Header**: Duplikát sekce záhlaví souboru ke konci souboru DWG

## Reference ##

* [Specifikace formátu souboru DWG](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)
* [Specifikace souboru DWG](https://www.scan2cad.com/dwg/file-spec/)
* [DWG – podle Wikipedie](https://en.wikipedia.org/wiki/.dwg)

