{
  "date" : "2021-08-10",
  "keywords" :[ "soubor .ovf", "formát souboru", "co je soubor .ovf", "soubor", "přípona souboru"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Zjistěte, co je formát souboru .ovf a rozhraní API, která mohou vytvářet a otevírat soubory OVF.",
  "title" :"Formát souboru OVF - Otevřít soubor virtualizace",
  "linktitle" : "OVF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## Co je soubor OVF?

Soubor OVF je textový soubor, který obsahuje informace o balení a distribuci softwaru, který běží na virtuálním počítači. Je naformátován podle [Open Virtualization Standard Specifications] (https://www.dmtf.org/standards/ovf), který popisuje všechny požadavky (jako je zabezpečení, přenositelnost, efektivita a rozšiřitelnost) pro spouštění aplikací na virtuálních strojích. Mezinárodní organizace pro normalizaci (ISO) přijala OVF jako normu ISO 17203.

## Stručná historie formátu souborů OVF

Formát souboru OVF byl představen organizací DMTF (Distributed Management Task Force), která vytváří otevřené standardy správy. Je nezávislý na jakémkoli konkrétním hypervizoru nebo architektuře instrukční sady. Balíček OVF obsahuje jeden nebo více virtuálních systémů, z nichž každý lze nasadit na virtuální stroj.

## Formát souboru OVF - Další informace

Balíček OVF se skládá z více souborů umístěných v jednom adresáři. Mezi nimi obsahuje právě jeden soubor deskriptoru OVF (s příponou .ovf), který je uložen ve formátu souboru [XML](/cs/web/xml/). Popisuje zabalené informace o virtuálním stroji a informace o metadatech o balíčku OVF, jako jsou:

* název
* hardwarové požadavky
* odkazy na další soubory v balíčku OVF a
* Lidsky čitelné popisy

Další soubory, které lze nalézt v balíčku OVF, zahrnují jeden nebo více obrazů disku a volitelně soubory certifikátů a další pomocné soubory.

## Reference

* [Otevřený virtualizační formát – DMTF](https://www.dmtf.org/standards/ovf)
* [Specifikace formátu souboru OVF](https://www.dmtf.org/sites/default/files/standards/documents/DSP0243_1.1.0.pdf)

