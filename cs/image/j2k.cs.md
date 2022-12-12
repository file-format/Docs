{
  "date" : "2019-10-11",
  "keywords" :[ "soubor j2k", "formát souboru j2k", "co je soubor j2k", "soubor", "příklad j2k", "přípona souboru j2k", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"J2K",
  "description":"Další informace o formátu souborů J2K a rozhraních API, která mohou vytvářet a otevírat soubory J2K.",
  "linktitle" : "J2K",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-03"
}

## Co je soubor J2K?

Soubor **J2K** je obrázek, který je komprimován pomocí komprese wavelet namísto komprese DCT. Tento formát souboru používá skupina JPEG (Joint Photographic Experts Group) 2000. Soubory J2K ukládají metadata o obrazovém souboru v XML na rozdíl od .jpeg nebo .jpg, které pro tento účel používají formát EXIF. Soubory J2K podporují 15bitové barvy, průhlednost alfa a bezeztrátovou kompresi. Existuje několik komerčních API pro dekódování obrázků JPEG 2000, jako je J2K-Codec. Soubor J2K lze otevřít v operačním systému Windows pomocí standardních prohlížečů obrázků.

## Formát souboru J2K ##

Formát souboru J2K je stejný jako formát JPEG 2000, který se často ukládá jako .jp2 a .jpc. Díky tomu se soubory J2K řídí stejným přístupem kódování metadat ve formátu XML, kde se jako reference mezi tagy Exif a komponentami XML používá standard 12234-1. Dále je vylepšen o rozšíření JPEG 2000 part-2, které kombinuje animační mechanismus a konfigurace kódového toku do jednoho obrázku. Takové soubory rozšířeného formátu souborů se ukládají jako .jpx.

### Rozložení souboru JPEG2000 ###

JPEG2000 podporuje různé aplikace založené na shodě pro rozšiřitelné formáty souborů. I když nejjednodušší typ může obsahovat jeden obrázek, složitější typy mohou zahrnovat sérii obrázků naskládaných na sebe nebo jsou časově sekvenované.

#### JP2 Box ####
Je to stavební blok nejvyšší úrovně formátu souboru JP2 a obsahuje pole typu a délky v záhlaví a datový oddíl. Nejpozoruhodnějším typem boxu je souvislý box codestream. Tento box ukládá ve své datové části kódový tok JPEG2000.

#### JPEG2000 CodeStream ####

JPEG2000 CodeStream je sekvence bajtů, která je nutná k dekódování komprimovaného obrázku JPEG2000. V případě, že soubor nemá nic jiného než tento kódový proud, nazývá se soubor raw codestream. Kódový tok JPEG je obvykle aplikace kompresního algoritmu JPEG2000 na obrázek, i když to není jediný způsob.

#### Dlaždice ####

Obrázek zakódovaný ve formátu JPEG2000 je soubor datových jednotek nazývaných pakety. Tyto pakety jsou udržovány v kódovém toku uvnitř skupin paketů nazývaných tile-parts. Před zakódováním obrázku kodér rozdělí obrázek na obdélníkovou mřížku bloků, nazývanou dlaždice, kde je každá dlaždice kódována samostatně bez ohledu na ostatní dlaždice.

{{< figure src="../JPEG2000_Codestream.png" alt="Formát souboru JPEG2000" >}}

## J2K komprese ##
JPEG 2000 využívá technologii komprese vlnek, díky čemuž je rychlý na základě skutečnosti, že v jakémkoli výřezu nebo okně, ve kterém prohlížeč zobrazuje obrázek, je zobrazeno relativně málo pixelů. To lze zdůraznit tím, že u velmi velkých obrázků (v gigabajtech) se na obrazovce objeví pouze několik megabajtů pixelů. To pomáhá rychle načíst a vykreslit pouze tu část obrazových dat, která je nutná k naplnění pixelů displeje. To také vyžaduje vysokorychlostní dekompresní technologii pro urychlení mechanismu načítání obrazu pro vytváření požadovaných snímků za chodu.

J2K využívá výhody rychlé dekomprese a získává pouze nezbytné informace pro pixelová data pro rychlé vykreslení části viditelných obrázků na obrazovky. J2K je určen především pro prohlížení dat a ne pro jejich editaci.

## J2K Identifikační číslo ##
Soubory JPEG 2000 mají podpisové bajty 6A 50 20 20.

### Typy mime ###
Registrované typy Mime pro soubory JPEG 2000 zahrnují:
* obrázek/jp2
* obrázek/jpx
* obrázek/jpm
* video/mj2

## Vylepšení oproti standardu JPEG ##
Mezi vylepšení oproti standardu JPEG patří:
* Vynikající kompresní výkon
* Vícenásobné rozlišení reprezentace
* Progresivní přenos podle pixelů a přesnost rozlišení
* Volba bezztrátové nebo ztrátové komprese
* Odolnost proti chybám, flexibilní formát souboru
* Podpora vysokého dynamického rozsahu
* Prostorové informace postranního kanálu

## Reference ##
* [Taubman, David; Marcellin, Michael (2012)](https://books.google.com/books?id=y7HeBwAAQBAJ&pg=PA402)

