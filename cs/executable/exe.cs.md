{
  "date" : "2021-06-30",
  "keywords" :[ "soubor exe", "formát souboru exe", "co je soubor exe", "soubor", "příklad exe", "přípona souboru exe", "přípona", "formát" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Soubor .exe je spustitelný soubor společnosti Microsoft, který je spuštěn v operačním systému Windows. Další informace o formátu souboru EXE.",
  "title" :"Co je spustitelný soubor EXE?",
  "linktitle" : "EXE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Co je soubor EXE?

Slovo EXE je zkratka pro **executable**. Soubor .exe je program, který lze spustit v operačním systému Microsoft Windows. Vývojáři aplikací většinou publikují své programy pro OS Windows ve spustitelném formátu jako soubory exe. Je to standardní formát souboru pro spouštění aplikací v systému Windows. **Setup.exe**, **Install.exe** a **cmd.exe** jsou některé běžné a dobře známé názvy souborů EXE.

## Formát souboru EXE

Kompilátory MS-DOS byly zavedeny s modely paměti s omezením paměti 64 kB. Obecnou koncepcí je nastavení různých segmentových registrů v x86 CPU (CS, DS, ES, SS) tak, aby ukazovaly na různé nebo stejné segmenty, a proto umožňují různé stupně přístupu k paměti. Některé konkrétní modely paměti byly:

- **Tiny**: Všechny přístupy do paměti jsou 16bitové (registry segmentů se nezměnily). Vytvoří soubor .COM namísto souboru .EXE.
- **Small**: Všechny přístupy do paměti jsou 16bitové (registry segmentů se nezměnily).
- **Kompaktní**: Datové adresy zahrnují segment i offset, při přístupu se znovu načítají registry DS nebo ES a umožňují až 1 milion dat. Přístupy ke kódu nemění registr CS, což umožňuje 64 kB kódu.
- **Střední**: Kódové adresy zahrnují adresu segmentu, opětovné načtení CS při přístupu a umožňující až 1 milion kódu. Přístupy k datům nemění registry DS a ES, což umožňuje 64K dat.
- **Velké**: Kódové i datové adresy jsou páry (segment, offset), vždy znovu načítají adresy segmentů. Celý 1M byte paměti je k dispozici pro kód i data.
- **Obrovský**: Stejné jako u velkého modelu, kompilátor generuje další aritmetiku, která umožňuje přístup k polím větším než 64 kB.

Vývojáři se musí rozhodnout, který model by měl být vybrán při vytváření exe souboru.

### Přenosný formát souboru EXE

Portable executable file format (PE) obsahuje řadu informačních záhlaví, následující je seznam záhlaví:

- **Záhlaví DOS**: Záhlaví systému MS-DOS zajišťuje buď zpětnou kompatibilitu, nebo plynulý pokles nových typů souborů.
- **PE Header**: V offsetu 60 (0x3C) od začátku DOS hlavičky je ukazatel na hlavičku PE File
- **COFF Header**: Hlavička COFF obsahuje některé informace, které jsou užitečné pro spustitelný soubor, a některé informace, které jsou užitečnější pro soubor objektu.
- **Volitelné záhlaví PE**: Volitelné záhlaví PE se vyskytuje přímo za záhlavím COFF a některé zdroje dokonce zobrazují dvě záhlaví jako součást stejné struktury.
- **Tabulka sekcí**: Bezprostředně za volitelným záhlavím PE najdeme tabulku sekcí. Tabulka sekcí se skládá z pole struktur IMAGE_SECTION_HEADER.
- **Mapovatelné sekce**: Může ušetřit místo v paměti mapováním kódu knihovny do více než jednoho procesu.

## Můžete spustit soubor EXE na počítači Mac?

Soubory EXE se v systému Mac OS nepoužívají jako spustitelné soubory. Pokud však chcete spustit soubor exe v systému Mac OS, můžete použít následující metody.

1. **Wine** – Wine je perfektní řešení pro lidi, kteří chtějí používat své PC aplikace na systémech Mac. Je to zkratka, která znamená „Wine Is Not A Emulator“. Wine vytváří stejné prostředí adresářů, jaké používá Microsoft, takže pomocí něj můžete spouštět aplikace pro Windows.
2. **Virtuální stroje** – Vytvořte virtuální stroj Windows pomocí Parallel Desktop nebo VM Virtual Box a spusťte svou aplikaci uvnitř virtuálního stroje.
3. **Boot Camp** – Instalace a konfigurace Windows Boot Camp na Mac OS vám umožní spustit operační systém Windows na počítači Mac.

## Reference

* [.exe- od Wikipewdia](https://en.wikipedia.org/wiki/.exe)
* [x86 Disassembly/Windows Executable Files](https://en.wikibooks.org/wiki/X86_Disassembly/Windows_Executable_Files#MS-DOS_EXE_Files)

