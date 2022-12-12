{
  "date" : "2019-10-11",
  "keywords" :[ "soubor gbr", "formát souboru gbr", "co je soubor gbr", "soubor", "příklad gbr", "přípona souboru gbr", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru GBR - Formát souboru Gerber pro PCB",
  "description":"Další informace o formátu souborů GBR a rozhraních API, která mohou vytvářet a otevírat soubory GBR.",
  "linktitle" : "GBR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor GBR?

Soubor s příponou .gbr je obrázkový formát Gerber pro výměnu dat návrhu desky plošných spojů (PCB). Byl vyvinut společností Ucamco. Návrhová data PCB jsou hlavní komponentou vyžadovanou výrobním průmyslem pro manipulaci. Soubor GRB obsahuje data PCB, jako jsou vrstvy mědi, pájecí maska, legenda a data vrtání a trasy. Lze jej použít k přenosu dat, jako jsou charakteristiky výroby DPS včetně tloušťky nebo povrchové úpravy ve standardizovaném formátu. Všechny systémy návrhu DPS vydávají soubory Gerber, které mohou být zpracovány systémy výroby DPS. Soubory GBR se nyní staly de facto standardem pro přenos dat návrhu desek s plošnými spoji (PCB). Společnost Ucamco poskytla [bezplatný online prohlížeč](https://gerber-viewer.ucamco.com/) pro otevírání a prohlížení formátů souborů GBR.

## Formát souboru GBR

GBR je formát UTF-8 čitelný pro člověka, který se skládá z pouhých 27 příkazů. Díky tomuto krátkému seznamu příkazů a jeho kompaktnosti lze GBR snadno ladit. Gerber je ve svém jádru otevřený vektorový formát pro 2D binární obrázky. Metainformace jsou přenášeny s obrázky pomocí atributů. Jeden soubor GRB určuje jeden obrázek a nevyžaduje žádné doprovodné soubory nebo externí parametry k interpretaci. Jeden obrázek potřebuje pouze jeden soubor. Používá 7bitové znaky ASCII pro všechny příkazy a názvy definované ve specifikaci, které lze tisknout. To plně pokrývá kompletní generování obrazu.

### Příklad souboru GBR

Následuje příklad souboru Gerber, který vytváří kružnici o průměru 1,5 mm se středem v počátku. Na každý řádek je jeden příkaz.

```
%FSLAX26Y26*%
%MOMM*%
%ADD   100C,1.5*%
D100* X0Y0D03*
M02*
```

## Reference

* [Formát Gerber](https://www.ucamco.com/en/gerber)

