{
  "date" : "2019-12-03",
  "keywords" :[ "doc", "soubor", "přípona", "formát souboru", "Word", "Dokument" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOC - soubor dokumentu Microsoft Word",
  "description":"Další informace o formátu souboru DOC a rozhraních API, která mohou vytvářet a otevírat soubory DOC.",
  "linktitle" : "DOC",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## Co je soubor DOC?

Soubory s příponou .doc představují dokumenty generované aplikací Microsoft Word nebo jinými dokumenty pro zpracování textu v binárním formátu souboru. Rozšíření bylo původně používáno pro dokumentaci ve formátu prostého textu na několika různých operačních systémech. Může obsahovat několik různých typů dat, jako jsou obrázky, formátované i prostý text, grafy, tabulky, vložené objekty, odkazy, stránky, formátování stránky, nastavení tisku a mnoho dalších. Formát byl oblíbený pro všechny druhy dokumentace kvůli rozmanitosti možností, které uživatelům nabízí pro psaní manuálů, návrhů, specifikací, životopisů, článků nebo jakýchkoli podobných dokumentů. Aktualizovaná verze DOC je [DOCX](/cs/word-processing/docx/), která je založena na Office OpenXML, jehož specifikace jsou volně dostupné.

## Stručná historie ##

WordPerfect, produkt společnosti [Corel](https://www.corel.com/en/), používal DOC jako rozšíření svého proprietárního formátu. V 80. letech zůstal WordPerfect volbou použití na většině počítačů díky své snadné dostupnosti, shodě s většinou počítačových strojů a operačních systémů. WordPerfect však zaznamenal svůj pád na operačním systému Windows, když Microsoft představil Microsoft Word jako svůj produkt pro formát souborů dokumentů a pro svůj proprietární formát zvolil příponu DOC. Jak se Microsoft Word stal stále populárnějším, formát souboru DOC prošel několika revizemi z Microsoft Word 97 - 2003. V roce 2007 byl výchozí formát souboru DOC nahrazen formátem Office Open XML (známým jako DOCX) a novými verzemi Microsoft Word nyní používá toto nové rozšíření jako výchozí formát souboru.

## Specifikace formátu souboru DOC – Další informace

Microsoft neuvolnil specifikace formátu souborů DOC po dlouhou dobu až do roku 2008. V únoru 2008 byly vydány specifikace formátu pro formát souboru .doc v rámci Microsoft Open Specification Promise. Ačkoli specifikace nepopisuje všechny funkce používané formátem DOC, poskytuje dostatek informací o znalostech potřebných pro práci s tímto formátem souboru. K využití dostupných informací je však nutné reverzní inženýrství. Specifikace byly několikrát aktualizovány a nejnovější [revize](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx) je 8.0, která byla aktualizována v srpnu 2018 .

### Některé základní pojmy ###

Než se pustíme do podrobností o specifikacích formátu souboru pro DOC, je nutné pochopit některé základní pojmy, abychom mohli s tímto formátem souboru pracovat.

**File Information Base (Fib):** Struktura Fib obsahuje informace o dokumentu a určuje ukazatele souborů na různé části, které tvoří dokument.
Fib je struktura s proměnnou délkou. S výjimkou základní části, jejíž velikost je pevná, před každou částí je uvedeno pole počtu, které určuje velikost další části.

**Pozice znaku:** CP nebo Pozice znaku představuje 32bitové celé číslo bez znaménka, které slouží jako index znaku v textu dokumentu od nuly. Umístění a velikost každého znaku v souboru nelze získat přímo a je třeba je vypočítat pomocí předem určeného algoritmu. Mezi postavy patří:

* Text dokumentu
* Kotvy objektů, jako jsou poznámky pod čarou nebo textová pole
* Řídicí znaky, jako jsou značky odstavců a značky buněk tabulky

**PLC:** Struktura PLC je pole CP následované polem datových prvků. Datové prvky pro jakékoli PLC musí mít stejnou velikost nula nebo více bajtů, a z tohoto důvodu musí být počet CP o jeden větší než počet datových prvků. Struktury PLC jsou různých typů, kde každý typ určuje, zda jsou pro daný typ povoleny duplicitní CP nebo ne. Struktura PLC se skládá z:

* **aCP (proměnná délka):** Pole prvků CP. Každý typ struktury **PLC** specifikuje význam prvků CP a povolený rozsah.
* **aData (proměnná délka):** Každý typ struktury **PLC** specifikuje strukturu a význam datových prvků, veškerá omezení počtu datových prvků a veškerá omezení dat v nich obsažených. Také specifikuje vztah mezi datovými prvky a odpovídajícími CP.

**Platný výběr:** Konstrukce souboru .DOC jsou popsány hlavně řadou CP. Existuje řada [pravidel](https://msdn.microsoft.com/en-us/library/dd908861(v#office.12).aspx) specifikovaných společností Microsoft, která je třeba v takovém případě dodržovat.

**STTB:** STTB je řetězcová tabulka, která se skládá z hlavičky, za kterou následuje pole prvků. Hodnota **cData** určuje počet prvků, které jsou obsaženy v poli.

**Ukládání vlastností:** Soubor aplikace Word může mít různé prvky, jako je text, odstavce, tabulky, obrázky a sekce, kde každý může mít své vlastní vlastnosti. Jejich vlastnosti jsou uloženy v souboru aplikace Word jako rozdíly oproti výchozímu nastavení. Takové rozdíly jsou specifikovány PRl, který se skládá z Single Property Modifier (Sprm) a jeho operandu. Aplikace může určit konečnou sadu vlastností aplikací seznamů **Prl**.

**Ochrana heslem:** Soubory aplikace Word mohou být chráněny také heslem, k čemuž lze použít jeden z následujících mechanismů.

* XOR zmatek
* Šifrování binárních dokumentů Office RC4
* Šifrování binárního dokumentu RC4 CryptoAPI

Pokud jsou FibBase.fEncrypted a FibBase.fObfuscation obě 1, soubor je zatemněn pomocí XOR obfuscation.

Pokud je FibBase.fEncrypted 1 a FibBase.fObfuscation je 0, soubor je zašifrován pomocí šifrování Office Binary Document RC4 Encryption nebo Office Binary Document RC4 CryptoAPI Encryption s EncryptionHeader uloženým v prvních FibBase.lKey bajtech proudu Table. EncryptionHeader.EncryptionVersionInfo určuje, který mechanismus šifrování byl použit k zašifrování souboru.

### Struktura souboru ###

Binární soubor Wordu je ve své originalitě složený soubor OLE, který se skládá z několika úložišť a proudů. Tato úložiště a streamy mají svou vlastní strukturu a velikosti, které určují parametry pro zápis a čtení. Tyto jsou:

#### Stream WordDocument ####

Tento proud obsahuje text dokumentu a další informace odkazované z jiných částí souboru. Tok nemá žádnou předdefinovanou strukturu kromě FIB na začátku, která je povinná a měla by mít offset 0. Tento tok nesmí být větší než 2147 MB.

#### 1TableStream nebo 0TableStream ####

Binární soubor aplikace Word může obsahovat toky tabulek známé jako 1Table stream nebo 0Table stream. Alespoň jeden z nich by měl být v dokumentu uveden. Pokud však dokument obsahuje proudy 1Table i 0Table, použije se pouze proud, na který odkazuje base.fWhichTblStm. Neodkazovaný stream MUSÍ být ignorován.
Proud tabulky NESMÍ být větší než 2147 MB.

#### Datový tok ####

Datový proud nemá žádnou předdefinovanou strukturu. Obsahuje data, na která se odkazuje z FIB nebo z jiných částí souboru. Tento proud nemusí být přítomen, pokud na něj nejsou žádné odkazy. Datový tok NESMÍ být větší než 2147 MB.

#### Úložiště fondu objektů ####

Úložiště fondu objektů obsahuje úložiště pro vložené objekty OLE. Toto úložiště nemusí být přítomno, pokud v dokumentu nejsou žádné vložené objekty OLE.

#### Vlastní úložiště dat XML ####

Vlastní úložiště dat XML je volitelné úložiště, jehož název MUSÍ být „MsoDataStore“.

#### Souhrnný informační stream ####

Datový proud souhrnných informací je volitelný proud, jehož název MUSÍ být "\005SummaryInformation", kde \005 je znak s hodnotou 0x0005, nikoli řetězcový literál "\005".

#### Souhrnný informační proud dokumentu ####

Proud souhrnných informací o dokumentu je volitelný proud, jehož název MUSÍ být "\005DocumentSummaryInformation", kde \005 je znak s hodnotou 0x0005, nikoli řetězcový literál "\005".

#### Šifrovací stream ####

Stream Encryption je volitelný stream, jehož název MUSÍ být „šifrování“. Tento stream NESMÍ být přítomen, pokud nejsou splněny obě následující podmínky:

* Dokument je zašifrován pomocí šifrování Office Binary Document RC4 CryptoAPI Encryption.
* Hodnota fDocProps se nastavuje v EncryptionHeader.Flags.

#### Úložiště maker ####

Úložiště maker je volitelné úložiště, které obsahuje makra pro daný soubor. Pokud existuje, MUSÍ to být kořenové úložiště projektu.

#### Úložiště podpisů XML ####

Úložiště podpisů XML je volitelné úložiště, jehož název MUSÍ být "_xmlsignatures".

#### Stream podpisů ####

Tok podpisů je volitelný tok, jehož název MUSÍ být "_signatures". Tento stream obsahuje digitální podpisy.

#### Správa práv k informacím Úložiště datového prostoru ####

Úložiště datového prostoru Information Rights Management je volitelné úložiště, jehož název MUSÍ být "\006DataSpaces", kde \006 je znak s hodnotou 0x0006, a nikoli řetězcový literál "\006". Pokud je toto úložiště přítomno, MUSÍ být přítomen také stream chráněného obsahu.
Je-li toto úložiště přítomno, všechny specifikované toky a úložiště kromě tohoto úložiště a toku chráněného obsahu BY MĚLY být načteny z toku chráněného obsahu, jak je uvedeno v [MS-OFFCRYPTO] a pokud některý z těchto toků a úložišť existuje mimo chráněný obsah. Stream, MĚLI bychom je ignorovat.

#### Stream chráněného obsahu ####

Proud chráněného obsahu je volitelný datový proud, jehož název MUSÍ být "\009DRMContent", kde \009 je znak s hodnotou 0x0009, nikoli řetězcový doslov "\009".
Pokud je tento proud přítomen, MUSÍ být přítomno také úložiště datového prostoru správy informačních práv.

## Reference ##

* [Specifikace vytváření souborů MS-DOC](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx)
* [Doc Computing](https://en.wikipedia.org/wiki/Doc_(computing))

