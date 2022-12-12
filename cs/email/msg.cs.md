{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSG - Microsoft Outlook Email Format",
  "description":"Další informace o formátu souborů MSG a rozhraních API, která mohou vytvářet a otevírat soubory MSG.",
  "linktitle" : "MSG",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor MSG?

MSG je formát souboru používaný [Microsoft Outlook](https://products.office.com/en-us/outlook/email-and-calendar-software-microsoft-outlook?rtc#1) a Exchange k ukládání e-mailových zpráv , kontakt, schůzku nebo jiné úkoly. Takové zprávy mohou obsahovat jedno nebo více e-mailových polí s odesílatelem, příjemcem, předmětem, datem a tělem zprávy nebo kontaktními informacemi, podrobnostmi o schůzce a jednou nebo více specifikacemi úkolu. Vlastnosti, které tvoří objekt Message, včetně, jsou také součástí souboru MSG. Soubor MSG má záhlaví, hlavní tělo zprávy a hypertextové odkazy jako prostý text ASCII. Soubory MSG jsou také vhodné s programy, které potřebují rozhraní MAPI (Messaging Applications Programming Interface) společnosti Microsoft.

## Struktura souborů MSG

Formát CFB_3 je základem souboru MSG. Paradigma je založeno na konceptech úložišť a streamů, které jsou velmi blízké adresářům a souborům. Proto je hlavním rozdílem v prvním případě celá hierarchie zabalená do samostatného souboru, který se nazývá složený soubor. Objekty tvoří soubory zpráv a skládají se z jedné vlastnosti nebo jejích kolekcí. Tato schopnost usnadňuje aplikacím ukládat složitá, strukturovaná data do jediného souboru. Tento formát také specifikuje více úložišť, přičemž každé úložiště představuje objekt Message jako hlavní komponentu. Tato úložiště obsahují řadu proudů představujících vlastnost dané komponenty. Vnořování úložného prostoru je také možné.

## Vlastnosti Mapi

Na nejvyšší úrovni souboru .msg obsahují úložiště datové proudy, které v nich ukládají vlastnosti. Vlastnosti lze kategorizovat následovně:

* Vlastnosti pevné délky
* Vlastnosti proměnné délky
* Vlastnosti s více hodnotami

Bez ohledu na kategorii je vlastnost buď označená, nebo pojmenovaná. Pro pojmenované vlastnosti jsou však vyžadovány vhodné informace o mapování, jak je určeno jejich úložištěm mapování.

## Úložiště

Úložiště tvoří klíčové součásti objektu Message. Formát souboru MSG uvádí následující úložiště:

## Struktura nejvyšší úrovně

Objekt zprávy představuje celou nejvyšší úroveň formátu souboru MSG. V závislosti na typu, vlastnostech, počtu příjemců a objektů Attachment může mít objekt zprávy různá úložiště datového proudu v odpovídajícím souboru .MSG.

### Vztah s jinými strukturami

Formát souboru Msg má k ostatním strukturám následující vztahy:

* Základem .msg je Binární formát souboru Compound File.
* Tento formát používá vlastnosti používané protokolem Message and Attachment Object Protocol.

## Scénáře, jak se vyhnout formátům MSG

Objekt zprávy lze sdílet mezi klienty nebo úložišti zpráv, které používají systém souborů .msg. Existuje několik okolností, za kterých by uložení objektu Message ve formátu souboru .msg nebylo vhodné. Například:

* V případě zachování velkého samostatného archivu je lepší použít plnohodnotný formát, ve kterém lze pohledy vykreslovat přesněji.
* Pokud je příjemce neznámý, je možné, že formát není podporován příjemcem a může být doručen soukromý nebo irelevantní.

## Příklad souboru MSG

Chcete-li si udělat představu, jak soubor MSG vypadá, můžete si stáhnout [ukázkový soubor MSG](https://products.conholdate.app/viewer/view/mL7cmq6qYbcNG329P/sample-msg-file.msg) a otevřít jej na počítače, abyste si mohli prohlédnout jeho obsah.

## Reference

* [[MS-OXMSG]: Formát souboru MSG Outlook](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

