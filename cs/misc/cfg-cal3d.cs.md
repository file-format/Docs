{
"datum": "27.09.2023",
  "keywords": [
"cfg",
"cfg soubor",
"konfigurační soubor modelu cfg cal3d",
"co je soubor cfg",
"jak otevřít soubor cfg",
"soubor",
"přípona souboru cfg",
"rozšíření"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formát souboru CFG - konfigurační soubor modelu Cal3D",
  "description":"Další informace o formátu konfiguračního souboru modelu CFG Cal3D a rozhraní API, která mohou vytvářet a otevírat soubory CFG.",
  "linktitle": "CFG Cal3D",
  "menu": {
    "docs": {
      "identifier": "misc-cfg-cal3d",
      "parent": "misc"
}
},
"lastmod": "27.09.2023"
}

## Co je soubor CFG?

Konfigurační soubor modelu Cal3D je textový soubor používaný knihovnou Cal3D, což je open-source sada nástrojů pro animaci postav. Tento soubor slouží jako plán pro sestavení trojrozměrného (3D) modelu. Obsahuje odkazy na různé součásti modelu, jako je struktura kostry, materiály, animace a další. V podstatě funguje jako centrální dokument, který pomáhá organizovat a definovat, jak do sebe všechny části 3D modelu zapadají v rámci Cal3D.

Cal3D je skeletální animační knihovna často používaná v počítačové grafice a vývoji her. Chcete-li pracovat s modely Cal3D, obvykle potřebujete vytvořit konfigurační soubor, který popisuje strukturu modelu, materiály, animace a další atributy. Níže je uveden příklad, jak může konfigurační soubor modelu Cal3D vypadat.

```
<MODEL>
  <HEADER MAGIC="C3D" VERSION="1050" />

  <!-- Skeleton -->
  <SKELETON>
    <BONE ID="0" NAME="Root">
      <TRANSLATION>0.0 0.0 0.0</TRANSLATION>
      <ROTATION>0.0 0.0 0.0</ROTATION>
      <SCALE>1.0 1.0 1.0</SCALE>
    </BONE>
    <!-- Add more bone definitions here -->
  </SKELETON>

  <!-- Mesh -->
  <MESH>
    <SUBMESH>
      <MATERIAL>MATERIAL_NAME</MATERIAL>
      <VERTEX>
        <!-- Vertex data for the first vertex -->
        <POSITION>0.0 0.0 0.0</POSITION>
        <NORMAL>0.0 0.0 1.0</NORMAL>
        <TEXCOORD>0.0 0.0</TEXCOORD>
        <!-- Add more vertices here -->
      </VERTEX>
      <FACE>
        <!-- Face data for the first face -->
        <VERTEXID>0 1 2</VERTEXID>
        <!-- Add more faces here -->
      </FACE>
      <!-- Add more submeshes here -->
    </SUBMESH>
  </MESH>

  <!-- Animation -->
  <ANIMATION>
    <SKELETON>
      <!-- Define animations and keyframes here -->
    </SKELETON>
  </ANIMATION>

</MODEL>
```

## Cal3D

Cal3D je open-source knihovna animací postav používaná ve 3D počítačové grafice a vývoji her. Poskytuje nástroje a funkce pro vytváření a animaci 3D postav nebo modelů. Cal3D se často používá k tomu, aby do interaktivních aplikací a her přinesl realistické animace postav.

Mezi klíčové vlastnosti a komponenty Cal3D patří:

1. **Síť:** Komponenta sítě definuje 3D geometrii postavy nebo objektu, včetně vrcholů, normál a souřadnic textury. Tvoří vizuální reprezentaci modelu.

2. **Skeleton:** Cal3D umožňuje vytvoření hierarchie kostry pro modely postav. Tato kostra definuje strukturu kosti a každá kost může být spojena s částí sítě. Kostry jsou klíčové pro animaci postav manipulací s kostmi.

3. **Materiály:** Materiály definují, jak by měl povrch modelu vypadat při vykreslování. To zahrnuje informace o texturách, shaderech a dalších vlastnostech vykreslování.

4. **Animace:** Cal3D podporuje různé animační techniky, které lze aplikovat na kostru. Tyto animace definují, jak se kosti v průběhu času pohybují a vytvářejí realistické animace postav, jako je chůze, běh nebo provádění jiných akcí.

5. **Konfigurační soubory:** Pro efektivní využití Cal3D jsou modely často doprovázeny konfiguračními soubory ve formátu prostého textu. Tyto soubory popisují strukturu modelu, včetně hierarchie kostí, dat sítě, materiálů a informací o animaci. Konfigurační soubory slouží jako reference pro Cal3D pro správné načtení a interakci s modelem.

## Formáty souborů používané Cal3D

Cal3D používá několik formátů souborů pro různé účely, jako je ukládání dat modelu, animací a konfiguračních informací. Zde jsou některé z běžných formátů souborů používaných Cal3D:

1. **Soubory binárních modelů Cal3D (.cmf):** Tyto soubory ukládají binární reprezentaci 3D modelů, včetně geometrie sítě, hierarchie kostí a materiálů. Soubory CMF se používají k efektivnímu načítání a vykreslování Cal3D modelů v aplikacích.

1. **Cal3D XML Model Files (.cmx):** Soubory založené na XML, které ukládají textovou reprezentaci Cal3D modelů. Obsahují informace o struktuře modelu, animacích, materiálech a další. Soubory [CMX](/cs/image/cmx/) se často používají pro snadněji čitelné úpravy a ladění.

1. **Cal3D Animation Files (.caf):** Tyto soubory ukládají data animací, včetně klíčových snímků a kostních transformací. Soubory CAF jsou nezbytné pro definování toho, jak se mají postavy nebo objekty pohybovat a animovat v modelu Cal3D.

1. **Cal3D Morph Target Files (.crf):** Používá se k definování morph cílů, které umožňují výrazy obličeje a další neskeletové deformace sítě.

1. **Soubory materiálů Cal3D (.cfm):** Tyto soubory ukládají informace o materiálu pro modely Cal3D. Určují, jak by měl být povrch modelu stínován, včetně odkazů na textury, shaderů a vlastností vykreslování.

1. **Cal3D Skeleton Files (.csf):** Soubory Skeleton ukládají informace o hierarchii kostí a struktuře modelu Cal3D. Definují, jak jsou kosti spojené a rodičovské v rámci kostry.

1. **Konfigurační soubory Cal3D (.cfg):** Tyto soubory ve formátu prostého textu slouží jako konfigurační soubory pro modely Cal3D. Obsahují odkazy na různé součásti modelu, včetně hierarchie kostí, dat sítě, materiálů a animací. Konfigurační soubory pomáhají Cal3D správně načíst a používat model.

1. **Formáty obrázků:** I když to není specifické pro Cal3D, formáty obrázkových souborů jako [JPEG](/cs/image/jpeg/), [PNG](/cs/image/png/), [BMP](/cs/image/bmp/ ), nebo [TGA](/cs/image/tga/) se běžně používají pro textury aplikované na modely Cal3D.

## Jak otevřít soubor CFG?

Programy, které otevírají soubory CFG, zahrnují

- Cal3dViewer
- Microsoft Poznámkový blok
- Apple TextEdit
- Jakýkoli textový editor

## Jiné soubory CFG

Zde jsou další typy souborů, které používají příponu souboru **.cfg**.

**Nastavení**
- [CFG - Celestia Configuration File](/cs/settings/cfg-celestia/)
- [CFG - Soubor připojení serveru Citrix](/cs/settings/cfg-citrix/)
- [CFG - Konfigurační soubor MAME](/cs/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/cs/settings/cfg-lightwave/)

**Hra**
- [CFG - Wesnoth Markup Language File](/cs/game/cfg-wesnoth/)
- [CFG - Konfigurační soubor MUGEN](/cs/game/cfg-mugen/)
- [CFG - konfigurační soubor zdrojového enginu](/cs/hra/cfg-sourceengine/)

**Systém a různé**
- [CFG - Soubor CFG](/cs/system/cfg/)
– [CFG – konfigurační soubor modelu Cal3D](/cs/misc/cfg-cal3d/)

## Reference
* [CAL3D](https://github.com/mp3butcher/Cal3D)
