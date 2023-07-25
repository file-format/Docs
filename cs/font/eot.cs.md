{
  "date" : "2020-08-20",
  "keywords" :[ "soubor eot", "formát souboru eot", "co je soubor eot", "soubor", "příklad eot", "přípona souboru eot", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EOT - TrueType Font File Format",
  "description":"Další informace o formátu souborů EOT a rozhraních API pro vytváření a otevírání souborů EOT.",
  "linktitle" : "EOT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Co je soubor EOT?

Soubor s příponou .eot je písmo OpenType, které je vložené do dokumentu. Ty se většinou používají ve webových souborech, jako je webová stránka. Byl vytvořen společností Microsoft a je podporován produkty společnosti Microsoft včetně souboru prezentace PowerPoint [.pps](/cs/presentation/pps). Soubor nemá primární použití a je jakýmsi doprovodným dokumentem s hlavním dokumentem nebo webovou stránkou. Podobně jako u písem OTF podporuje EOT pro glyfy obrysy Postscript i TrueType. Soubory EOT mají menší velikost z toho důvodu, že jsou komprimovány pomocí komprese LZ. EOT používá nástroj Microsoftu k vytvoření písma z existujících písem TTF/OTF.

## Stručná historie

Písmo EOT bylo předloženo W3C v roce 2007 jako součást CSS3, ale kvůli jeho požadavkům na trvalou instalaci na vzdáleném systému se stalo důvodem jeho zamítnutí. V březnu 2008 byl znovu předložen, ale W3C nakonec zvolilo [Web Font Format](/cs/font/woff/) (WOFF), který byl tehdy standardizován.

## Formát souboru EOT

Podrobnosti o formátu souboru EOT lze nalézt na [stránce odeslání W3](https://www.w3.org/Submission/EOT/#FileFormat) a obsahuje strukturu používanou tímto formátem písem. EOT se skládá z jediné struktury EMBEDDEDFONT, která poskytuje dostatek základních informací o názvu písma a podporovaných znacích. Zabalení těchto informací umožňuje uživatelským agentům vyhnout se rozbalení, dekomprimaci nebo instalaci písma, pokud je již na počítači přítomno.

### Struktura EMBEDDEDFONT
Struktura EMBEDDEDFONT prošla třemi revizemi s přidáním dalších dat na konec struktury s každou revizí. Poslední revize struktury EMBEDDEDFONT je znázorněna níže.

|Typ dat|Název položky|Popis|
---|---|---|
|unsigned long|EOTSize|Celková délka struktury v bajtech (včetně dat řetězce a písma)|
|unsigned long|FontDataSize|Délka písma OpenType (FontData) v bajtech|
|unsigned long|Verze|Číslo verze tohoto formátu - 0x00020002|
|nepodepsané dlouhé|Příznaky|Zpracování příznaků|
|byte[10]|FontPANOSE|Hodnota PANOSE pro toto písmo – viz http://www.microsoft.com/typography/otspec/os2.htm#pan|
|byte|Znaková sada|V systému Windows je odvozena z TEXTMETRIC.tmCharSet. Tato hodnota určuje znakovou sadu písma. DEFAULT_CHARSET (0x01) označuje žádnou preferenci. – Viz https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica|
|byte|Italic|Pokud je bit pro ITALIC nastaven v OS/2.fsSelection, hodnota bude 0x01 – viz http://www.microsoft.com/typography/otspec/os2.htm#fss|
|unsigned long|Weight|Hodnota váhy pro toto písmo – viz http://www.microsoft.com/typography/otspec/os2.htm#wtc|
|nepodepsané short|fsType|Příznaky typu, které poskytují informace o oprávněních pro vkládání – viz http://www.microsoft.com/typography/otspec/os2.htm#fst|
|nepodepsané zkratka|MagicNumber|Magické číslo pro soubor EOT - 0x504C. Používá se ke kontrole poškození dat.|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (bity 0-31) – viz http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (bity 32-63) – Viz http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (bity 64-95) – Viz http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (bity 96-127) – Viz http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|CodePageRange1|CodePageRange1 (bity 0-31) – viz http://www.microsoft.com/typography/otspec/os2.htm#cpr|
|unsigned long|CodePageRange2|CodePageRange2 (bity 32-63) – viz http://www.microsoft.com/typography/otspec/os2.htm#cpr|
|unsigned long|CheckSumAdjustment|head.CheckSumAdjustment – viz http://www.microsoft.com/typography/otspec/head.htm|
|unsigned long|Reserved1|Reserved - musí být 0|
|unsigned long|Reserved2|Reserved - musí být 0|
|unsigned long|Reserved3|Reserved - musí být 0|
|unsigned long|Reserved4|Reserved - musí být 0|
|unsigned short|Padding1|Padding pro zachování dlouhého zarovnání. Hodnota výplně musí být vždy nastavena na 0x0000.|
|unsigned short|FamilyNameSize|Počet bajtů použitých polem FamilyName|
|byte|FamilyName[FamilyNameSize]|Pole znaků UTF-16 o délce bajtů FamilyNameSize. Toto je řetězec rodiny písem v anglickém jazyce nalezený v tabulce názvů písma (ID názvu = 1) – viz http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding2|Hodnota odsazení musí být vždy nastavena na 0x0000.|
|unsigned short|StyleNameSize|Počet bajtů použitých StyleName|
|byte|StyleName[StyleNameSize]|Pole znaků UTF-16 o délce bajtů StyleNameSize. Toto je řetězec podrodiny písem v anglickém jazyce nalezený v tabulce názvů písma (ID názvu = 2) – viz http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding3|Hodnota odsazení musí být vždy nastavena na 0x0000.|
|unsigned short|VersionNameSize|Počet bajtů použitých názvem VersionName|
|bytes|VersionName[VersionNameSize]|Pole znaků UTF-16 o délce bajtů SizeNameSize. Toto je řetězec anglické verze nalezený v tabulce názvů písma (ID názvu = 5) – viz http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding4|Hodnota výplně musí být vždy nastavena na 0x0000.|
|unsigned short|FullNameSize|Počet bajtů použitých celým jménem|
|byte|FullName[FullNameSize]|Pole znaků UTF-16 o délce bajtů FullNameSize. Toto je řetězec úplného názvu v angličtině, který se nachází v tabulce jmen písma (ID názvu = 4) – viz http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding5|Hodnota výplně musí být vždy nastavena na 0x0000.|
|unsigned short|RootStringSize|Počet bajtů použitých polem RootString|
|byte|RootString[RootStringSize]|Pole znaků UTF-16 o délce bajtů RootStringSize.|
|unsigned long|RootStringCheckSum|Hodnota kontrolního součtu kořenového řetězce. Viz algoritmus pro zpracování RootStringChecksum níže.|
|unsigned long|EUDCCodePage|Hodnota kódové stránky potřebná pro podporu písem EUDC.|
|unsigned short|Padding6|Hodnota výplně musí být vždy nastavena na 0x0000.|
|unsigned short|SignatureSize|Počet bajtů použitých polem Signature. Aktuálně rezervováno a mělo by být nastaveno na 0x0000.|
|byte|Podpis[Velikost podpisu]|Momentálně rezervováno. Pokud je SignatureSize 0x0000, toto pole nemá žádnou délku.|
|unsigned long|EUDCFlags|Zpracování příznaků pro písmo EUDC. Typické hodnoty mohou být TTEMBED_XORENCRYPTDATA a TTEMBED_TTCOMPRESSED.|
|unsigned long|EUDCFontSize|Počet bajtů použitých polem Signature.|
|byte|EUDCFontData[EUDCFontSize]|Počet bajtů použitých pro data písem EUDC. Pokud je EUDCFontSize 0x00000000, toto pole nemá žádnou délku.
|byte|FontData[FontDataSize]|Data písem pro tento soubor EOT. Data mohou být komprimována nebo zašifrována XOR, jak indikují příznaky zpracování.|

## Reference

* [Formát souboru EOT](https://www.w3.org/Submission/EOT/)
* [Embedded OpenType](https://en.wikipedia.org/wiki/Embedded_OpenType)
* [Vkládání písem](https://en.wikipedia.org/wiki/Font_embedding)

