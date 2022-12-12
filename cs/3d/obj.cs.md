{
  "date" : "2019-10-11",
  "keywords" :[ "soubor obj", "formát souboru obj", "co je soubor obj", "soubor", "příklad obj", "přípona souboru obj", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru OBJ",
  "description":"Další informace o formátu souboru OBJ a rozhraních API, která mohou otevírat a vytvářet soubory OBJ.",
  "linktitle" : "OBJ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor OBJ?

Soubory **OBJ** používá aplikace Advanced Visualizer společnosti Wavefront k definování a ukládání geometrických objektů. Zpětný a dopředný přenos geometrických dat je umožněn prostřednictvím souborů OBJ. Formát OBJ podporuje jak polygonální geometrii jako body, čáry, vrcholy textur, plochy, tak geometrii volného tvaru (křivky a plochy). Tento formát nepodporuje animaci ani informace související se světlem a polohou scén.

Soubor OBJ je obvykle konečným produktem procesu 3D modelování generovaného CAD (Computer Aided Design). Výchozí pořadí pro ukládání vrcholů je proti směru hodinových ručiček, aby se zabránilo explicitní deklaraci normál ploch. Ačkoli soubory OBJ deklarují informace o měřítku v řádku komentáře, pro souřadnice OBJ nebyly deklarovány žádné jednotky.

## Historie formátu 3D OBJ

Společnost Wavefront Technologies vytvořila formát souboru OBJ pro svou aplikaci Advanced Visualizer pro ukládání geometrických objektů a 3D dat. Jeho verze 2.11 je nahrazena nově zdokumentovanou verzí 3. Formát souboru je otevřený a byl implementován jinými dodavateli pro jejich 3D grafickou aplikaci. Společnost Wavefront Technologies ponechala tento formát souborů otevřený a neutrální.

## Formát souboru OBJ

Ve 3D objektech je kódování geometrie povrchu náročná práce, kterou formát souboru OBJ zvládl velmi dobře. Tento formát je poměrně univerzální, protože nabízí řadu možností kódování geometrie povrchu. Níže jsou uvedeny tři povolené formáty, které mají své výhody a nevýhody:

### Teselace s polygonálními plochami

Formát souboru OBJ usnadňuje uživateli mozaikování povrchu 3D modelu pomocí jednoduchých nebo složitých geometrických tvarů. Pro kódování povrchové geometrie modelu ukládá soubor vrcholy a normály ke každému polygonu. Teselace sice zvyšuje hrubost modelu, přesto je nutné najít správnou rovnováhu mezi velikostí souboru a kvalitou tisku.

### Křivka volného tvaru

Formát souboru OBJ umožňuje uživatelem definovaným volným povrchovým křivkám určit povrchovou geometrii modelu. Protože křivky volného tvaru jsou složitější než polygonální plochy, protože s několika matematickými parametry lze zakřivené čáry nejlépe definovat křivkami volného tvaru. Proto s menším počtem dat ve srovnání s polygonálními teselacemi se křivky volného tvaru používají ke generování vysoce kvalitního kódování jakéhokoli 3D modelu bez zvětšení velikosti souboru.

### Volně tvarované povrchy

Formát souboru OBJ také specifikuje skládání geometrie povrchu pomocí volných ploch. Tento druh povrchových záplat volného tvaru (NURBS) je velmi vhodný pro povrchy bez pevných radiálních rozměrů, jako je korba nákladního auta, křídla vrtulníku nebo trup lodi. Použití povrchů s volným tvarem je velmi výhodné, protože jsou přesnější, aby udržely menší velikosti souborů při vyšší přesnosti. Tyto povrchy jsou nezbytnou součástí leteckého a automobilového průmyslu, kde je nízká přesnost neúprosná.

Následující klíčová slova jsou uspořádána podle datového typu pro definování geometrie povrchu.


|Prvky|Příkazy těla volné křivky/plochy|Atributy volné křivky/plochy
---|---|---|
|p|Bod|parm|Hodnoty parametrů|stupeň|Stupeň
|l|Line|trim|Vnější ořezávací smyčka|bmat|Základní matice
|f|Obličej|otvor|Vnitřní zastřihovací smyčka|krok|Velikost kroku
|curv|Curve|scrv|Speciální křivka|cstype|Křivka nebo typ povrchu
|curv2|2D křivka|sp|Speciální bod|**Konektivita a seskupení ploch**
|surf|Surface|end|Ukončit příkaz|con|connect
|**Zobrazit/vykreslit atributy**|g|Název skupiny
|úkos|Interpolace zkosení|shadow_obj|Odlévání stínů|s|Vyhlazovací skupina
|lod|Úroveň podrobností|trace_obj|Ray tracing|mg|Slučovací skupina
|d_interp|Rozpustit interpolaci|ctech|Technika aproximace křivky|o|Název objektu
|c_interp|Interpolace barev|stech|Technika aproximace povrchu|
|usemtl|Název materiálu|mtllib|Knihovna materiálů|
|**Geometrické vrcholy**|
|v|Geometrické vrcholy|vn|Normály vrcholů|
|vt|vrcholy textur|vp|vrcholy prostoru parametrů|

### Barva a textura

Soubor OBJ umožňuje ukládat informace o barvách a texturách v přidruženém formátu souboru zvaném Knihovna šablon materiálu (MTL). Vícebarevné geometrické modely se vykreslují pomocí těchto dvou souborů dohromady. Soubory MTL jsou založeny na ASCII a usnadňují počítačové vykreslování tím, že popisují vlastnosti povrchu odrážející světlo pomocí modelu Phongova odrazu. Standard byl přijat velkým počtem dodavatelů softwaru, kteří využívají jeho výhod pro výměnu materiálů. Formát MTL je mírně zastaralý, protože nemá podporu v nejnovějších technologiích, jako jsou zrcadlové a paralaxové mapy.

## Reference

* [Soubor .obj Wavefront](https://en.wikipedia.org/wiki/Wavefront_.obj_file)

