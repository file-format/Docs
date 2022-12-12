{
  "date" : "2019-10-11",
  "keywords" :[ "soubor j2c", "formát souboru j2c", "co je soubor j2c", "soubor", "příklad j2c", "přípona souboru j2c", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"J2C",
  "description":"Další informace o formátu souborů J2C a rozhraních API, která mohou vytvářet a otevírat soubory J2C.",
  "linktitle" : "J2C",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-14"
}

## Co je soubor J2C?

Soubor s příponou .j2c je variantou formátu souboru JPEG a je komprimován vlnkovou kompresí. Má téměř identický systém značek a segmentů jako souborový formát JPEG 2000. Formát souboru J2C je definován v části 1 stánku JPEG 2000, který podporuje ztrátovou i bezeztrátovou kompresi. Kódový tok JPEG 2000 byl navržen pro vložení do [JP2](/cs/image/jp2/) nebo jiného formátu souboru, i když se může objevit v souboru sám o sobě. Soubor J2C lze otevřít pomocí aplikací Adobe Photoshop 2020, Adobe Illustrator 2020 a Corel Paintshop Pro.

## Formát souboru J2C

Formát souboru J2C je stejný jako formát JPEG 2000, který se často ukládá jako .jp2 a .jpc. Díky tomu se soubory J2C řídí stejným přístupem kódování metadat ve formátu XML, kde se jako reference mezi tagy Exif a komponentami XML používá standard 12234-1. Dále je vylepšen o rozšíření JPEG 2000 part-2, které kombinuje animační mechanismus a konfigurace kódového toku do jednoho obrázku. Takové soubory rozšířeného formátu souborů se ukládají jako [.jpx](/cs/image/jpx/).

### Rozložení souboru JPEG2000

JPEG2000 podporuje různé aplikace založené na shodě pro rozšiřitelné formáty souborů. I když nejjednodušší typ může obsahovat jeden obrázek, složitější typy mohou zahrnovat sérii obrázků naskládaných na sebe nebo jsou časově sekvenované.

#### Box JP2
Je to stavební blok nejvyšší úrovně formátu souboru JP2 a obsahuje pole typu a délky v záhlaví a datový oddíl. Nejpozoruhodnějším typem boxu je souvislý box codestream. Tento box ukládá ve své datové části kódový tok JPEG2000.

#### JPEG2000 CodeStream

JPEG2000 CodeStream je sekvence bajtů, která je nutná k dekódování komprimovaného obrázku JPEG2000. V případě, že soubor nemá nic jiného než tento kódový proud, nazývá se soubor raw codestream. Kódový tok JPEG je obvykle aplikace kompresního algoritmu JPEG2000 na obrázek, i když to není jediný způsob.

#### Dlaždice ####

Obrázek zakódovaný ve formátu JPEG2000 je soubor datových jednotek nazývaných pakety. Tyto pakety jsou udržovány v kódovém toku uvnitř skupin paketů nazývaných tile-parts. Před zakódováním obrázku kodér rozdělí obrázek na obdélníkovou mřížku bloků, nazývanou dlaždice, kde je každá dlaždice kódována samostatně bez ohledu na ostatní dlaždice.

{{< figure src="../JPEG2000_Codestream.png" alt="Formát souboru JPEG2000" >}}

## Komprese J2C
JPEG 2000 využívá technologii komprese vlnek, díky čemuž je rychlý na základě skutečnosti, že v jakémkoli výřezu nebo okně, ve kterém prohlížeč zobrazuje obrázek, je zobrazeno relativně málo pixelů. To lze zdůraznit tím, že u velmi velkých obrázků (v gigabajtech) se na obrazovce objeví pouze několik megabajtů pixelů. To pomáhá rychle načíst a vykreslit pouze tu část obrazových dat, která je nutná k naplnění pixelů displeje. To také vyžaduje vysokorychlostní dekompresní technologii pro urychlení mechanismu načítání obrazu pro vytváření požadovaných snímků za chodu.

J2C využívá výhody rychlé dekomprese a načítá pouze nezbytné informace pro data pixelů pro rychlé vykreslení části viditelných obrázků na obrazovky. J2C je určen primárně k prohlížení dat a ne k jejich editaci.

## Identifikace J2C
Soubory JPEG 2000 mají podpisové bajty `FF 4F FF 51`.

### Typy pantomimy
Registrované typy Mime pro soubory JPEG 2000 zahrnují:
* obrázek/j2c
* obrázek/jpx
* obrázek/jpm
* video/mj2

## Vylepšení oproti standardu JPEG
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

