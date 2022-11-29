{
  "date" : "2019-10-11",
  "keywords" :[ "mhtml","mhtml-fil", "mhtml-filformat", "mhtml-filtyp", "fil", "typ", "vad är en mhtml-fil" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHTML - MIME HTML-fil",
  "description":"Läs mer om MHTML-filformat och API:er som kan skapa och öppna MHTML-filer.",
  "linktitle" : "MHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en MHTML-fil?

Filer med MHTML-tillägg representerar ett webbsidearkivformat som kan skapas av ett antal olika applikationer. Formatet är känt som arkivformat eftersom det sparar webbens **[HTML](/sv/web/html/)**-kod och tillhörande resurser i en enda fil. Dessa resurser inkluderar allt som är länkat till webbsidan som bilder, appletar, animationer, ljudfiler och så vidare. MHTML-filer kan öppnas i en mängd olika applikationer som Internet Explorer och Microsoft Word. Microsoft Windows använder MHTML-filformat för att registrera scenarier med problem som observerats under användningen av alla program på Windows som väcker problem. MHTML-filformatet kodar sidinnehållet som liknar specifikationer som definieras i message/rfc822, vilket är e-postrelaterade specifikationer i vanlig text. De faktiska specifikationerna för formatet är enligt [RFC 2557](https://tools.ietf.org/html/rfc2557).

## MHTML filformat

MHTML är också känt som MIME Encapsulation of Aggregate HTML-dokument för dess förmåga att koda HTML-webbsidor tillsammans med dess resurser till ett enda webbarkiv. Enligt RFC 2557-specifikationerna är ett aggregerat dokument ett MIME-kodat meddelande som innehåller en rotresurs (objekt) såväl som andra resurser kopplade till den via URI:er. Sådana andra resurser kan vara representation av inline-bilder, stilmallar, applets, etc. Dessutom kan dessa vara roten till andra multimediadokument. Fullständiga dokumentspecifikationer för MHTML-filformat finns som beskrivs i [RFC 2557](https://tools.ietf.org/html/rfc2557) och bör hänvisas till alla typer av applikationsutveckling för läsning/skrivning av detta filformat. Standarden specificerar att de kroppsdelar som ska refereras kan identifieras antingen med ett Content-ID eller med en Content-Location.

### MIME-innehållsrubriker

En MIME-innehållsrubrik, Content-Location, definieras för att lösa URI-referenser till resurser i andra kroppsdelar. Denna rubrik kan förekomma i alla meddelande- eller innehållsrubriker.

### Content-Location Header

En Content-Location är en representation av en URI som märker innehållet i en kroppsdel där den är placerad. Dess värde kan vara en absolut eller en relativ URI. Den kan användas för att märka en resurs som inte kan hämtas av några eller alla mottagare av ett meddelande. Ett enda meddelande tillåts endast ha en enda Content-Location-rubrik. Exempel på en struktur med flera delar/relaterad struktur som innehåller kroppsdelar med både Content-Location och Content-ID-etiketter:

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

### URI:er för MHTML-aggregat

URI:n för MHTML-aggregatet skiljer sig från dess rot-URI. Rubrikfältet Content-Location bör gälla för hela aggregatet om det används i rubriken för en flerdelad/relaterad rubrik. På liknande sätt kan uppsättningen av hämtade resurser skilja sig från uppsättningen av resurser som hämtas med hjälp av innehållsplatserna för dess delar när URI:n som hänvisar till MHTML-aggregatet används för att hämta detta aggregat. Till exempel kan hämtning av ett MHTML-aggregat returnera en gammal version, medan hämtning av rot-URI och dess in-line länkade objekt kan returnera en nyare version.

## Referenser

* [MIME Encapsulation of Aggregate Documents - RFC 2557](https://tools.ietf.org/html/rfc2557)
* [MHTML-filformat - av Wikipedia](https://en.wikipedia.org/wiki/MHTML)

