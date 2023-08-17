{
  "date" : "2021-02-01",
  "keywords" :[ "usdz", "soubor usdz", "formát souboru usdz", "formát souboru", "3d","stažení souboru usdz"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USDZ - formát ZIP s univerzálním popisem scény",
  "description":"Další informace o formátu souboru USDZ a rozhraních API, která mohou otevírat a vytvářet soubory USDZ.",
  "linktitle" : "USDZ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## Co je soubor USDZ?

Soubor s .usdz je nekomprimovaný a nešifrovaný ZIP archiv pro souborový formát [USD](/cs/3d/usd/) (Universal Scene Description), který obsahuje a proxy soubory jiných formátů (jako jsou textury a animace) vložené do archiv a spouští je přímo s běhovým časem USD bez nutnosti rozbalování. Soubory USDZ jsou balíčky, jejichž design je založen na nové abstrakci balíčku na úrovni Ar. Usdz byl registrován u IANA a má název typu média modelu a název podtypu vnd.usd+zip a jeho podrobnosti lze nalézt na [registrační stránce IANA](https://www.iana.org/assignments/media-types/model/vnd.usdz+zip).

## Formát souboru USDZ

Soubory USDZ jsou založeny na formátu souboru ZIP, který archivuje jednotlivé soubory ve svém kontejneru. To umožňuje koncovému přijímači pouze rozbalit obsah a použít normální soubory popisu scén USD pro práci a kontrolu. Téměř všechny operační systémy poskytují integrovanou podporu pro formáty souborů ZIP a výběr tohoto formátu archivace před jakoukoli vlastní metodou usnadňuje, aby soubory USDZ byly užitečné jako jednoduchý přenosový protokol.

### Omezení ZIP

Formát souboru USDZ používá formát souboru ZIP bez jakékoli „komprese“ a „šifrování“. To bylo navrženo tak, aby splnilo dva požadavky:

* Pro balíček, který je již načten do paměti nebo jako jeden soubor na disku, je API dostupné v USD pro přístup k datům obsaženým v obrázku
* Nemělo by být potřeba extrahovat soubory na disk nebo přidělovat více úložného prostoru

S USDZ jsou oba tyto požadavky splněny, protože většina obrazových formátů sama o sobě umožňuje interní kompresní schémata, což vede ke kompaktní velikosti souboru.

### Požadavky na rozvržení

Balíčky USDZ vyžadují rozložení souborů v balíčku tak, že data pro každý soubor by měla začínat na násobku 64 bajtů od začátku balíčku. Balíček by však měl začínat nativním [USD](/cs/3d/usd/) souborem v případě cílení na balíček pomocí jednoduchého odkazu. V takovém případě je tento první soubor USD označován jako výchozí vrstva. Klienti, kteří chtějí dodávat „streamovatelný obsah“, mohou také zvážit další omezení rozvržení.

## Soubor USDZ ke stažení
Vzhledem k tomu, že soubory usdz jsou nabité dalšími vysoce kvalitními obrázky a soubory usd, mohou zabírat více místa na disku. Zde můžete najít jednoduchý a menší ukázkový soubor USDZ ke stažení:

- [Sample.usdz](../sample.usdz)

## Reference

* [Specifikace formátu souboru USDZ](https://openusd.org/release/spec_usdz.html)
