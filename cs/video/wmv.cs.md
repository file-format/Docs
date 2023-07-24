{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru WMV",
  "description":"Další informace o formátu souborů WMV a rozhraních API, která mohou vytvářet a otevírat soubory WMV.",
  "linktitle" : "WMV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-16"
}

## Co je soubor WMV?

Advanced Systems Format (ASF) je digitální multimediální kontejner určený především pro ukládání a přenos mediálních toků. Microsoft Windows Media Video (WMV) je komprimovaný formát videa a Microsoft Windows Media Audio (WMA) je komprimovaný zvukový formát spolu s dalšími metadaty v kontejneru ASF vyvinutém společností Microsoft. Jakmile jsou soubory WMV nebo WMA zakódovány kodeky Windows Media Video a Windows Media Audio, jsou reprezentovány příponou .asf. WMV komprimuje velké soubory pro lepší přenosovou rychlost po síti při zachování kvality videa. WMV je speciálně navržen tak, aby běžel na všech zařízeních se systémem Windows. Po standardizaci Společností filmových a televizních inženýrů (SMPTE) je nyní WMV považován za otevřený standardní formát.

## Dějiny ##

S pomocí proprietárních kodeků společnosti Microsoft byl v roce 1999 vyvinut nový komprimovaný video formát známý jako WMV7, který byl založen na MPEG-4 Part 2. Vylepšení byla přidána v dalších dvou verzích, tj. WMV8 a 9. Microsoft předložil 9^^th^^ verzi WMV na SMPTE pro standardizaci v roce 2003, který byl nakonec standardizován v roce 2006 jako SMPTE 421M také známý jako VC-1. Myšlenkou WMV bylo vyvinout formát médií, který by mohl podporovat veškerý hardware a software podporovaný společností Microsoft. Dalším hlavním účelem bylo dále přenášet video streamy přes internet v optimálním scénáři. Po standardizaci od SMPTE se WMV stal také video formátem pro Blu-ray disky.

## Specifikace formátu souboru

### Kontejner

Obecně je WMV zabaleno do ASF kontejneru, ale kromě toho jej může podporovat i kontejner Matroska nebo AVI s příponami .mkv a .avi.

### Windows Media Video 9

Ačkoli jsou v řadě Windows Media Video 9 k dispozici různé zvukové a video kodeky pro vytváření a přehrávání digitálních médií, kodek WMV-9 je nejnovější a nejlepší video kodek, protože dokáže dosáhnout optimální komprese od velmi nízkých bitových rychlostí, tj. 160 x 120 při 10 Kbps až 1920 x 1080 při 4-8 Mbps pro různé HD videa.

### Struktura kodeku

WMV-9 má 8bitový vnitřní barevný formát 4:2:0. Stejně jako všechny ostatní populární standardy pro kompresi videa MPEG-1 a H.261, WMV-9 používá blokovou kompenzaci pohybu a schéma prostorové transformace. Obecně lze říci, že tyto standardy provádějí kompenzaci pohybu blok po bloku z předchozího rekonstruovaného snímku pomocí 2-D veličiny nazývané vektor pohybu (MV) pro signalizaci prostorového posunutí. Aktuální blok je tvořen pomocí predikce hodnot ze stejně velkého předchozího rekonstruovaného snímku, který je posunutý z aktuální polohy vektorem pohybu. Nakonec se zbytková chyba vypočítá jako rozdíl mezi pohybově kompenzovaným predikovaným blokem a skutečným blokem. Tato zbytková chyba je transformována pomocí lineární transformace zhutňování energie, poté kvantována a entropicky kódována.

Kvantované transformační koeficienty jsou entropicky dekódovány, dekvantizovány a inverzně transformovány, aby se vytvořila aproximace zbytkové chyby na straně dekodéru, která je pak přidána k pohybově kompenzované predikci pro generování rekonstrukce. Popis kodeku na vysoké úrovni je zobrazen na následujícím obrázku.

Zbytek sekce bude diskutovat o nových vylepšeních ve WMV-9, která jej odlišují od ostatních řešení kódování videa, jako jsou standardy MPEG. WMV-9 má intra (I), predikované (P) a obousměrně predikované (B) snímky. Intra rámce jsou ty, které jsou kódovány nezávisle a nejsou závislé na jiných rámcích. Predikované snímky jsou snímky, které závisí na jednom snímku v minulosti. Dekódování predikovaného snímku může nastat pouze poté, co byly dekódovány všechny referenční snímky před aktuálním snímkem počínaje posledním (I) snímkem. B snímky jsou snímky, které mají dva odkazy – jeden v časové minulosti a jeden v časové budoucnosti. B rámce jsou vysílány následně po jejich odkazech, což znamená, že B rámce jsou odesílány mimo pořadí, aby bylo zajištěno, že jejich reference jsou dostupné v době dekódování. B snímky ve WMV-9 se nepoužívají jako reference pro následující snímky. To umístí snímky B mimo dekódovací smyčku, což umožňuje použití zkratek během dekódování snímků B bez posunu nebo dlouhodobých vizuálních artefaktů. Výše uvedená definice snímků I, P a B platí pro progresivní i prokládané sekvence.

Výkon video kodeků se porovnává s jejich grafem zkreslení rychlosti (RD). Je to 2-D křivka, která ukazuje zkreslení způsobené kompresí při určitém datovém toku.

WMV-9 vyřešil tento problém zavedením různých technik uvedených níže:

1. Adaptivní transformace velikosti bloku

2. Transformační sada s omezenou přesností

3. Kompenzace pohybu

4. Kvantování a dekvantizace

5. Pokročilé entropické kódování

6. Smyčkové filtrování

7. Pokročilé kódování snímku B

8. Prokládané kódování

9. Vyhlazení překrytí

10. Nízkorychlostní nástroje

11. Kompenzace blednutí

## Reference ##

* [https://bytescout.com/blog/2014/10/windows-media-video-format.html](https://bytescout.com/blog/2014/10/windows-media-video-format.html )
* [https://en.wikipedia.org/wiki/Windows_Media_Video](https://en.wikipedia.org/wiki/Windows_Media_Video)


