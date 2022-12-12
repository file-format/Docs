{
  "date" : "2019-12-13",
  "keywords" :[ "soubor ppt", "formát souboru ppt", "co je soubor ppt", "soubor", "příklad ppt", "přípona souboru ppt", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souboru PPT a rozhraních API, která mohou vytvářet a otevírat soubory PPT.",
  "title" :"PPT - formát souboru PowerPoint",
  "linktitle" : "PPT",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor PPT?

Soubor s příponou PPT představuje soubor PowerPoint, který se skládá z kolekce snímků pro zobrazení jako SlideShow. Určuje binární formát souboru používaný aplikací Microsoft PowerPoint 97-2003. Soubor PPT může obsahovat několik různých typů informací, jako je text, odrážky, obrázky, multimédia a další vložené objekty OLE. Microsoft přišel s novějším formátem souborů pro PowerPoint, známým jako [PPTX](/cs/presentation/pptx/), od roku 2007, který je založen na Office OpenXML a je odlišný od tohoto binárního formátu souboru. Soubory PPT může vytvářet také několik dalších aplikačních programů, jako je OpenOffice Impress a Apple Keynote.

## Stručná historie ##

Společnost Microsoft představila formát souboru PPT s vydáním PowerPointu v roce 1987. Stabilní binární formát byl sdílen jako výchozí v PowerPoint 97-2003 pro Windows. Binární formát souboru je podporován pro čtení a zápis nejnovějšími verzemi PowerPointu, včetně PowerPoint 2016.

## Specifikace formátu souboru ##

Od svého zavedení prošel formát souboru PPT několika revizemi pro přidání nových funkcí a vylepšení. Nejnovější dostupné specifikace verze jsou specifikace revize 6.0, které byly zveřejněny v srpnu 2018, což by nemělo být směšováno se skutečným produktovým číslem formátu souboru PPT, protože Microsoft již pro tento formát neposkytuje žádné úpravy.

### Přehled formátu souboru ###

Některé z klíčových součástí formátu souboru PPT jsou následující:

#### Snímky ####

Uživatelská data, jako jsou tvary, text, animace a média, jsou přidána do prezentace uvnitř snímku. Prezentace může obsahovat jeden nebo více snímků, které se při spuštění prezentace zobrazí jako prezentace. Prezentace obsahuje hlavní snímky a snímky titulků, které fungují jako šablona pro běžné vizuální vlastnosti snímků prezentace. K dispozici je také hlavní snímek poznámek a hlavní snímek podkladů, které slouží podobnému účelu a poskytují společné vizuální vlastnosti pro všechny snímky s poznámkami a všechny tištěné podklady.

#### Tvary ####

Tvary jsou objekty, které uživatelům umožňují přidávat na snímek různý obsah ve formě zástupných tvarů, obrázků a grafů. Obrazce na hlavním snímku definují společná data pro skupiny obrazců.

#### Zástupné tvary ####

Jedná se o speciální zástupné symboly, které slouží jako kontejnery pro různé objekty. Různé zástupné tvary lze použít k poskytnutí vodítek pro vložení konkrétních typů tvarů, jako jsou tabulky nebo grafy. Uvnitř snímku se zástupný tvar přizpůsobí vizuálním vlastnostem hlavního hlavního snímku, titulního hlavního snímku nebo hlavního snímku poznámek.

#### Externí objekty ####

Externí objekty, jako je vložený a propojený zvuk, propojené video, vložené a propojené objekty OLE a hypertextové odkazy, lze vložit do snímku. Tyto objekty lze použít k aktivaci propojených objektů pro přístup k externím zdrojům během prezentace.

### Struktury formátu souborů ###

Binární formáty souborů PowerPoint se skládají z následujících proudů, které představují celkovou strukturu dokumentu a data.

* Aktuální uživatelský stream
* Stream dokumentů PowerPoint
* Stream obrázků
* Souhrnné informace a Souhrnné informace o dokumentu (volitelné)

Úplné specifikace pro formát souboru DOC lze nalézt tak, jak je poskytuje [Microsoft](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx) a měli byste je konzultovat s odkazem na oddíly uvedené v následujících podrobnostech.

#### Aktuální uživatelský stream ####

Uchovává záznam posledního uživatele, který dokument otevřel, a jeho jméno musí být "Aktuální uživatel".

#### Stream dokumentů PowerPoint ####

Uchovává záznamy o všech informacích o prezentaci PowerPoint a vysvětluje její rozvržení a obsah. Je to povinný datový proud, jehož název MUSÍ být „Dokument PowerPoint“. Obsah tohoto streamu je specifikován posloupností záznamů nejvyšší úrovně. Částečná omezení řazení pro sekvenci záznamů jsou specifikována v záznamech PersistDirectoryAtom a UserEditAtom.

Jako záznamy kontejneru jsou záznamy DocumentContainer, MainMasterContainer (část 2.5.3), HandoutContainer (část 2.5.8), SlideContainer (část 2.5.1) a NotesContainer (část 2.5.6) kořenem stromu záznamů o kontejneru. a atomové záznamy. Uvnitř libovolného záznamu kontejneru mohou existovat další záznamy, které nejsou explicitně uvedeny jako podřízené záznamy. Neznámé záznamy jsou identifikovány, když pole recType struktury RecordHeader (část 2.3.1) obsahuje hodnotu, která není specifikována výčtem RecordType (část 2.13.24). Tyto neznámé záznamy, pokud na ně narazí, MUSÍ být ignorovány a MOHOU<1> být zachovány. Neznámé záznamy lze ignorovat vyhledáním dopředných bajtů recLen od konce struktury RecordHeader.

Pokaždé, když je tento stream zapsán, mohou být k existujícímu streamu přidány nové záznamy nejvyšší úrovně, uživatelská úprava nebo může být obsah celého streamu nahrazen aktualizovanou sekvencí záznamů nejvyšší úrovně. Pokud není nahrazen celý datový proud, všechny dříve existující záznamy nejvyšší úrovně, které zahrnovaly jakoukoli předchozí uživatelskou úpravu, mohou být zastaralé následně připojenými záznamy nejvyšší úrovně, které tvoří aktuální uživatelskou úpravu.

#### Stream obrázků ####

Toto je volitelný datový proud, který obsahuje data o obrázcích obsažených v prezentaci PowerPoint. Jeho název MUSÍ být "Obrázky". Obsah tohoto streamu je specifikován záznamem OfficeArtBStoreDelay, jak je uvedeno v [MS-ODRAW] části 2.2.21.

#### Souhrnný informační stream ####

Vede statistiky o dokumentu podle standardu Microsoft Office. Název proudu souhrnných informací musí být "\005SummaryInformation", kde \005 je znak s hodnotou 0x0005, nikoli řetězcový literál "\005". Tento proud BY MĚL být u šifrovaných dokumentů vynechán. Obsah tohoto streamu je specifikován v [MS-OSHARED], oddíl 2.3.3.2.1.

#### Souhrnný informační proud dokumentu ####

Volitelný datový proud, jehož název MUSÍ být "\005DocumentSummaryInformation", kde \005 je znak s hodnotou 0x0005, nikoli řetězcový literál "\005". Tento proud MŮŽE být<2> u šifrovaných dokumentů vynechán. Obsah tohoto proudu je specifikován v [MS-OSHARED], oddíl 2.3.3.2.2.

#### Šifrovaný proud souhrnných informací ####

Volitelný stream, jehož název MUSÍ být „EncryptedSummary“. Tento stream existuje pouze v zašifrovaném dokumentu. Obsah tohoto streamu je specifikován v [MS-OFFCRYPTO], oddíl 2.3.5.4.

#### Úložiště digitálního podpisu ####

Volitelné úložiště, jehož název MUSÍ být "_xmlsignatures". MŮŽE být vynechán a MŮŽE být ignorován. Obsah tohoto úložiště je specifikován v [MS-OFFCRYPTO], oddíl 2.5.2.

#### Vlastní úložiště dat XML ####

Volitelné úložiště, jehož název MUSÍ být „MsoDataStore“. Obsah úložiště je specifikován v [MS-OSHARED], oddíl 2.3.6.

#### Stream podpisů ####

Volitelný stream, jehož název MUSÍ být „_signatures“. MĚLO BY být vynecháno a MŮŽE být ignorováno. Obsah tohoto streamu je specifikován v [MS-OFFCRYPTO], oddíl 2.5.1.

## Reference ##

* [Specifikace formátu souboru PPT](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx)
* [[MS-OSHARED]: Běžné datové typy a struktury objektů Office](https://msdn.microsoft.com/en-us/library/office/cc313156(v#office.12).aspx)
* [[MS-OFFCRYPTO] – Struktura šifrování dokumentů Office](https://msdn.microsoft.com/en-us/library/office/cc313071(v#office.12).aspx)
* [Formáty souborů PowerPoint](https://en.wikipedia.org/wiki/Microsoft_PowerPoint#File_formats)

