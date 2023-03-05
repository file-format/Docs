{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PST - formát souboru úložiště osobních informací aplikace Outlook",
  "description":"Další informace o formátu souboru PST a rozhraních API, která mohou vytvářet a otevírat soubory PST.",
  "linktitle" : "PST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor PST?

Soubory s příponou PST představují soubory osobního úložiště aplikace Outlook (nazývané také tabulka osobních úložišť), které ukládají různé uživatelské informace. Uživatelské informace jsou uloženy ve složkách různých typů, které zahrnují e-maily, položky kalendáře, poznámky, kontakty a několik dalších formátů souborů. Soubory PST se používají k archivaci dat e-mailů offline, která lze později načíst a zobrazit v různých aplikacích.

## Specifikace formátu souboru PST

Formát souboru PST [specifikace](https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx) jsou k dispozici od společnosti Microsoft jako bezplatné a neodvolatelné bezplatné patentové licencování prostřednictvím Open Specification Promise .

### Typ formátů PST

Formáty souborů PST jsou rozděleny do dvou typů na základě kódování typu souboru. Soubory PST s kódováním ANSI jsou starší formáty souborů a jsou podporovány pouze aplikací Outlook 2002 a staršími verzemi. Takové soubory mají maximální limit velikosti 2 GB (2^^31^^ bajtů) a nepodporují Unicode. Modernější typ formátu souboru, založený na kódování Unicode, odstraňuje omezení velikosti souboru a může dosáhnout maximální velikosti dat 50 GB.

### Logická organizace formátu souborů PST

Základem souborového formátu PST je B-Strom, který uchovává data tříděná a umožňuje vyhledávání, sekvenční přístup, vkládání, mazání atd. v logaritmickém čase. Celková struktura souboru PST je organizována do tří vrstev.

![Logical layers of a PST file](/cs/email/PST-1.png "Logical layers of a PST file")

"Vrstva databáze uzlů (NDB)" - Vrstva databáze uzlů leží na nižší úrovni souboru PST a zahrnuje databázi uzlů. Tyto uzly ve skutečnosti představují úložná zařízení nižší úrovně formátu souborů PST. NDB vrstva se skládá z hlavičky, informací o alokaci souborů, bloků a BTrees (Node BTree a Block BTree) z hlediska úložiště. Uzly a bloky vrstvy NDB jsou propojeny pomocí Data BID, což je jedna ze čtyř vlastností reference Node, tj. NID (Node ID), Parent NID, Data BID (Block BID) a SubNode BID.

`Vrstva seznamů, tabulek a vlastností -` Vrstva LTP poskytuje logické pochopení pojmů vyšší úrovně nad rámec NDB. Kromě jiných prvků se vrstva LTP skládá hlavně z kontextu vlastností (PC) a kontextu tabulky (TC). PC je sbírka vlastností, zatímco TC představuje dvourozměrnou matici kolekce vlastností vs. přítomnost těchto vlastností. Efektivní implementace PC a TC, vrstva LTP používá následující dva typy datových struktur na vrcholu NDB Node:

* Heap On Node (HN) – umožňuje dílčí alokaci datového toku uzlu do malých fragmentů s proměnlivou velikostí.
* BTree on Heap (BTH) - BTH poskytuje pohodlný a praktický způsob prohledávání datových PC, popsané výše, jsou implementovány jako BTH, a proto je implementováno zabudováním do struktury HN.

`Vrstva zpráv -` V této vrstvě jsou implementována pravidla vyšší úrovně a obchodní logika pro práci se soubory PST. Logickým výstupem této vrstvy jsou objekty Folder, Message Objects, Attachment Objects a Properties, což je možné díky kombinaci vrstev LTP a NDB. V této vrstvě jsou také definována pravidla a požadavky, které je třeba dodržovat při úpravě obsahu PST.

### Fyzická organizace formátu souborů PST

Vysoká úroveň organizace souborů souboru PST je znázorněna na obrázku níže. Toto je pouze přehled různých konceptů z logických prvků souboru PST.

![Physical organization of the PST file format](/cs/email/PST-2.png "Physical organization of the PST file format")


#### Informace o záhlaví PST

Struktura HEADER souboru PST je umístěna na samém začátku souboru s offsetem 0. Obsahuje informace metadat o souboru PST a informace ROOT pro přístup k datovým strukturám vrstvy NDB popsaným výše. Struktura HEADER se liší pro verze Unicode a ANSI formátu souboru PST.

Záhlaví začíná 4bajtovým magickým slovem **!BDN** reprezentovaným byty (0x21, 0x42, 0x44, 0x4E). Další 2bajtové magické číslo, **SM** (0x53, 0x4D), je umístěno na offsetu 8 od začátku souboru. Informace o verzi (ANSI nebo Unicode) leží v offsetu 10 od začátku souboru. Hexadecimální hodnota (0x17) určuje soubor PST Unicode, zatímco 0x0E nebo 0x0F představuje formát souboru ANSI.

|Pole|Popis
---|---|
|dwMagic (4 bajty)|MUSÍ být "{ 0x21, 0x42, 0x44, 0x4E } ("!BDN")"
|dwCRCPartial (4 bajty)|32bitová hodnota CRC 471 bajtů dat počínaje wMagicClient (0ffset 0x0008)
|wMagicClient (2 bajty)|MUSÍ být "{ 0x53, 0x4D ".
|wVer (2 bajty)|Verze formátu souboru. Tato hodnota MUSÍ být 14 nebo 15, pokud je soubor souborem ANSI PST, a MUSÍ být 23, pokud je soubor souborem PST Unicode.
|wVerClient (2 bajty)|Verze formátu souboru klienta. Verze, která odpovídá formátu popsanému v tomto dokumentu, je 19. Tvůrci nového souboru PST založeného na tomto dokumentu BY MĚLI tuto hodnotu inicializovat na 19.
|bPlatformCreate (1 bajt)|Tato hodnota MUSÍ být nastavena na 0x01.
|bPlatformAccess (1 bajt)|Tato hodnota MUSÍ být nastavena na 0x01.
|dwReserved (8 bajtů)|
|bidUnused (pouze 8 bajtů Unicode)|Při vytvoření formátu souboru Unicode PST byla přidána nepoužitá výplň.
|bidNextP (Unicode: 8 bajtů; ANSI: 4 bajty)|BID na další stránku. Stránky mají speciální počítadlo pro přidělování hodnot bidIndex. Hodnota bidIndex pro BID pro stránky se přiděluje z tohoto čítače.
|bidNextB (pouze 4 bajty ANSI): |Další BID. Tato hodnota je monotónní čítač, který udává BID, který má být přiřazen dalšímu přidělenému bloku. Hodnoty BID se zvyšují v krocích po 4. Další podrobnosti naleznete v části 2.2.2.2.
|dwUnique (4 bajty)|Jedná se o monotónně rostoucí hodnotu, která se mění při každé změně struktury HEADER souboru PST. Funkcí této hodnoty je poskytnout jedinečnou hodnotu a zajistit, aby se CRC HEADER po každé úpravě záhlaví lišily.
|rgnid[](128 bajtů)|Pevné pole 32 NID, z nichž každý odpovídá jednomu z 32 možných typů NID_TYPE (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE,NID_TYPE_ASSOC_MESSAGE)
|qwUnused (8 bajtů)|Nepoužité místo; MUSÍ být nastaveno na nulu. Pouze souborový formát Unicode PST.
|kořen (Unicode: 72 bajtů; ANSI: 40 bajtů)|Struktura ROOT (část 2.2.2.5).
|dwAlign (4 bajty)|Nepoužité bajty zarovnání; MUSÍ být nastaveno na nulu. Pouze souborový formát Unicode PST.
|rgbFM (128 bajtů)|Zastaralá FMap. Toto se již nepoužívá a MUSÍ být vyplněno 0xFF. Čtenáři BY MĚLI ignorovat hodnotu těchto bajtů.
|rgbFP (128 bajtů)|Zastaralá FPmap. Toto se již nepoužívá a MUSÍ být vyplněno 0xFF. Čtenáři BY MĚLI ignorovat hodnotu těchto bajtů.
|bSentinel (1 bajt)|MUSÍ být nastaven na 0x80.
|bCryptMethod (1 byte)|Ukazuje, jak jsou data v souboru PST kódována. MUSÍ být nastavena na jednu z předdefinovaných hodnot (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC).
|rgbReserved (2 bajty)| Rezervováno; MUSÍ být nastaveno na nulu.
|bidNextB (8 bajtů)|Ukazuje další dostupnou hodnotu BID. Pouze souborový formát Unicode PST.
|bidNextB (POUZE Unicode: 8 bajtů)|Další BID. Tato hodnota je monotónní čítač, který udává BID, který má být přiřazen dalšímu přidělenému bloku. Hodnoty BID se zvyšují v krocích po 4. Další podrobnosti naleznete v části 2.2.2.2.
|dwCRCFull (4 bajty)|32bitová hodnota CRC 516 bajtů dat počínaje wMagicClient až bidNextB včetně. Pouze souborový formát Unicode PST.
|ullReserved (8 bajtů)|Rezervováno; MUSÍ být nastaveno na nulu. Pouze formát souboru ANSI PST.
|dwReserved (4 bajty)|Reserved; MUSÍ být nastaveno na nulu. Pouze formát souboru ANSI PST.
|rgbReserved2 (3 bajty)|
|bRezervováno (1 bajt) |
|rgbReserved3 (32 bajtů) |

### Ochrana dat ###

Z bezpečnostních důvodů mohou být soubory PST také chráněny heslem, což vyžaduje, aby načítací aplikace před zobrazením použila heslo. Heslo použité na soubor PST je uloženo v úložišti zpráv. To však neposkytuje silnou ochranu dat, protože heslo lze odstranit dostupnými nástroji. Uživatelem zadané heslo se také nepoužívá jako součást klíče pro kódování a dekódování šifrovacích algoritmů. Neexistuje tedy žádná výhoda z ochrany dat, ke kterým mají přístup neoprávněné strany. Uložení hesla jako CRC-32 hash původního řetězce z něj také dělá slabou metodu pro zabezpečení dat proti přístupu hrubou silou.

## Reference ##

* [Formát souboru osobních složek Outlooku (.pst)](https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx)
* [Specifikace formátu souboru osobních složek](https://github.com/libyal/libpff/blob/master/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

