{
  "date" : "2021-02-15",
  "keywords" :[ "soubor asf", "formát souboru asf", "co je soubor asf", "soubor", "příklad asf", "přípona souboru asf", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASF - Advanced Systems File Format",
  "description":"Další informace o formátu souborů ASF a rozhraních API, která mohou vytvářet a otevírat soubory ASF.",
  "linktitle" : "ASF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Co je soubor ASF?

Soubor s příponou .asf je formát multimediálního souboru pro ukládání a přehrávání digitálních mediálních proudů přes síť. Jedná se o kontejnerový formát souboru, který může mít video i audio obsah pro streamování online. Soubory ASF najdete jen zřídka a pravděpodobněji narazíte na soubory Windows Media Audio ([WMA](/cs/audio/wma/)) a Windows Media Video ([WMV](/cs/video/wmv/)), které oba specifikují soubory ASF. s obsahem zakódovaným příslušnými kodeky. Soubory Windows Media lze vytvářet a číst pomocí sady Windows Media Format SDK.

## Formát souboru ASF

Soubor ASF může obsahovat více nezávislých nebo závislých toků. To může zahrnovat více zvukových proudů pro vícekanálový zvuk nebo vícenásobné datové toky videa. Díky více datovým tokům jsou toky vhodné pro přenos v různých šířkách pásma. Kromě toho mohou být proudy v souboru ASF v komprimovaném nebo nekomprimovaném formátu. Nejlepší komprese je dosaženo s kodeky Microsoft Windows Media Audio a Video 9 Series. Úplné specifikace formátu souboru ASF jsou k dispozici na [Webové stránky společnosti Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

### Struktura souboru nejvyšší úrovně ASF

Soubory ASF logicky obsahují tři typy objektů nejvyšší úrovně:

* `Objekt záhlaví` - povinný a musí být umístěn na začátku každého souboru ASF
* `Datový objekt` - povinný a musí následovat za objektem záhlaví
* `Index Object(s)` - volitelné, ale užitečné při poskytování časově založeného náhodného přístupu k souborům ASF

Následující obrázek ukazuje strukturu souborů ASF nejvyšší úrovně.

![ASF File Structure](../asf.png "ASF File Structure")

#### Objekt záhlaví nejvyšší úrovně ASF

Objekt Header poskytuje dobře známou sekvenci bajtů na začátku souborů ASF a může volitelně obsahovat metadata, jako jsou bibliografické informace. Obsahuje všechny informace, které jsou nutné pro správnou interpretaci informací v datovém objektu. Objekt záhlaví může zahrnovat několik standardních objektů, včetně, ale bez omezení na:

* Objekt Vlastnosti souboru - Obsahuje globální atributy souborů.
* Objekt Vlastnosti toku – Definuje tok digitálních médií a jeho charakteristiky.
* Objekt rozšíření záhlaví - Umožňuje přidat další funkce do souboru ASF při zachování zpětné kompatibility.
* Objekt Popis obsahu – Obsahuje bibliografické informace.
* Objekt příkazu skriptu – Obsahuje příkazy, které lze spustit na časové ose přehrávání.
* Objekt značky - Poskytuje pojmenované body skoku v souboru.

Objekt záhlaví je reprezentován pomocí následující struktury:

|Název pole |Typ pole |Velikost (bity)|
---|---|---|
|ID objektu| GUID| 128|
|Velikost objektu| QWORD| 64|
|Počet objektů záhlaví| DWORD| 32|
|Rezervováno1| BYTE| 8|
|Rezervováno2| BYTE| 8|

#### Datový objekt nejvyšší úrovně ASF

Všechna data digitálních médií pro soubor ASF jsou obsažena v datovém objektu a jsou uložena ve formě datových paketů ASF. Každý datový paket má pevnou délku a obsahuje data pro jeden nebo více digitálních mediálních toků.

#### Objekty indexu nejvyšší úrovně ASF

Objekty indexu nejvyšší úrovně ASF mají následující dva typy:

* `Jednoduchý indexový objekt` - Obsahuje časový index video dat v souboru ASF. Časový interval mezi položkami rejstříku je konstantní a je uložen v objektu Simple Index Object.
* `Objekt indexu` – odkazuje na objekt indexu, objekt indexu mediálního objektu a objekt indexu časového kódu, jejichž formáty jsou podobné. Stejně jako jednoduchý objekt indexu indexuje objekt indexu podle času s pevným časovým intervalem, ale není omezen na toky videa.

## Reference

* [Formát souboru ASF – Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)
* [Formát souboru QuickTime – Wikipedie](https://en.wikipedia.org/wiki/QuickTime_File_Format)

