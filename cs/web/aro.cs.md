{
  "date" : "2021-12-09",
  "keywords" :[ "aro", "soubor .aro", "formát souboru aro", "typ souboru", "soubor", "typ", "co je soubor .aro" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru ARO - soubor webové aplikace SteelArrow",
  "description" :"Zjistěte, co je soubor ARO a rozhraní API, která mohou vytvářet a otevírat soubory ARO.",
  "linktitle" : "ARO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## Co je soubor ARO?

Soubor ARO je soubor webové stránky na straně serveru, který se generuje pomocí webové aplikace SteelArrow. Obsahuje [HTML](/cs/web/html/) a SteelArrow tagy a skripty. Ty se spouštějí na serveru, aby se vygenerovala stránka s kompletní odpovědí před odesláním do prohlížeče uživatele. Soubory ARO obsahují téměř 95 % obsahu HTML, zatímco zbytek tvoří kód SteelArrow. Aby soubory ARO fungovaly za vás, měl by být server SteelArrow Web Applications nainstalován a spuštěn na počítači webového serveru.

## Formát souboru ARO

Soubory ARO jsou napsány v souboru značkovacího jazyka HTML s vloženým kódem JavaScript a aplety Java. [Značky SteelArrow](http://www.steelarrow.com/docs/basics1.aro) jsou základními stavebními kameny pro vývoj webových stránek. Ačkoli tyto nemění zobrazení stránky, používají se k vyplnění stránky daty. Kromě toho mohou být také použity pro řízení výstupu pomocí podmíněných příkazů.

### Příklad značky ARO

The<SAOUTPUT> Tag ARO umožňuje vývojářům vydávat datové hodnoty na libovolném místě ve skriptu. Lze jej například použít k získání výstupu z tabulky PARAM<SAOUTPUT VALUE=PARAM[]> které lze zobrazit v HTML<BODY> štítek.

## Reference

* [štítky SteelArrow](http://www.steelarrow.com/docs/basics.aro)

