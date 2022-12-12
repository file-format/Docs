{
  "date" : "2019-10-11",
  "keywords" :[ "AVI", "Komprimované audio video", "Soubor", "Rozšíření", "Formát souboru", "Multimediální kontejner", "XVid", "DivX", "Kodeky", "Formát souboru pro výměnu zdrojů", "RIFF"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru AVI - soubor pro prokládání zvuku a videa",
  "description":"Další informace o formátu souborů AVI a rozhraních API, která mohou vytvářet a otevírat soubory AVI.",
  "linktitle" : "AVI",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-04-23"
}

## Co je soubor AVI? ##

Formát souboru **AVI** je formát multimediálního kontejneru Audio Video, který byl představen společností Microsoft. Obsahuje audio a video data vytvořená a komprimovaná pomocí několika kodeků (kodérů/dekodérů), jako jsou **XVid** a **DivX**. Vzhledem k tomu, že ke kódování obsahu AVI lze použít různé kodeky, aplikace pro načítání, tj. přehrávače AVI, by měly být schopny je otevřít pouze v případě, že mají nainstalované požadované kodeky, se kterými byl obsah AVI vytvořen. Formát je standardně podporován na všech platformách **Microsoft Windows** a také na téměř všech ostatních hlavních platformách. Několik aplikací a rozhraní API poskytuje možnost vytvářet/ukládat, číst a převádět AVI do jiných populárních formátů, jako jsou MP4, MOV, WMV atd.

## Formát souboru AVI ##

Soubor s příponou .avi je soubor AVI. Je to podformát Resource Interchange File Format (RIFF). RIFF organizuje data do bloků nebo "kusů", které jsou označeny značkou FourCC. Soubor AVI je jednoduše jeden „kus“ v souboru ve formátu RIFF.

V prvním dílčím bloku je záhlaví souboru identifikováno značkou "hdrl"; jeho obsah zahrnuje šířku, výšku a snímkovou frekvenci videa. Ve druhém dílčím bloku představuje značka pohybu snímkovou frekvenci videa. Video AVI se skládá ze skutečných audio/vizuálních dat v tomto bloku. Existuje také třetí volitelný subchunk s tagem „idx1“, který označuje pozici v rámci souboru jednotlivých datových bloků, které do souboru patří.

### Omezení ###

* Informace o poměru stran nelze zakódovat do původní specifikace AVI, i když pozdější specifikace OpenDML (AVI 2.0) nabízí standardizovanou metodu
* Ačkoli jsou soubory AVI široce používány ve filmové a televizní postprodukci, různé přístupy k přidávání časového kódu do nich si konkurují, což ovlivňuje použitelnost formátu.
* Video soubor zakódovaný v AVI nemůže používat techniku komprese, která vyžaduje budoucí data snímků za kódovaným snímkem (B-snímek)
* Je problematické používat soubory AVI s proměnnými datovými toky (VBR) (jako je zvuk MP3 se vzorkovací frekvencí pod 32 kHz)
* Soubor AVI kódující celovečerní filmy ve standardním rozlišení, jak se běžně používá, bude pravděpodobně vyžadovat režii asi 5 MB za hodinu, v závislosti na způsobu použití souboru
* Titulky musí být pevně zakódovány do video streamu nebo distribuovány v samostatném souboru v případě, že soubory AVI nemohou obsahovat přílohy, jako jsou fonty a titulky

## Stručná historie ##

AVI byl představen společností Microsoft v roce 1992 s cílem poskytnout robustnější a pokročilejší formát audio a video souborů. Tento formát se rychle stal populárním při používání internetu a umožňuje jednotlivcům přímo i nepřímo sdílet video soubory prostřednictvím cloudového úložiště médií.

## Reference ##

* [AVI – z Wikipedie](https://en.wikipedia.org/wiki/Audio_Video_Interleave)

