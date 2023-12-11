{
"datum": "24.05.2023",
  "keywords": [
"soubor cba",
"co je soubor cba",
"jak vytvořit soubor CBA",
"co obsahuje soubor CBA",
"jaký je formát souboru cba",
"soubor",
"přípona souboru cba",
"rozšíření"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formát souboru CBA - Archiv komiksů",
  "description":"Další informace o formátu CBA a rozhraních API, která mohou vytvářet a otevírat soubory CBA.",
  "linktitle": "CBA",
  "menu": {
    "docs": {
      "identifier": "compression-cba",
      "parent": "compression"
}
},
"lastmod": "24.05.2023"
}

## Co je soubor CBA?

Soubor Comic Book Archive (CBA), také známý jako Comic Book Archive nebo Comic Book Reader soubor, je populární formát používaný k ukládání a distribuci digitálních komiksů. Obvykle obsahuje sbírku jednotlivých stránek komiksu nebo obrázků spojených do jednoho souboru pro snadnou organizaci a čtení.

Jedním z běžných formátů pro vytváření souborů Comic Book Archive je formát TAR (Tape Archive). TAR je formát archivace souborů používaný v prostředí Unix a Linux. Kombinuje více souborů do jednoho souboru, který se často používá pro účely zálohování.

## Jak vytvořit soubor CBA?

Chcete-li vytvořit soubor Comic Book Archive pomocí nástroje archivace TAR, obvykle byste měli postupovat takto:

1. Shromážděte všechny stránky komiksu nebo obrázky, které chcete zahrnout do archivu.
2. Otevřete příkazový řádek nebo okno terminálu.
3. Přejděte do adresáře, kde jsou umístěny stránky/obrázky komiksu.
4. K vytvoření archivu použijte příkaz TAR s příslušnými volbami. Příkaz může vypadat například takto:

```
tar -cf comicbook.cbt page1.jpg page2.jpg page3.jpg
```

V tomto příkladu volba -c říká TAR, aby vytvořil nový archiv, a volba -f určuje název výstupního souboru (v tomto případě comicbook.cbt). Po zadání možností zadáte názvy souborů, které chcete zahrnout do archivu (strana1.jpg, strana2.jpg, strana3.jpg).

5. Po provedení příkazu nástroj TAR vytvoří soubor Comic Book Archive (v tomto příkladu comicbook.cbt) v aktuálním adresáři.

Jakmile budete mít soubor Comic Book Archive, můžete použít různé programy nebo aplikace pro čtení komiksů k otevření a čtení komiksů na vašem počítači nebo zařízení. Tyto aplikace obvykle poskytují funkce, jako je navigace po stránkách, zoomování a přidávání záložek, které zlepšují zážitek ze čtení.

## Co obsahuje soubor CBA?

Soubor Comic Book Archive (CBA) vytvořený pomocí archivačního nástroje TAR obsahuje kolekci jednotlivých stránek komiksu nebo obrázků sdružených do jednoho souboru. Konkrétní obsah archivu závisí na zabalené komiksové knize.

Soubor Comic Book Archive obvykle obsahuje následující:

- **Stránky komiksu:** Hlavním obsahem archivu jsou samotné stránky komiksu. Tyto stránky se obvykle ukládají jako jednotlivé obrazové soubory, například JPEG nebo PNG, které představují každou stránku komiksu. Stránky jsou uspořádány ve specifickém pořadí, aby byl zachován narativní tok komiksu.
- **Metadata:** Některé formáty archivu komiksů mohou obsahovat metadata o komiksu, jako je název, autor, vydavatel, datum vydání a popis. Tyto informace pomáhají identifikovat a kategorizovat komiks.
- **Další soubory:** Kromě stránek komiksu a metadat může archiv obsahovat další doplňkové soubory související s komiksem. Tyto soubory mohou zahrnovat přebal, propagační obrázky, bonusový obsah nebo textové soubory poskytující dodatečné informace nebo komentáře.

## Jaký je formát souboru CBA?

Formát souboru Comic Book Archive (CBA) vytvořený pomocí nástroje archivace TAR je obvykle ve formátu TAR. TAR, zkratka pro Tape Archive, je formát archivace souborů běžně používaný v systémech Unix a Linux. Není to specifické pro komiksy, ale je to univerzální archivační formát.

Formát TAR je přímočarý způsob, jak spojit více souborů do jednoho archivního souboru. Samo o sobě neposkytuje kompresi, takže výsledný soubor TAR může být ve srovnání s jinými komprimovanými formáty jako ZIP nebo RAR velký. Soubory TAR však lze komprimovat pomocí dalších nástrojů nebo kombinovat s kompresními algoritmy, jako je gzip nebo bzip2, aby se zmenšila velikost souboru.

Formát TAR zachovává strukturu souborů, oprávnění k souborům a časová razítka zahrnutých souborů. Ukládá soubory postupně v rámci archivu, což umožňuje snadnou extrakci jednotlivých souborů nebo celého archivu.

## Reference
* [Archiv komiksů](https://en.wikipedia.org/wiki/archiv_komiksů)

