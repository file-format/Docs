{
"date":"2023-10-11",
   "keywords":[
"chr",
"soubor chr",
"soubor znaků chr cryengine",
"jak otevřít soubor chr",
"soubor",
"přípona souboru chr",
"rozšíření",
"soubor"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"Formát souboru CHR - soubor znaků CryENGINE",
   "description":"Další informace o formátu souboru CHR CryENGINE Character a rozhraních API, která mohou vytvářet a otevírat soubory CHR.",
   "linktitle":"CHR CryENGINE",
   "menu":{
      "docs":{
         "identifier":"3d-chr-cryengine",
         "parent":"3d"
}
},
"lastmod":"2023-10-11"
}

## Co je soubor CHR?

Soubor CHR v kontextu CryENGINE odkazuje na **CryENGINE Character File**. CryENGINE je herní engine vyvinutý společností Crytek a tyto soubory se používají pro ukládání modelů postav a souvisejících dat pro použití ve videohrách a dalších aplikacích v reálném čase.

## Soubor znaků CryENGINE

Znakový soubor CryENGINE obvykle obsahuje následující součásti:

1. **Model postavy**: Toto je 3D model postavy, včetně její geometrie, textur a animací. Tyto modely jsou často vytvářeny pomocí softwaru jako Autodesk Maya nebo Blender a poté importovány do CryENGINE.
    




















2. **Data animací**: CryENGINE podporuje složité animace postav, takže soubor ".chr" může obsahovat různé animace, jako je chůze, běh, skákání a další. Tyto animace jsou obvykle uloženy jako data klíčových snímků.
    




















3. **Informace o riggingu**: Manipulace se týká procesu vytváření struktury kostry pro model postavy, což umožňuje použití animací na model. Soubor ".chr" může obsahovat informace o hierarchii kostí a jak je síť postavy spojena s touto kostrou.
    




















4. **Materiálové a texturové údaje**: Informace o materiálech použitých na modelu postavy a souvisejících mapách textur mohou být zahrnuty v souboru „.chr“. CryENGINE podporuje fyzikálně založené vykreslování, takže tyto materiály mohou být poměrně podrobné.
    




















5. **Fyzikální data**: Pokud je postava určena k interakci s herním světem, soubor „.chr“ může obsahovat fyzikální data, jako jsou tvary kolize nebo omezení pro fyziku ragdoll.
    




















6. **Nastavení konfigurace**: Součástí souboru „.chr“ mohou být také různá nastavení konfigurace související s chováním postavy v herním světě, jako je chování AI nebo skriptované události.

## CryENGINE

CryENGINE je výkonný herní engine vyvinutý společností Crytek, německou videoherní společností. Je známý svými špičkovými grafickými schopnostmi a byl použit k vytvoření některých vizuálně úžasných a technologicky vyspělých videoher. Zde jsou některé klíčové funkce a informace o CryENGINE:

1. **Grafika a vykreslování**: CryENGINE je známý svými pokročilými grafickými schopnostmi. Podporuje funkce jako globální osvětlení v reálném čase, vysoce kvalitní dynamické osvětlení a stíny, fyzikálně založené vykreslování (PBR) a textury s vysokým rozlišením. Tyto funkce přispívají k vytváření vizuálně ohromujících a realistických herních světů.
    




















2. **Fyzikální engine**: CryENGINE obsahuje vestavěný fyzikální engine, který umožňuje realistické interakce mezi objekty v herním světě. Podporuje funkce jako fyzika tuhého těla, fyzika měkkého těla a fyzika ragdoll, takže je vhodný pro vytváření dynamických a pohlcujících prostředí.
    




















3. **Terén a vegetace**: CryENGINE poskytuje nástroje pro vytváření rozsáhlých a detailních venkovních prostředí. Podporuje úpravy terénu, umístění vegetace a dynamické systémy počasí, což umožňuje vývojářům vytvářet rozsáhlé a realistické venkovní prostředí.
    




















4. ** Animace postav**: CryENGINE obsahuje robustní nástroje pro animaci postav. Podporuje komplexní sestavy postav, animaci obličeje a systém prolínání stromů, který umožňuje vývojářům vytvářet realistické pohyby a animace postav.
    




















5. **Systém umělé inteligence**: Engine obsahuje systém umělé inteligence, který umožňuje vytvářet inteligentní NPC (nehráčské postavy) a nepřátelskou umělou inteligenci. Vývojáři mohou skriptovat chování a interakce umělé inteligence, aby vytvořili náročné a pohlcující herní zážitky.
       





















6. **Skriptování**: CryENGINE používá skriptovací jazyk zvaný „Schematyc“, který umožňuje vývojářům vytvářet herní logiku a interakce. Navíc podporuje C++ pro pokročilejší programovací potřeby.

## Formáty souborů používané CryENGINE

Zde jsou některé z běžných typů souborů spojených s CryENGINE:

1. **cryproj**: Projektové soubory CryENGINE. Tyto soubory ukládají projektová nastavení a konfigurace pro konkrétní herní projekt.
    




















2. **.úroveň**: Soubory úrovní obsahují data 3D herního světa, včetně terénu, objektů, osvětlení a dalších nastavení specifických pro úroveň. Úrovně jsou základní součástí herního designu v CryENGINE.
    




















3. **.cgf**: Formát geometrie znaků. Tyto soubory obsahují data 3D modelu pro postavy, předměty a další herní prostředky. Soubory CGF mohou obsahovat geometrii, textury a data animací.
    




















4. **.chrparams**: Soubory parametrů znaků. Tyto soubory ukládají nastavení a konfigurace pro modely postav a jejich animace.
    




















5. **.dds**: Formát textury DirectX. CryENGINE běžně používá soubory DDS k ukládání textur, včetně difuzních map, normálních map a dalších typů textur.
    




















6. **.cryshader**: Soubory CryENGINE Shader. Tyto soubory definují, jak se vykreslují materiály a objekty v herním světě, určují shadery, vlastnosti materiálů a další.
    




















7. **.crytif**: Soubor informací o texturách. Tyto soubory ukládají další informace o texturách, jako je nastavení komprese, mipmapy a další detaily související s texturou.
    




















8. **.cdf**: Soubor definice znaků. Soubory CDF se používají k definování znakových prostředků a jejich vlastností, včetně příloh, stavů animací a nastavení souvisejících se znaky.
    




















9. **.dds**: CryENGINE také používá soubory DDS (DirectDraw Surface) pro různé texturové mapy, jako jsou normální mapy, zrcadlové mapy a difuzní mapy.
    




















10. **.anim**: Soubory animací. Tyto soubory ukládají data animací pro postavy a objekty, včetně klíčových snímků, pozic kostí a sekvencí animace.
    




















11. **.xml**: Soubory XML lze použít pro různé konfigurace a definice dat v rámci CryENGINE, jako je herní logika, chování AI a další.
    




















12. **.pak**: [soubory PAK](/cs/game/pak/) jsou archivní soubory používané k balení herních prostředků a zdrojů, což zefektivňuje distribuci a načítání her.

## Jak otevřít soubor CHR?

Programy, které otevírají soubory CHR, zahrnují

- **Crytek CryENGINE SDK** (bezplatná zkušební verze) pro Windows

**Podtyp:** Soubory 3D obrázků

## Další soubory CHR

Zde jsou další typy souborů, které používají příponu souboru **.chr**.

**3D**
- [CHR - soubor znaků CryENGINE](/cs/3d/chr-cryengine/)
- [CHR - 3ds Max Characters File](/cs/3d/chr-3ds/)

**Písmo a hra**
- [CHR - Borland Character Set](/cs/font/chr/)
- [CHR - Klub literatury Doki Doki! Soubor postavy](/cs/game/chr-doki/)

## Reference
- [CryEngine](https://en.wikipedia.org/wiki/CryEngine)

