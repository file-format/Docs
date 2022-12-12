{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFT - soubor šablony e-mailu aplikace Microsoft Outlook",
  "description":"Další informace o formátu souborů OFT a rozhraních API, která mohou vytvářet a otevírat soubory OFT.",
  "linktitle" : "OFT",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor OFT?

Soubory s příponou .oft jsou soubory šablon, které jsou vytvořeny pomocí aplikace Microsoft Outlook. Předformátovaná sada rozvržení pro šablony zpráv se pak používá k odesílání e-mailů s běžnými informacemi, aby se ušetřil čas. Takové soubory lze vygenerovat vytvořením nového e-mailu, přidáním nezbytných informací a poté pomocí rozevíracího seznamu Uložit jako šablonu Office (.oft) z aplikace Microsoft Outlook. Uživatelé mohou otevřít soubory OFT dvojitým kliknutím na soubor a otevře se v přidružené aplikaci na konkrétním systému.

## Struktura souboru OFT ##

Formát souboru .OFT používá ve své podstatě souborový formát [MSG](/cs/email/msg/). Jediný rozdíl je v tom, že soubory OFT mají třídu úložiště CLSID_TemplateMessage ({0006F046-0000-0000-C000-000000000046}) (WriteClassStg), zatímco soubory MSG používají CLSID_MailMessage (00020D0B-00000000000000000000000000000).

Formát CFB_3 je základem souboru MSG. Paradigma je založeno na konceptech úložišť a streamů, které jsou velmi blízké adresářům a souborům. Proto je hlavním rozdílem v prvním případě celá hierarchie zabalená do samostatného souboru, který se nazývá složený soubor. Objekty tvoří soubory zpráv a skládají se z jedné vlastnosti nebo jejích kolekcí. Tato schopnost usnadňuje aplikacím ukládat složitá, strukturovaná data do jediného souboru. Tento formát také specifikuje více úložišť, přičemž každé úložiště představuje objekt Message jako hlavní komponentu. Tato úložiště obsahují řadu proudů představujících vlastnost dané komponenty. Vnořování úložného prostoru je také možné.

### Vlastnosti OFT

Na nejvyšší úrovni souboru .msg obsahují úložiště datové proudy, které v nich ukládají vlastnosti. Vlastnosti lze kategorizovat následovně:

* Vlastnosti pevné délky
* Vlastnosti proměnné délky
* Vlastnosti s více hodnotami

Bez ohledu na kategorii je vlastnost buď označená, nebo pojmenovaná. Pro pojmenované vlastnosti jsou však vyžadovány vhodné informace o mapování, jak je určeno jejich úložištěm mapování.

### OFT úložiště

Úložiště tvoří klíčové součásti objektu Message. Formát souboru MSG uvádí následující úložiště:

### Struktura nejvyšší úrovně

Objekt Message představuje celou nejvyšší úroveň formátu souboru Msg. V závislosti na typu, vlastnostech, počtu příjemců a objektů Attachment může mít objekt zprávy různá úložiště datového proudu v odpovídajícím souboru .MSG.

#### Vztah s jinými strukturami

Formát souboru MSG/OFT má k jiným strukturám následující vztahy:

* Základem .msg je Binární formát souboru Compound File.
* Tento formát používá vlastnosti používané protokolem Message and Attachment Object Protocol.

## Reference

* [[MS-OXMSG]: Formát souboru MSG Outlook](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

