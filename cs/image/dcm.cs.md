{
  "date" : "2019-10-11",
  "keywords" :[ "soubor dcm", "formát souboru dcm", "co je soubor dcm", "soubor", "příklad dcm", "přípona souboru dcm", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru DCM – soubor digitálních lékařských informací",
  "description":"Další informace o formátu souborů DCM a rozhraních API, která mohou vytvářet a otevírat soubory DCM.",
  "linktitle" : "DCM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-07-03"
}

## Co je soubor DCM?

Soubory s příponou .dcm představují digitální obraz, který uchovává lékařské informace pacientů, jako jsou MRI, CT skeny a ultrazvukové snímky. Soubory DCM používají formát obrazového souboru [DICOM](/cs/image/dicom) (Digital Imaging and Communications in Medicine) a mohou obsahovat referenční informace o pacientovi. Byl vyvinut [National Electrical Manufacturers Association](https://en.wikipedia.org/wiki/National_Electrical_Manufacturers_Association) (NEMA) a měl standardizovat formát zobrazovacích souborů pro distribuci a prohlížení lékařských snímků.

## Formát souboru DCM

Soubory DCM ukládají informace ve formátu obrazu DICOM. Tyto soubory ukládají datovou sadu, což jsou informace ze skutečného světa, které představují instanci SOP související s DICOM IOD. Metainformace souboru DICOM jsou uloženy v souboru, za kterým následuje bajtový proud aktuální sady dat.

### Metainformace souboru DICOM ##

Každý soubor DICOM obsahuje hlavičku identifikačních informací pro zapouzdřenou datovou sadu, která se skládá z:
* 128bajtová preambule souboru
* 4bajtová předpona DICOM
* Soubor Meta Elements

Tato hlavička je nutností pro každý soubor DICOM.

### Prvky metadat souboru ###
|Název atributu|Značka|Typ| Popis atributu
---|---|---|---|
|Preambule souboru|Žádná pole tagu nebo délky|1|Pevné pole o velikosti 128 bajtů dostupné pro použití podle aplikačního profilu nebo implementace. Pokud nejsou použity aplikačním profilem nebo specifickou implementací, všechny bajty musí být nastaveny na 00H. Čtečky nebo aktualizátory sady souborů se při určování, zda tento soubor je nebo není souborem DICOM, nesmí spoléhat na obsah této preambule.
|Předpona DICOM|Žádný štítek nebo pole délky|1|Čtyři bajty obsahující řetězec znaků "DICM". Tato předpona je určena k rozpoznání, zda tento soubor je nebo není souborem DICOM.
|Délka skupiny metainformací souboru|(0002,0000)|1|Počet bajtů za tímto metaprvkem souboru (konec pole Hodnota) až po poslední metaprvek souboru metainformací souboru 2 včetně
|Verze meta informací souboru|(0002,0001)|1|Toto je dvoubajtové pole, kde každý bit identifikuje verzi této hlavičky metainformací souboru. Ve verzi 1 je hodnota prvního bajtu 00H a hodnota bajtu druhé hodnoty je 01H. Implementace čtoucí soubory s metainformacemi, kde tento atribut má bit 0 (lsb) druhého bajtu nastavený na 1, mohou interpretovat metainformace souboru, jak je uvedeno v tomto verze PS3.10. Všechny ostatní bity se nekontrolují.
|UID třídy SOP pro ukládání médií|(0002,0002)|1|Unikátně identifikuje třídu SOP přidruženou k souboru dat. UID třídy SOP povolená pro ukládání médií jsou specifikována v PS3.4 - Profily aplikací pro ukládání médií.
|UID instance SOP úložiště médií|(0002,0003)|1|Unikátně identifikuje instanci SOP spojenou se sadou dat umístěnou v souboru a za metainformacemi souboru.
|UID syntaxe přenosu|(0002,0010)|1|Unikátně identifikuje syntaxi přenosu použitou ke kódování následující sady dat. Tato syntaxe přenosu se nevztahuje na metainformace souboru.
|UID třídy implementace|(0002,0012)|1|Unikátně identifikuje implementaci, která napsala tento soubor, a jeho obsah. Poskytuje jednoznačnou identifikaci typu implementace, která naposledy zapisovala soubor v případě problémů s výměnou.
|Název verze implementace|(0002,0013)|3|Určuje verzi pro UID třídy implementace (0002,0012) pomocí až 16 znaků repertoáru.
|Název entity zdrojové aplikace|(0002,0016)|3|Název entity aplikace DICOM (AE) AE, která napsala obsah tohoto souboru (nebo jej naposledy aktualizovala). Pokud je použit, umožňuje sledování zdroje chyb v případě problémů s výměnou médií.
|UID tvůrce soukromých informací|(0002,0100)|3|UID tvůrce soukromých informací (0002,0102).
|Soukromé informace|(0002,0102)|1C|Obsahuje soukromé informace umístěné v metainformacích souboru. Tvůrce musí být identifikován v (0002,0100). Povinné, pokud je přítomno UID tvůrce soukromých informací (0002,0100).

### Zapouzdření souboru dat ###

Soubor DICOM obsahuje jednu sadu dat, která představuje jednu instanci SOP související s jedinou třídou SOP. UID syntaxe přenosu metainformací souboru DICOM bude definovat syntaxi přenosu použitou ke kódování sady dat.

### Podpora informací o správě souborů ###

Vrstva formátu médií poskytuje v případě potřeby pro daný aplikační profil DICOM následující informace o správě souborů.

* Identifikace vlastníka obsahu souboru

* Statistiky přístupu k souboru (např. datum a čas vytvoření)

* Řízení přístupu k souboru aplikace

* Řízení přístupu k fyzickým médiím (např. ochrana proti zápisu)

## Reference ##
* [DICOM Standard](https://www.dicomstandard.org/current/)
* [Formát souboru DICOM](http://dicom.nema.org/dicom/2013/output/chtml/part10/chapter_7.html)

