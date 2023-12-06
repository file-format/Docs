{
"datum": "2023-05-31",
  "keywords": [
"soubor na ploše",
"co je soubor na ploše",
"co obsahuje soubor plochy",
"ukázkový soubor plochy",
"jak otevřít soubor na ploše",
"jaký je formát souboru plochy",
"soubor",
"přípona souboru na ploše",
"rozšíření"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formát souboru DESKTOP – vstupní soubor plochy",
  "description":"Další informace o formátu DESKTOP a rozhraních API, která mohou vytvářet a otevírat soubory DESKTOP.",
"linktitle": "DESKTOP",
  "menu": {
    "docs": {
      "identifier": "settings-desktop",
      "parent": "settings"
}
},
"lastmod": "2023-05-31"
}

## Co je soubor DESKTOP?

Soubor .desktop je konfigurační soubor používaný desktopovými prostředími Linuxu k definování zástupců aplikací a spouštěčů. Poskytuje metadata o aplikaci, jako je její název, ikona, příkaz k provedení a další vlastnosti. Tyto soubory se obvykle používají k vytváření zástupců v nabídkách aplikací, spouštěcích plochách nebo panelech v systémech založených na Linuxu.

## Co obsahuje soubor DESKTOP?

Soubor .desktop má specifický formát a obsahuje několik klíčových polí:

- **[Desktop Entry]:** Toto je hlavička hlavní sekce pro soubor .desktop.
- **Name:** Určuje název aplikace.
- **Komentář:** Poskytuje stručný popis nebo komentář k aplikaci.
- **Exec:** Definuje příkaz, který se má provést při spouštění aplikace.
- **Ikona:** Určuje cestu k souboru ikony spojenému s aplikací.
- **Terminál:** Určuje, zda se má aplikace spouštět v okně terminálu.
- **Typ:** Určuje typ položky, například "Aplikace" nebo "Odkaz."
- **Kategorie:** Určuje kategorie nebo skupiny, pod kterými se má aplikace zobrazit v nabídce.
- **StartupNotify:** Určuje, zda by prostředí plochy mělo zobrazovat oznámení o spuštění aplikace.
- **NoDisplay:** Určuje, zda má být aplikace skryta v nabídkách.
- **Akce:** Definuje další akce, které lze v aplikaci provést, jako je otevření konkrétního souboru.

## Příklad souboru DESKTOP

Zde je příklad souboru .desktop pro fiktivní textový editor s názvem "MyTextEditor":

```
[Desktop Entry]
Name=MyTextEditor
Comment=A simple text editor
Exec=mytexteditor %F
Icon=/path/to/icon.png
Terminal=false
Type=Application
Categories=TextEditor;Utility;
StartupNotify=true
NoDisplay=false
Actions=OpenNewWindow;OpenExistingFile;

[Desktop Action OpenNewWindow]
Name=Open New Window
Exec=mytexteditor

[Desktop Action OpenExistingFile]
Name=Open Existing File
Exec=mytexteditor %U
```

V tomto příkladu soubor .desktop definuje aplikaci "MyTextEditor" s přidruženými vlastnostmi. Zahrnuje také dvě další akce, „Otevřít nové okno“ a „Otevřít existující soubor“, ke kterým lze přistupovat z kontextové nabídky spouštěče aplikací.

Umístěním souboru .desktop do konkrétních adresářů, jako je `/usr/share/applications` nebo `~/.local/share/applications`, ho desktopové prostředí rozpozná a podle toho zobrazí aplikaci v nabídkách nebo umožní její spuštění z plocha počítače.

## Jak otevřít soubor DESKTOP?

Soubory .desktop může otevřít a zpracovat několik softwarových programů. Tyto programy jsou obvykle správci souborů nebo desktopová prostředí v systémech založených na Linuxu. Zde jsou nějaké příklady:

- **Nautilus (Files):** Výchozí správce souborů pro desktopové prostředí GNOME.
- **Nemo:** Správce souborů pro desktopové prostředí Cinnamon.
- **Dolphin:** Výchozí správce souborů pro desktopové prostředí KDE Plasma.
- **Thunar:** Výchozí správce souborů pro desktopové prostředí Xfce.
- **Editor nabídky KDE:** Nástroj specifický pro prostředí KDE Plasma desktop, který umožňuje prohlížet a upravovat soubory .desktop.

Tito správci souborů a desktopová prostředí poskytují grafické rozhraní pro správu souborů .desktop. Umožňují prohlížet a upravovat vlastnosti souborů .desktop, vytvářet spouštěče aplikací a organizovat zástupce v nabídkách aplikací nebo na ploše.

Soubory .desktop jsou soubory ve formátu prostého textu, takže je můžete také otevřít a upravit pomocí libovolného textového editoru. Jednoduše klikněte pravým tlačítkem myši na soubor .desktop a vyberte "Otevřít pomocí" nebo "Otevřít pomocí jiné aplikace" a vyberte textový editor ze seznamu nainstalovaných programů.

## Jaký je formát souboru DESKTOP?

Formát souboru .desktop má specifickou strukturu a formát. Jedná se o prostý textový soubor se sadou párů klíč-hodnota uspořádaných do sekcí. Zde je přehled formátu:

- **Záhlaví sekcí:** Každá sekce začíná záhlavím uzavřeným v hranatých závorkách ([]). Primární sekce se obvykle jmenuje [Desktop Entry], která obsahuje hlavní metadata pro aplikaci nebo spouštěč.
- **Páry klíč–hodnota:** V každé sekci definujete vlastnosti pomocí párů klíč–hodnota. Formát je "Key=Value". Klíč identifikuje vlastnost a hodnota poskytuje odpovídající data.
- **Syntaxe vlastností:** Hodnoty vlastností mohou být různých typů včetně řetězců, booleovských hodnot, cest k souborům nebo seznamů. Formát pro každou hodnotu vlastnosti závisí na jejím typu.
- **Komentáře:** Do souboru .desktop můžete přidat komentáře pomocí symbolu '#'. Cokoli za '#' online je považováno za komentář a je ignorováno.

## Reference
* [Soubory vstupu na plochu](https://www.baeldung.com/linux/desktop-entry-files)

