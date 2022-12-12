{
  "date" : "2020-03-16",
  "keywords" :[ "Soubor IGES", "Formát souboru", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souboru IGES a rozhraních API, která mohou vytvářet a otevírat soubory IGES.",
  "title" :"Formát souboru IGES",
  "linktitle" : "IGES",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## Co je soubor IGES?

Soubor s příponou .iges se používá k výměně informací o návrhu mezi aplikacemi CAD (Computer-Aided Design). IGES je zkratka pro Initial Graphics Exchange Specifications. Informace vyměňované pomocí IGES zahrnují schéma zapojení, drátěný model, povrchy volného tvaru nebo reprezentace modelování těles. IGES nachází své aplikace v tradičních technických výkresech, analýze modelů a výrobních funkcích. Formát si může vyměňovat 2D nebo 3D informace o návrhu mezi CAD programy. Soubory IGES lze otevřít pomocí několika aplikací CAD, jako je Autodesk a CADSoftTools ABViewer. K dispozici je také několik rozhraní API pro programové otevírání a převod souborů IGES.

## Formát souboru IGES

Soubory IGES jsou v textovém formátu ASCII a lze je otevřít v libovolném textovém editoru a zobrazit obsah souboru. Textové informace v souboru IGES jsou reprezentovány ve formátu "Hollerith". Běžný soubor IGES může obsahovat tisíce řádků reprezentujících 2D nebo 3D informace, které lze vyměňovat podle tohoto formátu. Soubor IGES je rozdělen do pěti sekcí označených konkrétním velkým písmenem v 73. sloupci. Těmito sekcemi jsou sekce „Start“ (S), „Globální“ (G), „Zadávání dat“ (D), „Data parametrů“ (P) a „Konec“ (T). Sekce Data Entry a Parameter Data jsou běžně zkráceny DE a PD, v daném pořadí.

### Záhlaví souboru IGES

Sekce Start a Global obsahují základní informace o:
* Název souboru a jeho zdroj
* Oddělovače pro sekci Data parametrů
* Autor souboru a další obecné informace.

Sekce Start a Global z ukázkového dokumentu na Wikipedii jsou následující.
```
S      1
1H,,1H;,4HSLOT,37H$1$DUA2:[IGESLIB.BDRAFT.B2I]SLOT.IGS;,                G      1
17HBravo3 BravoDRAFT,31HBravo3->IGES V3.002 (02-Oct-87),32,38,6,38,15,  G      2
4HSLOT,1.,1,4HINCH,8,0.08,13H871006.192927,1.E-06,6.,                   G      3
31HD. A. Harrod, Tel. 313/995-6333,24HAPPLICON - Ann Arbor, MI,4,0;     G      4
```
Jak je vidět, počáteční pole obsahuje pro člověka čitelné popisy souboru a ve sloupcích 1-72 mám libovolné znaky, přičemž řádek končí záhlavím oddílu a číslem řádku oddílu. V části Start musí být alespoň 1 řádek. Globální sekce obsahuje data preprocesoru. Musí se také nacházet v souboru a končit formátem G000000#.

### Sekce zadávání dat (DE) a dat parametrů (PD).

#### Sekce zadávání dat
Soubor IGES se skládá z několika entit, které obsahují informace o základních datech formátu souboru IGES. Entita obsahuje informace o různých prvcích datového formátu IGES a používá se pro kreslení. Mezi běžně používané entity patří:
* Kruhový oblouk
* Složená křivka
* Kuželový oblouk
* Letadlo
* Linka

To je jen několik a v IGES je kolem 150 různých subjektů. Každá entita je identifikována číslem typu, například:
* CIRCULAR ARC (Typ 100)
* LINE (typ 110)

##### Vlastnosti entity

Každá deklarovaná entita má následující vlastnosti.

|Název pole|Popis|
---|---|
|Typ entity |Toto je popisovaný typ entity. Například 116 popisuje entitu bodu.|
|Ukazatel PD |Udává umístění dat těchto entit v sekci Data parametrů. Toto umístění je jednoduše číslo řádku uvnitř sekce PD, která obsahuje první řádek dat této entity.|
|Struktura |Nula nebo ukazatel na definiční entitu. Neplatí pro většinu subjektů|
|Vzor čárového písma| Číslo nebo ukazatel na entitu vzoru písma řádku. Číslo znamená: * 0 Není zadán žádný vzor (výchozí) * 1 Plná * 2 Přerušovaná * 3 Skrytá * 4 Středová čára * 5 Tečkovaná|
|Úroveň| Určuje úrovně, které mají být spojeny s touto entitou. Umožňuje entitě objevit se na více než jedné úrovni|
|Zobrazit| Určuje možnosti zobrazení. Jsou to: 0 Označuje stejnou viditelnost a vlastnosti ve všech pohledech. Výchozí ukazatel na entitu View (Typ 410), kterou lze zobrazit z odkazu na entitu Viditelné Asociativnosti pohledu (Typ 402, Formulář 3)
|Ukazatel transformační matice| Odkazuje na entitu transformační matice (typ 124) nebo je ve výchozím nastavení nula (bez transformace)|
|Asociativita zobrazení štítků| Odkazuje na asociativitu zobrazení štítků (typ 402, formulář 5), která definuje, jak se zobrazí štítek entity.|
|Stavové číslo| Obsahuje čtyři části po dvou číslech. 1-2: Stav prázdné. Buď 00 pro normální nebo 01 pro blanked. 3-4: Přepínač podřízené entity: je 00 pro nezávislé, 01 pro fyzicky závislé, 02 pro logicky závislé a 03 pro oba. 5-6: Příznak použití entity: je buď 00 pro geometrii, 01 pro anotaci, 02 pro definici, 03 pro jiné, 04 pro logiku, 05 pro 2D parametrickou a 06 pro konstrukční geometrii. Nakonec 7-8 je hierarchie, kde 00 označuje globální shora dolů (použijte charakteristiky této entity), 01 je globální odložení (nepoužívejte charakteristiky této entity) a 02 je vlastnost použití hierarchie (použijte entitu hierarchie (typ 406, formulář 10)určit charakteristiky hierarchického seskupení).|
|Pořadové číslo| Určeno pomocí D#, kde # je číslo řádku pro tuto sekci (nikoli z horní části souboru). To se také používá k ukázání na tuto entitu Data Entry.|
|Typ entity| je specifikováno dvakrát pro každý výpis entity|
|Číslo tloušťky čáry| Určuje tloušťku při zobrazování entity. Nejmenší je 1, 0 je výchozí|
|Číslo barvy| Určuje barvu entity. Povolené celočíselné hodnoty jsou: 0 Žádná barva (výchozí) 1 Černá 2 Červená 3 Zelená 4 Modrá 5 Žlutá 6 Purpurová 7 Azurová 8 Bílá|
|Číslo počtu řádků parametrů| Určuje počet řádků, které tato entita zabírá v sekci Parametr dat|
|Číslo formuláře| Označuje formu nebo reprezentaci této entity. Mění způsob interpretace dat parametrů. Výchozí hodnota je 0|
|Vyhrazené pole| Nepoužitý|
|Vyhrazené pole| Nepoužitý|
|Štítek entity| Identifikátor zadaný přihláškou - oprávněný k právu|
|Číslo dolního indexu| Číselný kvalifikátor pro označení entity. Oba dohromady tvoří jedinečný identifikátor entity|
|Pořadové číslo Viz výše. |To bude D#+1, protože každá entita je specifikována na dvou řádcích.|

#### Sekce dat parametrů
Po sekci Data Entries následuje sekce Parametr Data. Uvádí data pro každý příslušný záznam a uvádí parametry pro entitu na základě oddělovačů zadaných v sekci Globální (obvykle čárky k oddělení parametrů a středník k ukončení výpisu).


## Reference
* [IGES by WikiPedia](https://en.wikipedia.org/wiki/IGES)

