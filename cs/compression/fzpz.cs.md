{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru FZPZ - soubor Fritzing Part",
  "description":"Zjistěte, co je soubor FZPZ a rozhraní API, která mohou vytvářet a otevírat soubory FZPZ.",
  "linktitle" : "FZPZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-20"
}

## Co je soubor FZPZ?

Soubor FZPZ je součást/část používaná v návrhu elektronických obvodů vytvořená pomocí aplikace prototypování a návrhu obvodů **Fritzing**. Jedná se o komprimovaný archiv, který obsahuje soubor [FZP](/cs/cad/fzp/) a čtyři obrázky [SVG](/cs/image/svg/) popisující celkovou část Fritzingu. Výhodou použití těchto souborů je, že uživatelé mohou s každým sdílet své soubory FZPZ z hlediska opětovné použitelnosti. Sdílení dílů FZPZ pomáhá při integraci částí obvodů pro rychlé vytváření větších návrhů PCB.

## Formát souboru FZPZ - Další informace

Soubory FZPZ se ukládají na disk jako komprimované archivy [ZIP](/cs/compression/zip/). Příponu můžete přejmenovat z .fzpz na .zip a pomocí libovolného standardního dekompresního nástroje, jako je WinZIP, extrahovat soubory z archivu.

### Informace o struktuře souboru FZPZ

Jak již bylo zmíněno, soubor FZPZ je archivní soubor, který obsahuje vícenásobné soubory pro reprezentaci součásti použité na desce plošných spojů. FZPZ obsahuje následující soubory:

* `Čtyři soubory SVG` - které představují prkénko, schéma, PCB a obrázky ikon
* `Soubor FZP` – Soubor XML, který obsahuje informace o vlastnostech součásti, konektorech a sběrnicích

Soubory jsou obvykle pojmenovány následovně.

* část.soubor.fzp
* svg.breadboard.file.svg
* svg.icon.file.svg
* svg.pbc.file.svg
* svg.schematic.file.svg

## Reference ##

* [Nové díly s rozšířením fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

