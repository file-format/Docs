{
  "date" : "2019-10-11",
  "keywords" :[ "soubor dng", "formát souboru dng", "co je soubor dng", "soubor", "příklad dng", "přípona souboru dng", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DNG - Formát obrázku digitálního fotoaparátu",
  "description":"Další informace o formátu souborů DNG a rozhraních API, která mohou vytvářet a otevírat soubory DNG.",
  "linktitle" : "DNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor DNG?

DNG je obrazový formát digitálního fotoaparátu používaný pro ukládání nezpracovaných souborů. Byl vyvinut společností Adobe v září 2004. V podstatě byl vyvinut pro digitální fotografii. DNG je rozšířením standardního formátu [TIFF](/cs/image/tiff/)/EP a významně využívá metadata. Aby mohli fotografové manipulovat s nezpracovanými daty z digitálních fotoaparátů se snadnou flexibilitou a uměleckým ovládáním, volí soubory camera raw. Formáty JPEG a TIFF ukládají snímky, které zpracovává fotoaparát, a proto v těchto formátech není k dispozici mnoho prostoru pro úpravy.

## Historie a verze formátu souborů DNG

Doposud bylo k dispozici 5 verzí specifikace DNG. Verze 1.0.0.0 byla spuštěna v září 2004 spolu s vydáním "2.3" (ACR a DNG Converter). V únoru 2005 byla vydána verze 1.1.0.0. V květnu 2008 byla vydána verze 1.2.0.0 a byla použita v "4.4". Verze 1.3.0.0 byla zveřejněna v červnu 2009. Verze 1.4.0.0 se objevila v roce 2012.

## Formát souboru DNG

Zatímco soubory camera raw zachycují nezpracovaná nebo málo zpracovaná data přímo ze snímače. Protože jsou podobné filmovým negativům, jsou formáty camera raw také známé jako „digitální negativy“. Výhodou raw formátů je zvýšená umělecká kontrola pro koncového uživatele. Uživatel může upravit různé rozsahy parametrů podle požadavků, jako je vyvážení bílé, mapování tónů, redukce šumu, doostření a tak dále. Na druhou stranu soubor camera raw musí být zpracován pro jakékoli použití pomocí jakéhokoli softwaru nebo pomocí konvertoru.

Protože pro soubory camera raw nebyl k dispozici žádný standardní formát, způsobovalo to koncovému uživateli řadu problémů. Tyto problémy řešila společnost Adobe a definovala neproprietární formát pro soubory camera raw. Formát je známý jako Digital Negative nebo DNG. DNG může být použito širokou škálou hardwaru a softwaru pro zpracování nezpracovaných souborů. Kromě toho lze DNG použít také jako meziformát pro ukládání snímků, které byly původně zachyceny fotoaparáty, které mají své vlastní proprietární raw formáty.

### Specifikace formátu souboru DNG

V této části popíšeme formát DNG jako rozšíření TIFF 6.0.

* **Přípony souborů**: DNG používá přípony „.DNG“ nebo „.TIF“.
* **Stromy SubIFD**: DNG nepodporuje řetězce SubIFD, místo toho DNG doporučuje použití stromů SubIFD, jak je uvedeno ve specifikacích TIFF-EP. Nejvyšší kvalita a rozlišení může používat NewSubFileType 0, zatímco miniatury se sníženou kvalitou by měly používat NewSubFileType rovný 1. Rovněž se doporučuje, i když to není vyžadováno, aby první IFD musel mít miniaturu nízké kvality nebo rozlišení.
* **Pořadí bajtů**: Pořadí bajtů musí podporovat čtečky DNG, a to i pro soubory z konkrétního modelu fotoaparátu.
* **Maskované pixely**: Většina snímačů fotoaparátu vypočítává plně maskované pixely na okraji snímače pomocí černého kódování. Tyto pixely lze před uložením obrázku ve formátu DNG buď zahrnout, nebo oříznout. Pokud maskované pixely nejsou oříznuty, musí být plocha těchto pixelů uvedena v tagu ActiveArea. Informace shromážděné z těchto pixelů o úrovni kódování černé by měly být použity buď před uložením nezpracovaných dat, nebo mohou být zahrnuty do souboru DNG určujícího úroveň černé.
* **Vadné pixely**: Před uložením nezpracovaných dat jako DNG by měly být vadné pixely vyloučeny.
* **Metadata**: Metadata mohou být zahrnuta do DNG některým z následujících způsobů:
** Pomocí značek metadat TIFF-EP nebo EXIF
** Prostřednictvím značky metadat IPTC (33723)
** Použití značky metadat XMP (700)
* **Proprietární data**: Dodavatelé obvykle zahrnují proprietární data v nezpracovaných souborech, která mají používat jejich vlastní převodníky. DNG ukládá svá proprietární data v soukromých značkách, soukromých IFD a v soukromém MakerNote. Dodavatelé musí používat značky DNGPrivateData a MakerNoteSafety, aby zajistili, že aplikace, které upravují soubory DNG, uchovávají tato proprietární data.

Následují některá důležitá omezení a rozšíření značek TIFF.

**BitsPerSample**

Podporováno je 8 až 32 bitů/vzorek. Každý vzorek musí mít stejnou hloubku, když se SamplesPerPixel nerovná 1. Pokud se však BitsPerSample nerovná 8, 16 nebo 32, pak musí být bity zabaleny do bajtů pomocí výchozího FillOrder TIFF 1 (big-endian).

**Komprese**

Jsou podporovány dvě hodnoty značky komprese:

* Hodnota # 1: Nekomprimovaná data.
* Hodnota # 7: Komprimovaná data JPEG, buď základní DCT JPEG, nebo bezeztrátová komprese JPEG.

**Fotometrická interpretace**

Následující hodnoty jsou podporovány pouze pro miniatury a náhledy IFD:

* 1 = BlackIsZero. Předpokládá se, že je v barevném prostoru gama 2.2.
* 2 = RGB. Předpokládá se, že je v barevném prostoru sRGB.
* 6 = YCbCr. Používá se pro náhledové obrázky zakódované ve formátu JPEG.

Pro nezpracovaný IFD jsou podporovány následující hodnoty a předpokládá se, že jde o nativní barevný prostor kamery:

* 32803 # CFA (Color Filter Array).
* 34892 # LinearRaw.

**Orientace**

Orientační značka se používá pro prohlížeče souborů, aby mohly provádět bezeztrátovou rotaci souborů DNG. Čtečky DNG musí podporovat všechny možné orientace, včetně zrcadlených orientací.

## Funkce v nejnovější verzi DNG

Verze DNG 1.4 Říjen 2012 má následující pokročilé funkce.

* Výchozí uživatelské oříznutí
* Transparentnost
* Plovoucí desetinná čárka (HDR)
* Ztrátová komprese
* Proxy

## Reference ##

* [Specifikace DNG – od společnosti Adobe](https://www.kronometric.org/phot/processing/DNG/dng_spec_1.4.0.0.pdf)
* [Digital Negative – Wikipedia](https://en.wikipedia.org/wiki/Digital_Negative)
* [DNG – Veřejný archivní formát pro nezpracovaná data z digitálního fotoaparátu](https://helpx.adobe.com/photoshop/digital-negative.html)

