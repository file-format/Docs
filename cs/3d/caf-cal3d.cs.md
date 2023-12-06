{
"date":"2023-01-04",
   "keywords":[
"kavárna",
"soubor caf",
"soubor binární animace caf cal3d",
"jak otevřít soubor caf",
"soubor",
"přípona souboru caf",
"rozšíření",
"soubor"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"Formát souboru CAF - soubor binární animace Cal3D",
   "description":"Další informace o formátu CAF Cal3D Binary Animation File a rozhraních API, která mohou vytvářet a otevírat soubory CAF.",
"linktitle":"CAF Cal3D",
   "menu":{
      "docs":{
         "identifier":"3d-caf-cal3d",
         "parent":"3d"
}
},
"lastmod":"2023-01-04"
}

## Co je soubor CAF?

Soubor .CAF obvykle odkazuje na **"Cal3D Binary Animation File."** Cal3D je open-source knihovna 3D animací postav často používaná při vývoji videoher a dalších interaktivních 3D aplikací. Tyto soubory ".caf" jsou speciálně navrženy pro ukládání binárních animačních dat pro postavy nebo objekty vytvořené pomocí rámce Cal3D.

Soubory CAF hrají klíčovou roli při předávání realistických lidských pohybů postavám. Definují animace pro různé akce, jako je chůze, běh nebo jiné dynamické akce, které postava může provádět. Animace Cal3D mohou být také reprezentovány ve formátu [XML](/cs/web/xml/) pomocí souborů s příponou ".xaf". Tato reprezentace XML poskytuje alternativní způsob ukládání a manipulace s daty animace v Cal3D.

## Binární animační soubor Cal3D

Zde je několik informací o tom, co můžete najít v souboru binární animace Cal3D:

1. **Data animací:** Soubory .caf primárně obsahují data animací, jako jsou animace koster, klíčové snímky, transformace kostí a další informace související s animacemi postav nebo objektů.

2. **Informace o kostře:** Animace Cal3D jsou obvykle založeny na hierarchii koster, kde se k deformaci sítě postavy používají kosti. Soubor .caf uchovává informace o hierarchii kostí a transformacích pro každý klíčový snímek.

3. **Klíčové snímky:** Animace v Cal3D je obvykle uložena jako série klíčových snímků. Soubor .caf bude obsahovat data pro každý klíčový snímek, včetně pozic a orientací kostí v těchto klíčových snímcích.

4. **Blend Weights and Poses:** V pokročilejších animacích mohou soubory .caf obsahovat také informace o prolnutí různých animací dohromady a definování různých pozic pro postavy.

5. **Komprese:** Aby se zmenšila velikost souboru a optimalizoval výkon, mohou soubory .caf využívat kompresní techniky k efektivnímu ukládání dat animace.

## Jak otevřít soubor CAF?

Programy, které otevírají nebo odkazují na soubory CAF

- **Cal3dViewer** (zdarma) pro Windows
- **Cal3D** (zdarma) pro Linux

**Podtyp:** Soubory 3D obrázků

## Další soubory CAF

Zde jsou další typy souborů, které používají příponu souboru **.caf**.

**3D a zvuk**
- [CAF - Cal3D Binary Animation File](/cs/3d/caf-cal3d/)
- [CAF - Core Audio File](/cs/audio/caf/)

**Databáze a programování**
- [CAF - Cathy Catalog File Format](/cs/database/caf/)
- [CAF - CryENGINE Character Animation File](/cs/programming/caf-cryengine/)

## Reference
* [CAL3D](https://github.com/mp3butcher/Cal3D)

