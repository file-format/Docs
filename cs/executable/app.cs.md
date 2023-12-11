{
"datum": "2023-02-02",
  "keywords": [
"soubor aplikace",
"co je soubor aplikace",
"soubor",
"jak otevřít soubor aplikace",
"přípona souboru aplikace",
"rozšíření"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
  "description":"Další informace o formátu souboru APP a rozhraních API, která mohou vytvářet a otevírat soubory APP.",
"title": "Formát souboru APP – balíček aplikací macOS",
  "linktitle": "APP",
  "menu": {
    "docs": {
      "identifier": "executable-app",
      "parent": "executable"
}
},
"lastmod": "2023-02-02"
}

## Co je soubor APP?

Soubor .app v macOS je speciální typ adresáře, který obsahuje všechny soubory potřebné ke spuštění konkrétní aplikace, včetně spustitelného kódu, prostředků a metadat. Rozšíření .app signalizuje operačnímu systému, že s tímto adresářem by se mělo zacházet jako s jednou jednotkou, nikoli jako sbírkou samostatných souborů, a že jej lze spustit přímo z Finderu nebo Docku.

Finder je výchozí aplikace správce souborů v systému macOS. Umožňuje vám procházet a organizovat soubory a adresáře v počítači. Dock je funkce macOS, která poskytuje rychlý přístup k často používaným aplikacím a dokumentům. Finder i Dock umožňují spouštět aplikace kliknutím na jejich soubory .app, čímž se otevře příslušný balíček aplikací. Když spustíte aplikaci, spustí se spustitelný kód v rámci balíčku .app, čímž se aplikace zpřístupní k použití. Soubor .app představuje aplikaci v systému souborů a poskytuje uživateli způsob přístupu k aplikaci a její spuštění.

Když ve Finderu v systému macOS kliknete pravým tlačítkem na soubor .app a vyberete „Zobrazit obsah balíčku“, uvidíte vnitřní strukturu balíčku aplikací. To je užitečné, pokud chcete získat přístup k prostředkům nebo souborům používaným aplikací nebo pokud chcete zkontrolovat obsah aplikace pro účely odstraňování problémů. Obsah balíčku souboru .app obvykle zahrnuje adresáře zdrojů, jako jsou obrázky a zvuky, a také spustitelný kód aplikace. Prozkoumáním obsahu souboru .app můžete získat hlubší přehled o tom, jak je aplikace sestavena a co dělá.

## Jak otevřít soubor APP?

Chcete-li otevřít soubor .app v systému macOS, jednoduše na soubor ve Finderu dvakrát klikněte. Tím se spustí aplikace obsažená v balíčku .app. Pokud je aplikace nainstalována ve vašem systému a byla přidružena k typu souboru .app, poklepáním na soubor by se měla aplikace automaticky spustit. Pokud aplikace není přidružena k typu souboru .app, možná budete muset na soubor kliknout pravým tlačítkem myši a vybrat možnost „Otevřít v programu“ a vybrat vhodnou aplikaci, kterou chcete otevřít.

Soubor .app můžete otevřít v Terminálu v macOS pomocí příkazu „open“. Chcete-li to provést, přejděte do adresáře, kde je umístěn soubor .app, pomocí příkazu „cd“ a poté spusťte následující příkaz:

```
open <AppName>.app 
```

kde<AppName> je název aplikace, kterou chcete spustit. Tím se aplikace spustí, jako byste na ni dvakrát klikli ve Finderu. Příkaz "open" je univerzální nástroj, který lze použít k otevření mnoha různých typů souborů, včetně aplikací, dokumentů a adresářů. Když u souboru .app použijete příkaz „otevřít“, spustí se aplikace obsažená v balíčku.

## Reference
* [Bundle (macOS)](https://en.wikipedia.org/wiki/Bundle_(macOS))
