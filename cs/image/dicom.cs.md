{
  "date" : "2019-10-11",
  "keywords" :[ "soubor dicom", "formát souboru dicom", "co je soubor dicom", "soubor", "příklad dicom", "přípona souboru dicom", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DICOM - Formát souborů digitálního zobrazování a komunikace",
  "description":"Další informace o formátu souboru DICOM a rozhraních API, která mohou vytvářet a otevírat soubory DICOM.",
  "linktitle" : "DICOM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor DICOM?

DICOM je zkratka pro Digital Imaging and Communications in Medicine a týká se oblasti lékařské informatiky. DICOM se používá pro integraci lékařských zobrazovacích zařízení, jako jsou tiskárny, servery, skenery atd. od různých dodavatelů a také obsahuje identifikační údaje každého pacienta pro jedinečnost. Soubory DICOM lze sdílet mezi dvěma stranami, pokud jsou schopny přijímat obrazová data ve formátu DICOM. Komunikační částí DICOM je protokol aplikační vrstvy a ke komunikaci mezi entitami využívá TCP/IP. Verze podporované webovými službami jsou 1.0, 1.1, 2 nebo novější.

## Dějiny ##

DICOM byl vyvinut společně American College of Radiology (ACR) a National Electrical Manufacturers Association (NEMA) pro výměnu a prohlížení lékařských snímků, jako jsou MRI, CT skeny a ultrazvukové snímky. Zpočátku bylo těžké dekódovat obrázky, které stroje produkovaly. Proto ACR a NEMA společně vytvořily tým v roce 1983, který vydal svůj první standard, ACR/NEMA 300 v roce 1985. Druhá verze byla vydána v roce 1988, která byla mezi prodejci populárnější, ale brzy se zjistilo, že i druhá verze potřebuje vylepšení. 3. verze standardu byla vydána v roce 1993 jako „DICOM“. 3.0 je stále nejnovější verze, ale od roku 1993 je průběžně aktualizována.

## Formát souboru DICOM ##

DICOM je kombinací definice formátu souboru a síťového komunikačního protokolu. DICOM používá příponu .DCM. .DCM existuje ve dvou různých formátech, tj. formátu 1.xa formátu 2.x. DCM Format 1.x je dále k dispozici ve dvou verzích normální a rozšířené. Pro webové služby DICOM se používají protokoly HTTP a HTTPS.

### Záhlaví souboru ###

Záhlaví souboru obsahuje 128 bajtovou preambuli souboru a 4 bajtovou předponu DICOM.

**Preambule # 128 bajtů**|**Předpona # 4 bajty „D, I, C, M**

**Preambule** se používá pro přístup k obrázkům a dalším datům v souboru DICOM a poskytuje kompatibilitu s běžně používanými formáty souborů obrázků.

**Prefix** obsahuje řetězec "DICM" jako velká písmena.

### Soubor dat ###

Každý soubor musí obsahovat jednu datovou sadu představující instanci SOP a třídu SOP se souvisejícím IOD. Soubor dat je reprezentace informací skutečného světa. Datová sada obsahuje datové prvky a datové prvky obsahují hodnoty atributů daného objektu. Struktura atributů je specifikována v IOD. Datový objekt DICOM se skládá z řady atributů, včetně položek, jako je jméno, ID atd., a také jednoho speciálního atributu obsahujícího data obrazových pixelů.

### Datové prvky ###

Datový prvek se skládá z datového prvku Tag, délky hodnoty a hodnoty pro datový prvek. Existuje 5 typů datových prvků, jmenovitě Požadované datové prvky typu 1, Podmíněné datové prvky typu 1C, Požadované datové prvky typu 2, Podmíněné datové prvky typu 2C a volitelné datové prvky typu 3. Základní Tři typy struktur datových prvků jsou následující.

**Datový prvek s explicitním VR**

|Číslo skupiny|Číslo prvku|Reprezentace hodnoty|Rezervováno|Délka hodnoty|Pole hodnoty
---|---|---|---|---|---|
|2 bajty|2 bajty|2 bajty|2 bajty # 0x00, 0x00|4 bajty|"Value Length Bytes"

**Datový prvek s explicitním VR**

|Číslo skupiny|Číslo prvku|Reprezentace hodnoty|Délka hodnoty|Pole hodnoty
---|---|---|---|---|
|2 bajty|2 bajty|2 bajty|2 bajty|"Bajty délky hodnoty"

**Datový prvek s implicitní VR**


|Číslo skupiny|Číslo prvku|Délka hodnoty|Pole hodnoty
---|---|---|---|
|2 bajty|2 bajty|4 bajty|"Bajty délky hodnoty"

1. **Značka datového prvku**: Seřazené celé číslo, které představuje číslo skupiny a číslo prvku
1. **Value Representation VR**: VR je znakový řetězec, který představuje VR datového prvku.
1. **Value Length**: je celé číslo bez znaménka reprezentující explicitní délku pole hodnoty.
1. **Value Field**: Popisuje hodnoty datových prvků.

## Syntaxe převodu ##

Přenosová syntaxe je sada pravidel pro kódování, která jednoznačně představují abstraktnější syntaxe. S pomocí přenosové syntaxe komunikující entity vyjednávají o běžných technikách kódování, které podporují.

## SOP ##

Sjednocení IOD a DIMSE definuje třídu SOP. Definice třídy SOP obsahuje pravidla a sémantiku, která může omezit používání služeb ve skupině DIMSE Service Group nebo atributů IOD. Příklady prvků služby jsou Store, Get, Find, Move atd. Příklady objektů jsou CT snímky, MR snímky, ale zahrnují také seznamy plánů, tiskové fronty atd.

## Služby ##

DICOM poskytuje různé služby, většinou související s komunikací dat. Každý z nich je stručně popsán níže:


**Store:** Služba DICOM Store odesílá obrázky nebo jiné objekty do systému pro archivaci obrázků a komunikace (PACS) nebo na server.


**Závazek úložiště:** Služba Závazek úložiště se používá k potvrzení, že obraz byl trvale uložen v zařízení na jakémkoli typu média.


**Query/retrieve:** Tato služba umožňuje pracovní stanici najít seznamy obrázků nebo jiných objektů a poté je načíst z PACS.


**Modality worklist:** Služba modality worklist poskytuje seznam zobrazovacích procedur, které byly naplánovány k provedení zařízením pro získávání snímků.


**Tisk:** Tato služba odesílá snímky do tiskárny.

## Čísla portů přes IP ##

DICOM používá následující porty TCP a UDP:

1. 104
1. 2761
1. 2762
1. 11112

## Reference ##

* [https://en.wikipedia.org/wiki/DICOM](https://en.wikipedia.org/wiki/DICOM)
* [https://www.leadtools.com/sdk/medical/dicom-spec](https://www.leadtools.com/sdk/medical/dicom-spec)
* [https://www.dicomstandard.org/concepts/](https://www.dicomstandard.org/concepts/)
* [https://www.dicomlibrary.com/dicom/](https://www.dicomlibrary.com/dicom/)

