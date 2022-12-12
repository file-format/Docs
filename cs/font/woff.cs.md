{
  "date" : "2020-08-20",
  "keywords" :[ "soubor woff", "formát souboru woff", "co je soubor woff", "soubor", "příklad woff", "přípona souboru woff", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WOFF - Web Open File Format",
  "description":"Soubor WOFF je otevřený formát písma vytvořený ve formátu Web Open Font Format.",
  "linktitle" : "WOFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-30"
}

## Co je soubor WOFF?

Soubor s příponou .woff je soubor webového písma založený na formátu WOFF (Web Open Font Format). Má komprimovaný kontejner specifický pro formát založený na typech písem TrueType (.TTF) nebo OpenType (.OTT). WOFF byl představen s cílem odlišit webová fonty od souborů fontů používaných v desktopových aplikacích. Kromě toho je formát zaměřen na snížení latence přenosu písem ze serveru do počítače klienta po síti. K dispozici je několik nástrojů, které dokážou převést soubory WOFF na TTF a další formáty souborů písem.

## **Formát souboru WOFF**

Formát písma WOFF komprimuje datové tabulky písem tabulkových struktur sfnt používaných v různých typech písem, jako je TrueType, OpenType a Open Font Format. Je to jako kontejner pro tyto typy písem a má také prostor pro zahrnutí metadat písem a dat pro soukromé použití, která mají být zahrnuta do kontejneru. Převaděče používají soubory sfnt do souboru ve formátu WOFF a uživatelští agenti obnovují zakódovaný soubor pro použití s webovým dokumentem. Je třeba poznamenat, že obnovená data písem přesně odpovídají vstupnímu formátu písma ze všech hledisek.

Soubor WOFF Pomůcky často obsahují další funkce, jako je podmnožina glyfů, ověřování nebo přidávání funkcí písma, ale není to nutné. Jak tvůrce, tak agenti použití musí zajistit, aby byla zachována platnost podkladových dat písem.

### Struktura souboru WOFF

Struktura souboru WOFF je podobná jako u písem sfnt. Je založen na adresáři tabulek, který obsahuje délky a offsety jednotlivých tabulek dat písem. Po této úvodní informaci následují všechny tabulky. Soubor obsahuje databázi písem, které jsou stejné jako v původních písmech. Pořadí tabulek je také stejné, ale každá může být komprimována. Adresář tabulky WOFF však nahrazuje původní adresář tabulky.

Soubor WOFF se skládá z následujících částí:

* WOFFHeader - Záhlaví souboru se základním typem a verzí písma, spolu s offsety na metadata a bloky soukromých dat.
* TableDirectory - Adresář tabulek písem, udávající původní velikost, komprimovanou velikost a umístění každé tabulky v souboru WOFF.
* FontTables - Tabulky dat písem ze vstupního písma sfnt, komprimované pro snížení požadavků na šířku pásma.
* ExtendedMetadata – Volitelný blok rozšířených metadat, reprezentovaný ve formátu XML a komprimovaný pro uložení v souboru WOFF.
* PrivateData – Volitelný blok soukromých dat, který může použít návrhář písem, slévárna nebo prodejce.

### Záhlaví WOFF
Záhlaví WOFF obsahuje identifikační podpis, který označuje druh dat obsažených v souboru. Záhlaví WOFF spolu s jeho poli je následující.

|Typ|Název pole|Popis|
---|---|---|
|UInt32|podpis |0x774F4646 'wOFF' |
|UInt32| chuť | "Verze sfnt" vstupního písma.|
|UInt32| délka |Celková velikost souboru WOFF.|
|UInt16| numTables |Počet položek v adresáři tabulek písem.|
|UInt16| vyhrazeno |Vyhrazeno; nastavit na nulu.|
|UInt32| totalSfntSize |Celková velikost potřebná pro nekomprimovaná data písem, včetně hlavičky sfnt, adresáře a tabulek písem (včetně odsazení).|
|UInt16| majorVersion |Hlavní verze souboru WOFF.|
|UInt16| minorVersion |Menší verze souboru WOFF.|
|UInt32| metaOffset |Offset k bloku metadat, od začátku souboru WOFF.|
|UInt32| metaLength |Délka komprimovaného bloku metadat.|
|UInt32| metaOrigLength |Nekomprimovaná velikost bloku metadat.|
|UInt32| privOffset |Offset k bloku soukromých dat, od začátku souboru WOFF.|
|UInt32| privLength |Délka bloku soukromých dat.|


## **Reference**
* [Formát souboru w3 WOFF](https://www.w3.org/TR/WOFF/)

