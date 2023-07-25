{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EML - e-mailová zpráva",
  "description":"Další informace o formátu souborů EML a rozhraních API, která mohou vytvářet a otevírat soubory EML.",
  "linktitle" : "EML",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-16"
}

## Co je soubor EML?

Formát souboru EML představuje e-mailové zprávy uložené pomocí aplikace Outlook a dalších relevantních aplikací. Téměř všichni e-mailoví klienti podporují tento formát souboru pro jeho shodu s RFC-822 Internet Message Format Standard. Microsoft Outlook je výchozí software pro otevírání typů zpráv EML. Soubory EML lze použít k uložení na disk i k rozeslání příjemcům pomocí komunikačních protokolů.

## Stručná historie EML

Specifikace formátu souboru EML jsou k dispozici podle [RFC 822](https://www.ietf.org/rfc/rfc0822.txt) Standardní formát. Před RFC-822 řídil RFC-733 pravidla výměny síťových zpráv až do roku 1982, kdy byl první vytvořen jako vylepšení laterálních norem ARPA. Microsoft zároveň vytvořil vlastní COM moduly pro vývoj vlastního e-mailového klienta Outlook Express. RFC-822 se vydal cestou zavedení jako proprietární formát, když se Microsoft odchýlil od otevřeného standardu a vytvořil souborový formát [PST](/cs/email/pst/), kde jsou e-maily ukládány ve vysoce strukturovaném databázovém formátu. To vedlo k problémům pro uživatele e-mailových klientů jiných společností než Microsoft, když byly e-maily přeposílány z aplikace Microsoft Outlook.

Bylo to v roce 2001, kdy byl standard 822 rozšířen na 2822 - Internet Message Format, který se v současnosti používá pro vytváření, čtení a odesílání zpráv EML ve formátu MIME RFC-822.

## Specifikace formátu souborů EML

Soubory EML se skládají ze dvou odlišných částí:

* Hlavičky - Obsahuje informace o hlavičce zprávy
* Tělo zprávy – Obsahuje řadu informací, které mohou zahrnovat obsah zprávy, vložené obrázky a přílohy

### Informace o záhlaví ###

Soubor EML se skládá z informací záhlaví a volitelně z těla zprávy. Každý řádek záhlaví v EML má dvě části oddělené dvojtečkou ":". První se nazývá Název záhlaví a druhý za dvojtečkou je tělo záhlaví. Mezi taková záhlaví patří například:

* E-mailová adresa odesílatele
* E-mailová adresa příjemce
* Předmět e-mailu
* Čas a datum razítka zprávy

**Příklad záhlaví**

Z:<John@bmw.eml.light.com>

Na:<Andy@fileformat.com>

Datum: Čt, 8. března 2018 10:43:37 +0100

Předmět: bmw eml světlo

### Tělo zprávy ###

Tělo zprávy EML obsahuje primární informace e-mailu ve formě textu, hypertextových odkazů a příloh. Tělo e-mailu může obsahovat čistý čitelný text, ale není to nutné. V tomto případě může být tělo zprávy prázdné nebo může obsahovat zakódovaná data příloh.

Obsah těla zprávy je popsán pomocí Content-Type, který umožňuje čtecím aplikacím číst informace v příslušných formátech. Ve skutečnosti představuje povahu a formát dokumentu. Struktura typu MIME nebo typu obsahu je velmi jednoduchá; skládá se z typu a podtypu, dvou řetězců oddělených '/'. Není povolen žádný prostor. "Typ" představuje kategorii a může být diskrétní nebo vícedílný typ. "Podtyp" je specifický pro každý typ. Seznam typů, které spadají do kategorie Content-Type, je dlouhý, ale některé důležité typy obsahu jsou následující:


|**Typ**|**Popis**|**Příklad podtypů**
---|---|---|
|text|Představuje formát, který je čitelný pro člověka|text/prostý, text/html, text/css, text/javascript
|image|Představuje obrázek jakéhokoli typu kromě videí|image/bmp, image/png, image/jpg, image/gif
|audio|Představuje jakýkoli formát zvukového souboru|audio/mdi, audio/wav
|application|Reprezentuje jakýkoli druh binárních dat|application/octet-stream, application/vnd.mspowerpoint, application/xhtml+xml, application/xml, application/pdf

### Reprezentace přílohy v těle EML ###

Tělo EML obsahuje hranice pro každý typ obsahu, který obsahuje. Příloha v těle zprávy je identifikována podle typu Content-Type a Content-Disposition, jak ukazuje následující příklad:

Content-Type: text/plain; charset#"windows-1252"; name#"apple app store.txt"
Obsah-Dispozice: příloha; filename#"apple app store.txt"
Content-Transfer-Encoding: base64
X-Attachment-Id: f_jkhztmd02

Jak je vidět, nastavení Content-Disposition na přílohu umožňuje čtecím aplikacím získat informace o příloze, jako je název souboru přílohy a kódování přenosu. Informace záhlaví přílohy je následována kódovaným obsahem přílohy, který se má číst.

#### Příklad tabulky jako přílohy ####

Content-Type: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet; name#"english_spodr.xlsx"
Obsah-Dispozice: příloha; název_souboru#"english_spodr.xlsx"
Content-Transfer-Encoding: base64
X-Attachment-Id: f_jkhztmd43

## Reference

* [RFC 822](https://www.ietf.org/rfc/rfc0822.txt)

