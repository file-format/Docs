{
"date":"2023-10-11",
   "keywords":[
"shader",
"shader soubor",
"shader quake 3 engine shader soubor",
"jak otevřít soubor shaderu",
"soubor",
"přípona souboru shaderu",
"rozšíření",
"soubor"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"Formát souboru SHADER - soubor Quake 3 Engine Shader",
   "description":"Další informace o formátu souboru SHADER Quake 3 Engine Shader a rozhraních API, která mohou vytvářet a otevírat soubory SHADER.",
"linktitle":"SHADER Quake",
   "menu":{
      "docs":{
         "identifier":"game-shader-quake",
         "parent":"game"
}
},
"lastmod":"2023-10-11"
}

## Co je soubor SHADER?

Formát souboru SHADER se používá v **Quake 3 engine** k definování shaderů pro textury a materiály ve hře. Shadery se používají k určení, jak má být povrch vykreslen, včetně jeho vzhledu, odrazivosti, průhlednosti a dalších vizuálních vlastností.

## Soubor Quake 3 Engine SHADER

Zde je základní přehled struktury a syntaxe souboru shader enginu Quake 3:

```Plain Text
// Comments can be added with double slashes

// A shader is defined with "shader" keyword followed by shader name
shader shader_name
{
    // Properties and stages of shader are defined within curly braces

    // The properties for this shader are specified using key-value pairs
    // Common properties include surfaceparm, cull, deformvertexes, q3map_*, etc.

    // Example properties:
    surfaceparm nolightmap
    cull disable

    // Stages of shader are defined using stage keyword
    stage
    {
        // The properties for this stage are also specified using key-value pairs

        // Example stage properties:
        texture texture_filename
        // texture is used to specify image file for this stage

        // Additional properties for this stage can include blending modes,
        // scrolling, scaling and other texture manipulation settings.
        // These can be specified with key-value pairs.

        // Example stage properties:
        blendFunc GL_DST_COLOR GL_SRC_COLOR
        // Specifies a blending mode

        tcMod scroll 0.1 0.1
        // Scrolls texture in S and T direction

        tcMod scale 2 2
        // Scales texture

        // You can have multiple stages within a shader, each with its own properties
    }
}
```

V souboru shaderu Quake 3 engine můžete definovat více shaderů, každý s vlastní sadou vlastností a fází. Tyto shadery se používají k definování vzhledu různých textur a materiálů v herním světě. Engine tyto informace využívá k vykreslování povrchů se zadanými vizuálními efekty a chováním.

Shader soubory v Quake 3 engine jsou jednoduché textové soubory, které obsahují instrukce, jak by se textury a materiály měly objevit ve hře. Tyto soubory lze otevřít a upravit pomocí běžného textového editoru a obvykle se nacházejí v adresáři **"/scripts"** v balíčku .PK3 hry.

## Motor Quake 3

Quake 3 engine je vysoce vlivný a všestranný herní engine vyvinutý společností id Software. Poprvé byl představen s vydáním hry „Quake III Arena“ v roce 1999 a od té doby byl použit v různých dalších hrách. Engine je známý pro svou pokročilou grafiku, možnosti pro více hráčů a upravitelnost.

Zde jsou některé klíčové vlastnosti a aspekty enginu Quake 3:

1. **Grafický engine:** Quake 3 engine byl ve své době proslulý svou špičkovou grafickou technologií. Představil pokročilé funkce, jako jsou zakřivené povrchy, shadery a dynamické osvětlení, které byly na konci 90. let přelomové.
    





2. **Zaměření na více hráčů:** Quake 3 Arena byla primárně navržena jako střílečka z pohledu první osoby pro více hráčů. Síťový kód enginu a podpora online hraní pro více hráčů byly výjimečné, díky čemuž se stal populární volbou pro soutěžní online hraní.
    





3. **Modifikovatelnost:** Quake 3 engine je známý svou modifikovatelností. id Software uvolnil zdrojový kód motoru pod open-source GNU General Public License (GPL). To povzbudilo vytváření mnoha modů a vlastních map, což vedlo k živé moddingové komunitě.
    





4. **Skriptovaná hratelnost:** Engine používal k definování herních pravidel a chování systém založený na skriptech, díky čemuž bylo pro moddery a mappery relativně snadné vytvářet vlastní herní režimy a jedinečné zážitky.
    





5. **Podpora vlastního obsahu:** Engine Quake 3 podporoval vlastní obsah, včetně textur, modelů a zvukových souborů, což umožňovalo vysoký stupeň přizpůsobení v uživatelsky vytvořených mapách a modech.
    





6. **Design úrovní:** Modul používal systém navrhování úrovní založený na kartáčích, kde byly mapy konstruovány vyřezáváním prostor z pevných kartáčů. Tento přístup byl dobře zdokumentovaný a uživatelsky přívětivý pro návrháře úrovní.


V průběhu let byl Quake 3 engine používán jako základ pro mnoho dalších her a modů, včetně „Return to Castle Wolfenstein“, „Star Wars Jedi Knight II: Jedi Outcast“ a „Urban Terror“ mimo jiné. Zanechalo trvalé dědictví ve světě vývoje her a pomohlo formovat žánr stříleček z pohledu první osoby. Zatímco se od té doby objevily novější a pokročilejší motory, engine Quake 3 je nadále respektován pro svůj přínos hernímu průmyslu.

## Jak otevřít soubor SHADER?

Mezi programy, které otevírají nebo odkazují na soubory SHADER, patří

- **id Software Quake 3** (placený) pro (Windows, Mac, Linux)
- Microsoft Poznámkový blok
- Poznámkový blok++
- Jakýkoli textový editor

## Další soubory SHADER

Zde jsou další typy souborů, které používají příponu souboru **.shader**.

**Herní soubory**
- [SHADER - Godot Engine Shader File](/cs/hra/shader-godot/)
- [SHADER - Quake 3 Engine Shader File](/cs/hra/shader-quake/)
- [SHADER - Unity Shader Asset](/cs/hra/shader-unity/)

## Reference
- [id Tech 3](https://en.wikipedia.org/wiki/Id_Tech_3)

