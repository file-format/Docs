{
  "date" : "2019-10-11",
  "keywords" :["xhtml", "Soubor", "Rozšíření", "Formát souboru", "Přípona souboru", "rozšiřitelné html"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XHTML - Formát souboru Extensible Hypertext Markup Language",
  "description":"Zjistěte, co je formát souboru XHTML a rozhraní API, která mohou vytvářet a otevírat soubory XHTML.",
  "linktitle" : "XHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor XHTML?

XHTML je textový formát souboru se značkami v XML, využívající přeformulování HTML 4.0. Tyto soubory jsou vhodné k otevření nebo prohlížení ve webovém prohlížeči. XHTML byl navržen tak, aby byl strukturovanější, méně skriptovací, obecný; pomocí všech existujících možností XML a více nezávislých na zařízení. XHTML poskytuje obecně užitečnou sadu prvků a atributů s možnostmi rozšíření v kombinaci se styly. Atributy se používají z kolekce atributů metadat. XHTML poskytuje flexibilitu a dostupnost tím, že podřizuje všechny **[HTML](/cs/web/html/)** prezentační prvky šablonám stylů. Styly jsou všestrannější než tyto prezentační prvky. Specifikace pro HTML 4.01, HTML5 a XHTML dynamicky vyvíjí World Wide Web Consortium (W3C).

## Stručná historie formátu souboru XHTML

Historie XHTML začíná návrhem dokumentu vydaným v prosinci 1998 World Wide Web Consortium. Tento dokument odkazuje na "Přeformulování HTML v XML", specifikaci nazvanou XHTML 1.0. Tato nová specifikace přeformulovala HTML v XML pomocí existujících prvků nebo atributů. V květnu 1999 konsorcium W3 prohlásilo, že HTML 4.0 bylo přeformováno na XML aplikaci. tedy XHTML. 26. ledna 2000 byla W3C vydána první specifikace, která definuje XHTML 1.0. Dále 31. května 2001 W3C oznámilo XHTML jako nezávislý jazyk a začalo pracovat na vývoji HTML 5.0. V roce 2005 však vznikla pracovní skupina (WHATWG), která měla za cíl vylepšit běžné HTML nezávislé na XHTML. WHATWG nakonec začalo pracovat na HTML5 souběžně s XHTML 2.

## Formát souboru XHTML

XHTML je formát, který je sbírkou různých typů dokumentů a modulů, které napodobují, kategorizují a rozšiřují HTML 4. Soubory v XHTML jsou založeny na XML a jejich cílem je pracovat s uživatelskými agenty založenými na XML. Soubory XHTML jsou kompatibilní s XML. K prohlížení, úpravám a ověřování souborů XHTML se používají standardní nástroje XML. Aplikace závislé na HTML Document Object Model nebo XML Document Object Model [DOM] mohou pracovat prostřednictvím XHTML dokumentů. Pokud si dnes zvolí XHTML, mohou vývojáři obsahu využívat všechny související výhody XML, aniž by se museli starat o dopřednou nebo zpětnou kompatibilitu svého obsahu.

Sada souvisejících prvků vytváří modul v XHTML. Modul formuláře nebo tabulky může obsahovat různé prvky formuláře nebo tabulky, které lze zobrazit na webové stránce. Cílem modularizace bylo izolovat prvky HTML do sad mnoha propojených prvků. Aby vývojáři obsahu mohli využít výhod výběru modulů pro různé typy zařízení. Kromě toho moduly umožňují uživatelským agentům vybírat prvky bez ztráty konzistence se standardem XHTML. Požadavky na analýzu XHTML jsou stejné jako XML, zatímco HTML praktikuje své vlastní.

### Soulad dokumentu

XHTML2 nabízí specifikace odpovídající dokumentům XHTML 1.0, které využívají prvky a atributy jmenných prostorů z XML a XHTML 1.0. Shoda dokumentu je dvou typů.

Přísně vyhovující dokument je založen na XML, který potřebuje pouze povinné služby definované v této specifikaci. Pro soubory XHTML musí být splněna následující kritéria:

* Soubor musí odpovídat omezením definovaným v DTD a v příloze B.
* Základním prvkem souboru musí být html.
* Základní prvek souboru musí obsahovat deklaraci pro jmenný prostor XHTML a měl by být definován jako:

```
http://www.w3.org/1999/xhtml.
```

* Základní prvek může být zapsán jako:

```
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
```

Dříve než základní prvek musí být deklarován DOCTYPE, jehož veřejný identifikátor musí odkazovat na jednu ze tří definic typu dokumentu (DTD). Systémový identifikátor může být upraven tak, aby vyhovoval současným systémovým konvencím.

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">
```

V dokumentech XML není nutné specifikovat deklarace XML ve všech dokumentech; vývojáři obsahu jsou však lákáni k používání deklarací XML ve všech svých dokumentech XHTML. Tyto deklarace jsou povinné buď v případě, že kódování znaků dokumentu je odlišné od UTF-8 /16, nebo nebylo žádné kódování specifikováno řídícím protokolem. Následující příklad dokumentu XHTML definuje deklarace XML

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

Vyhovující uživatelský agent musí splňovat následující pravidla:

* Parsování a vyhodnocování XHTML dokumentu provádí uživatelský agent, který zajišťuje jeho konzistenci s doporučením XML 1.0.
* V případě ověřování uživatelského agenta musí zkontrolovat platnost dokumentů pro jejich odkazované DTD podle XML. Když je soubor XHTML zpracován uživatelským agentem jako generický XML, budou vlastnosti typu ID uznány jako identifikátory fragmentů.

Pokud uživatelský agent narazí na nerozpoznaný prvek, musí splnit následující povinná kritéria

* zpracovat obsah tohoto neznámého prvku
* ignorujte atribut a jeho hodnotu
* Použijte hodnotu poskytnutého atributu jako výchozí.

Když uživatelský agent narazí na deklaraci reference entity, která nebyla dříve zpracována, měla by být zpracována jako znaky (začínající znakem „&“ a končící středníkem). Během zpracování obsahu mohou znaky nebo odkazy na znakové entity, které jsou předvídatelné uživatelským agentem, ale nerenderovatelné, používat jakékoli alternativní vykreslování, které poskytuje podobný význam. V takovém případě musí být dokument zobrazen tak, aby bylo uživateli zřejmé, že proces vykreslování neproběhl normálně. Pro zpracování bílých znaků musí uživatelský agent hledat definici ze znaků CSS [CSS2].

## XHTML Zpětná kompatibilita

Zpětná kompatibilita dokumentů XHTML 1. je dobře obeznámena s uživatelskými agenty HTML 4, pokud jsou dodržována správná pravidla. XHTML 1.1 je plně kompatibilní s výjimkou rubínových anotací, i když je prohlížeče HTML 4 obecně ignorují. XHTML 2.0 je poměrně méně kompatibilní, nicméně problém byl do určité míry vyřešen použitím skriptování.

## Reference

* [Historie XHTML: Od 90. let do dneška](https://www.brighthub.com/internet/web-development/articles/109224.aspx)

