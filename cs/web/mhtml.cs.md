{
  "date" : "2019-10-11",
  "keywords" :[ "mhtml", "soubor mhtml", "formát souboru mhtml", "typ souboru mhtml", "soubor", "typ", "co je soubor mhtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHTML - MIME HTML soubor",
  "description":"Další informace o formátu souboru MHTML a rozhraních API, která mohou vytvářet a otevírat soubory MHTML.",
  "linktitle" : "MHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor MHTML?

Soubory s příponou MHTML představují formát archivu webových stránek, který může vytvářet řada různých aplikací. Tento formát je známý jako archivní formát, protože ukládá webový **[HTML](/cs/web/html/)** kód a související zdroje do jednoho souboru. Tyto zdroje zahrnují vše, co je spojeno s webovou stránkou, jako jsou obrázky, aplety, animace, zvukové soubory a tak dále. Soubory MHTML lze otevřít v různých aplikacích, jako je Internet Explorer a Microsoft Word. Microsoft Windows používá formát souboru MHTML pro záznam scénářů problémů pozorovaných během používání jakékoli aplikace v systému Windows, která vyvolává problémy. Formát souboru MHTML kóduje obsah stránky podobně jako specifikace definované ve zprávě/rfc822, což jsou specifikace týkající se e-mailu ve formátu prostého textu. Skutečné specifikace formátu jsou popsány v [RFC 2557](https://tools.ietf.org/html/rfc2557).

## Formát souboru MHTML

MHTML je také známé jako MIME Encapsulation of Aggregate HTML documents pro svou schopnost kódovat webové stránky HTML spolu se svými prostředky do jediného webového archivu. Podle specifikací RFC 2557 je souhrnný dokument zpráva zakódovaná v MIME, která obsahuje kořenový zdroj (objekt) a další zdroje s ním spojené prostřednictvím identifikátorů URI. Takovými dalšími zdroji mohou být reprezentace vložených obrázků, stylů, apletů atd. Kromě toho mohou být základem jiných multimediálních dokumentů. Úplné specifikace dokumentu pro formát souboru MHTML jsou popsány v [RFC 2557](https://tools.ietf.org/html/rfc2557) a měly by být uvedeny pro jakýkoli druh vývoje aplikací pro čtení/zápis tohoto formátu souboru. Norma specifikuje, že části těla, na které se má odkazovat, mohou být identifikovány buď pomocí Content-ID, nebo podle Content-Location.

### Záhlaví obsahu MIME

Záhlaví obsahu MIME, Content-Location, je definováno pro řešení odkazů URI na zdroje v jiných částech těla. Toto záhlaví se může vyskytovat v libovolném záhlaví zprávy nebo obsahu.

### Záhlaví obsahu-umístění

Content-Location je reprezentace URI, která označuje obsah části těla, kde je umístěn. Jeho hodnota může být absolutní nebo relativní URI. Lze jej použít k označení zdroje, který někteří nebo všichni příjemci zprávy nemohou získat. Jedna zpráva může mít pouze jednu hlavičku Content-Location. Příklad vícedílné/související struktury obsahující části těla se štítky Content-Location a Content-ID:

```
Content-Type: multipart/related; boundary#"boundary-example";
                    type#"text/html"

      --boundary-example

      Content-Type: text/html; charset#"US-ASCII"

      ... ... <IMG SRC#"fiction1/fiction2"> ... ...
      ... ... <IMG SRC#"cid:97116092811xyz@foo.bar.net"> ... ...

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092511xyz@foo.bar.net>
      Content-Location: fiction1/fiction2

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092811xyz@foo.bar.net>
      Content-Location: fiction1/fiction3

      --boundary-example--
```

### URI agregátů MHTML

URI agregátu MHTML se liší od jeho kořenového URI. Pole záhlaví Content-Location by se mělo vztahovat na celý souhrn, pokud je použito v záhlaví vícedílného/souvisejícího záhlaví. Podobně se sada zdrojů načtených může lišit od sady zdrojů získaných pomocí umístění obsahu jejích částí, když se k načtení tohoto agregátu použije URI odkazující na agregát MHTML. Například načtení agregace MHTML může vrátit starou verzi, zatímco načtení kořenového URI a jeho in-line propojených objektů může vrátit novější verzi.

## Reference

* [MIME Encapsulation of Aggregate Documents – RFC 2557](https://tools.ietf.org/html/rfc2557)
* [Formát souboru MHTML – podle Wikipedie](https://en.wikipedia.org/wiki/MHTML)

