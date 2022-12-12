{
  "date" : "2021-06-24",
  "keywords": [ "GADGET file", "what is a gadget file", "extension", "format", "what is a GADGET file", "archive" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Další informace o formátu souboru GADGET a rozhraních API, která mohou vytvářet a otevírat soubory GADGET.",
  "title" :"GADGET - soubor virtuálního CD",
  "linktitle" : "GADGET",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-06-24"
}

## Co je soubor GADGET?

Soubor GADGET se skládá z malého softwarového programu, který se spouští v postranním panelu Windows Vista nebo Windows 7. Komprimuje několik webových souborů a soubory mohou obsahovat soubory [.html](/cs/web/html), [.css](/cs/web/css) nebo [.js](/cs/web/js) a také další webové soubory. Soubory GADGET se používají pro malé součásti, jako jsou vyhledávací nástroje, informační kanály, systémové nástroje a malé hry. Ačkoli jsou GADGETy hostovány postranním panelem, nejsou specifické pro oblast postranního panelu; tyto lze odpojit a přesunout na plochu podle potřeby.

## Formát souboru GADGET

Soubor GADGET je přejmenovaný archiv [ZIP](/cs/compression/zip) obsahující kolekci souborů HTML, XML, JScript a CSS (Cascading Style Sheets). Instalace obsahuje stažení souboru .gadget a umožnění procesu stahování pro instalaci komponenty nebo uložení souboru .gadget do místního systému a poklepáním zahájíte proces instalace.

GADGET v zásadě obsahuje dva soubory:

1. **Gadget.xml**: Manifest, soubor XML obsahující obecnou prezentaci a informace o konfiguraci gadgetu.
2. **name.html**: Soubor HTML, ve kterém je název zadán v<name> tag přidruženého manifestu gadgetu, který poskytuje obal pro uživatelské rozhraní gadgetu a obsahuje základní funkce gadgetu.

Současně lze spustit více instancí souboru GADGET. Například, pokud někdo chce znát čas v různých časových pásmech, může spustit více instancí gadgetu hodin nastavením jednotlivých hodin na určité časové pásmo.

### Ukončení GADGET

Vzhledem k tomu, že platforma Windows Sidebar ve Windows 7 má vážné zranitelnosti, gadgety již nejsou k dispozici na oficiálních stránkách společnosti Microsoft. Později Microsoft tuto funkci v novějších verzích Windows vyřadil. GADGET by mohl být kdykoli zneužit k přístupu k souborům počítače, poškození počítače, odhalení závadného obsahu nebo změně jejich chování.

## Reference

* [Postranní panel Windows – od společnosti Microsoft](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/sidebar/-sidebar-entry)
* [Vývoj miniaplikace pro postranní panel Windows, část 1](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/sidebar/-sidebar-overview-gdo)

