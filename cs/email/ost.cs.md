{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OST - formát souboru úložiště aplikace Outlook",
  "description":"Další informace o formátu souboru OST a rozhraních API, která mohou vytvářet a otevírat soubory OST.",
  "linktitle" : "OST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor OST?

Soubory OST nebo Offline Storage Files představují data poštovní schránky uživatele v režimu offline na místním počítači po registraci na Exchange Server pomocí aplikace Microsoft Outlook. Je automaticky vytvořen při prvním použití aplikace Microsoft Outlook po připojení k serveru. Jakmile je soubor vytvořen, data se synchronizují s e-mailovým serverem, takže jsou dostupná i offline v případě odpojení od e-mailového serveru. Soubory OST mohou používat položky poštovní schránky, jako jsou e-maily, kontakty, informace z kalendáře, poznámky, úkoly a další podobná data. Uživatelé mohou vytvářet e-maily a další datové položky v souboru OST i bez připojení k serveru, ale nebudou synchronizovány se serverem. Po navázání spojení se místní soubor znovu synchronizuje se serverem, takže server i místní kopie jsou na stejné úrovni informací.

## Formát souboru OST

Formát souborů OST (Offline Storage Table) a [PST](/cs/email/pst/) (Personal Storage Table) se skládá z formátu Personal Folder File (PFF), který odpovídá ukládání uživatelských e-mailů, kontaktů a schůzek. Data v souboru PFF jsou uložena v little-endian se všemi daty a časy reprezentovanými jako FILETIME v UTC. [MS-PST] definuje dva typy PFF:

* 32bitový formát ANSI
* 64bitový formát Unicode

Formát souboru PST [specifikace](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546), jak je dostupný od společnosti Microsoft, lze také použít pro formát souborů OST jako bezplatný a neodvolatelné patentové licencování prostřednictvím Open Specification Promise. Skládá se z následujících rozlišitelných prvků:

* Fle hlavička
* Data záhlaví souboru
* Uzel větve indexu
* Uzel indexového listu
* (Soubor) index ofsetu
* Index deskriptoru (položky).
* Místní deskriptory
* Typ tabulky položek

### Informace v záhlaví

Struktura HEADER souboru OST je umístěna na samém začátku souboru s offsetem 0. Obsahuje informace metadat o souboru OST a informace ROOT pro přístup k datovým strukturám vrstvy NDB popsaným výše. Struktura HEADER se liší pro verze Unicode a ANSI formátu souboru OST.

Záhlaví začíná 4bajtovým magickým slovem **!BDN** reprezentovaným byty (0x21, 0x42, 0x44, 0x4E). Další 2bajtové magické číslo, **SM** (0x53, 0x4D), je umístěno na offsetu 8 od začátku souboru. Informace o verzi (ANSI nebo Unicode) leží v offsetu 10 od začátku souboru. Hexadecimální hodnota (0x17) určuje soubor OST Unicode, zatímco 0x0E nebo 0x0F představuje formát souboru ANSI.

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
|ullReserved (8 bajtů)|Rezervováno; MUSÍ být nastaven na nulu. Pouze formát souboru ANSI PST.
|dwReserved (4 bajty)|Reserved; MUSÍ být nastaveno na nulu. Pouze formát souboru ANSI PST.
|rgbReserved2 (3 bajty)|
|bRezervováno (1 bajt) |
|rgbReserved3 (32 bajtů) |

## Reference

* [Formát souboru osobních složek Outlooku (.ost)](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [Specifikace formátu souboru osobních složek](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

