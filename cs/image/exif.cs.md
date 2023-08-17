{
  "date" : "2019-10-11",
  "keywords" :[ "soubor exif", "formát souboru exif", "co je soubor exif", "soubor", "příklad exif", "přípona souboru exif", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EXIF",
  "description":"Další informace o formátu souboru EXIF a rozhraních API, která mohou vytvářet a otevírat soubory EXIF.",
  "linktitle" : "EXIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor EXIF?
EXIF je zkratka pro „Exchangeable Image File Format“, což je definice, kterou poprvé poskytla [Japan Camera Industry Association](https://en.wikipedia.org/wiki/Japan_Electronic_Industries_Development_Association) (JCIA) v roce 1985. Standard spravuje Japan Electronics and Information Technology Industries Association (JEITA) k dnešnímu dni. EXIF je standard pro specifikace obrazových a zvukových formátů používaných především digitálními fotoaparáty a skenery.

Standard EXIF zahrnuje tagování a informace o metadatech s obrazovým souborem. Metadata mohou obsahovat informace jako model fotoaparátu, rychlost závěrky, datum a čas, clona, výrobce, expoziční čas, rozlišení X, rozlišení Y atd. Normálně jsou data EXIF ve výchozím nastavení skryta. Aby bylo možné zobrazit data EXIF, je třeba vybrat vlastnosti zobrazení v aplikaci pro prohlížení obrázků. Metadata Exif mohou také obsahovat miniatury spolu s technickými a primárními obrazovými daty v jediném obrazovém souboru.

## Historie a verze ##

* V říjnu 1995 JEIDA založila verzi 1. V této verzi JEIDA definovala strukturu, která se skládá z formátu obrazových dat a informací o atributech a základních značek.
* V listopadu 1997 byla představena verze 1.1 s většinou značek z verze 1, ale také byla přidána ustanovení pro informace o volitelných atributech a operaci formátu.
* Červen 1998, verze 2 s barevným prostorem sRGB, komprimovanými miniaturami a zvukovými soubory.
* Prosinec 1998, verze 2.1 s vylepšeným úložištěm a informacemi o atributech.
* Únor 2002, verze 2.2, vylepšená verze 2.1 s přidáním dokončování tisku.
* Září 2003, verze 2.21 s volitelným barevným prostorem známým jako adobe RGB.

## Formát souboru EXIF

EXIF používá následující formáty souborů s přidáním specifických metadat.

1. [JPEG](/cs/image/jpeg/) – diskrétní kosinusová transformace (DCT) pro komprimované obrazové soubory.
1. [TIFF](/cs/image/tiff/) Rev. 6.0 (RGB nebo YCbCr) pro nekomprimované obrazové soubory.
1. [RIFF](https://en.wikipedia.org/wiki/Resource_Interchange_File_Format) [WAV](https://en.wikipedia.org/wiki/WAV) pro zvukové soubory (Lineární [PCM](https://en.wikipedia.org/wiki/Pulse-code_modulation) nebo ITU-T [G.711](https://en.wikipedia.org/wiki/G.711) μ-Law PCM pro nekomprimovaná zvuková data a [ IMA](https://en.wikipedia.org/wiki/Interactive_Multimedia_Association)-[ADPCM](https://en.wikipedia.org/wiki/ADPCM) pro komprimovaná zvuková data).

### Značka používaná EXIFem ###

Značka 0xFFE0~~0xFFEF je "Značka aplikace", kterou používá uživatelská aplikace. Například starší digitální kamery používají pro ukládání snímků formát JFIF (JPEG File Interchange Format). JFIF používá značku APP0 (0xFFE0) pro vkládání konfiguračních dat digitální kamery a miniaturního obrázku. Kromě toho EXIF také používá značku aplikace pro vkládání dat, ale EXIF používá značku APP1 (0xFFE1), aby se zabránilo konfliktu s formátem JFIF. Každý formát souboru EXIF začíná tímto formátem.


|Značka SOI|Značka APP1|Data APP1|Jiná značka
---|---|---|---|
|FFD8|FFE1|SSSS 457869660000 TTTT......|FFXX SSSS DDDD......

Začíná od SOI (0xFFD8) Marker, takže je to soubor JPEG. Poté ihned následuje značka APP1. Všechna data EXIF jsou uložena v této datové oblasti APP1. Část "SSSS" v horní tabulce znamená velikost datové oblasti APP1 (datová oblast EXIF). Vezměte prosím na vědomí, že velikost "SSSS" zahrnuje také velikost samotného deskriptoru. Po "SSSS" se spustí data APP1. První část je speciální údaj pro identifikaci, zda je použit EXIF nebo ne, ASCII znak "EXIF" a 2 bajty 0x00. Po oblasti značek APP1 následují další značky JPEG.

### Struktura dat Exif ###

Hrubá struktura EXIF dat (APP1) je zobrazena níže. Jak bylo uvedeno výše, EXIF data začínají ASCII znakem "EXIF" a 2 bajty 0x00, pak následují EXIF data. EXIF používá k ukládání dat formát TIFF.


Značka |FFE1|APP1
---|---|
|SSSS|Data APP1|Velikost dat APP1
|45786966 0000|Záhlaví Exif
|49492A00 08000000|Záhlaví TIFF
|XXXX. . . .|IFD0 (hlavní obrázek)|Adresář
|LLLLLLLL|Odkaz na IFD1
|XXXX. . . .|Datová oblast IFD0
|XXXX. . . .|Exif SubIFD|Adresář
|00000000|Konec odkazu
|XXXX. . . .|Datová oblast Exif SubIFD
|XXXX. . . .|IFD1(obrázek miniatury)|Adresář
|00000000|Konec odkazu
|XXXX. . . .|Datová oblast IFD1
|FFD8XXXX. . . XXXXFFD9|Miniatura obrázku

#### Záhlaví TIFF ####

8bajtová hlavička souboru [TIFF](/cs/image/tiff/) obsahuje následující informace:

`Bajty 0-1:` Pořadí bajtů použité v souboru. Zákonné hodnoty jsou: „II“ (4949.H) „MM“ (4D4D.H).

Ve formátu „II“ je pořadí bajtů vždy od nejméně významného bajtu po nejvýznamnější bajt, pro 16bitová i 32bitová celá čísla. Toto se nazývá pořadí bajtů typu little-endian. Ve formátu „MM“ je pořadí bajtů vždy od nejvýznamnějšího po nejméně významný, pro 16bitová i 32bitová celá čísla. Toto se nazývá pořadí bajtů big-endian.

`Bajty 2-3:` Libovolné, ale pečlivě zvolené číslo (42), které dále identifikuje soubor jako soubor TIFF. Pořadí bajtů závisí na hodnotě bajtů 0-1.

`Bajty 4-7:` Posun (v bajtech) prvního IFD. Adresář může být na libovolném místě v souboru za záhlavím, ale musí začínat na hranici slova. Adresář obrazových souborů může zejména sledovat obrazová data, která popisuje. Čtenáři se musí řídit ukazateli, kam mohou vést. Termín bajtový offset se v tomto dokumentu vždy používá k označení umístění vzhledem k začátku souboru TIFF. První bajt souboru má offset 0.

#### Adresář souborů obrázku ####

IFD obsahuje informace o obrázku a také ukazatele na aktuální data obrázku. Skládá se z 2bajtového počtu položek v adresáři (tj. počtu polí), po kterém následuje sekvence 12bajtových položek v polích. , následovaný 4bajtovým offsetem dalšího IFD (nebo 0, pokud žádný). V souboru TIFF musí být alespoň 1 IFD a každý IFD musí mít alespoň jednu položku.

##### Záznam IFD #####

Každý 12bajtový záznam IFD je v následujícím formátu.


|Bajty|Popis
---|---|
|0-1|Značka, která identifikuje pole
|2-3|Typ pole
|4-7|Počet uvedeného typu
|8-11|Posun hodnoty, posun souboru (v bajtech) hodnoty pro pole. Očekává se, že hodnota bude začínat na hranici slova; odpovídající Posun hodnoty bude tedy sudé číslo. Tento posun souboru může ukazovat kdekoli v souboru, dokonce i za daty obrázku

Pole TIFF je logická entita sestávající z tagu TIFF a jeho hodnoty. Tento logický koncept je implementován jako položka IFD plus skutečná hodnota, pokud se nevejde do části hodnota/posun, posledních 4 bajtů položky IFD. Pojmy pole TIFF a položka IFD jsou ve většině kontextů zaměnitelné.

#### Náhled obrázku ####

Formát Exif obsahuje miniaturu obrázku (kromě Ricoh RDC-300Z). Obvykle se nachází vedle IFD1. K dispozici jsou 3 formáty miniatur; Formát JPEG (JPEG používá YCbCr), formát RGB TIFF, formát YCbCr TIFF.

##### Miniatura formátu JPEG #####

Pokud je hodnota značky Compression(0x0103) v IFD1 '6', formát miniatury je JPEG. Většina obrázků Exif používá pro miniatury formát JPEG. V takovém případě můžete získat offset miniatury podle značky JpegIFOffset(0x0201) v IFD1, velikost miniatury podle značky JpegIFByteCount(0x0202). Formát dat je běžný formát JPEG, začíná od 0xFFD8 a končí 0xFFD9. Zdá se, že formát JPEG a velikost 160x120 pixelů jsou doporučeným formátem miniatur pro Exif2.1 nebo novější.

##### Miniatura formátu TIFF #####

Pokud je hodnota značky Compression(0x0103) v IFD1 '1', formát miniatury není komprimovaný (tzv. obrázek TIFF). Počáteční bod dat miniatury je StripOffset(0x0111) Tag, velikost miniatury je součet StripByteCounts(0x0117) Tag.

## Reference ##

* [EXIF – z Wikipedie](https://en.wikipedia.org/wiki/Exif)
* [Formát souboru EXIF](https://www.media.mit.edu/pia/Research/deepview/exif.html)

