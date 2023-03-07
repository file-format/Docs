{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTACCESS-fil - Apache HTACCESS-filformat",
  "description" :"Din filformatguide för att lära dig vad en HTACCESS-fil är",
  "linktitle" : "HTACCESS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en HTACCESS fil?

En HTACCESS-fil är en Apache-konfigurationsfil som tillhandahåller en mekanism för att tillåta konfigurationsändringar för olika mappar/kataloger på en webbplats. Den innehåller konfigurationsdirektiv som är tillämpliga på katalogen och underkatalogerna.

En HTACCESS-fil utför ett antal kontroller som att definiera indexsidan för en webbplats, lista 404-felsidan (sidan hittades inte), utföra 301- eller 302-sidansomdirigeringar, blockera åtkomst från en specifik IP-adress eller andra webbplatser. Användningen av .htaccess-filer saktar därför ner den övergripande prestandan för din Apache [HTTP](/sv/web/html/)-server.

## HTACCESS filformat

HTACCESS-filer lagras på skiva i vanlig textfilformat. Det betyder att du kan öppna och redigera dessa filer i vilken textredigerare som helst. Det finns inget namn före "." i en .htaccess-fil, vilket visar att det är en dold fil i mappen.

## Vanliga användningsområden för en HTACCESS-fil

Fem vanliga användningsområden för en HTACCESS-fil är följande.

### Mod_Rewrite

En HTACCESS-fil kan användas för att ange och ändra hur URL:er och webbsidor på en webbplats visas för användarna.

### Autentisering

Autentisering kan uppnås med .htaccess genom att skapa en passowrd-fil som heter .htpasswd. Detta låter webbplatsbesökarna ange ett lösenord om de vill besöka en viss del av webbsidan.

### Anpassade felsidor

Du kan skapa anpassade felsidor som 400 Bad Request, 401 Authorization Required, 403 Forbidden Page, 404 File not Found och 500 Intern Error with .htaccess-fil. Dessa kommer dock att sakta ner serverns prestanda eftersom alla dessa kontroller kommer att utföras när sidorna öppnas.

### MIME-typer

Apache HTACCESS-filer kan modifieras så att de inkluderar MIME-typer (Multipurpose Internet Mail Extensions). Detta gör att din server kan stödja leverans av programfiler som inte stöddes av webbplatsen.

### SSI

Server Side Includes (SSI) fungerar som en stor tidsbesparare på en webbplats. SSI kan aktiveras genom att infoga följande kod i din .htaccess-fil.

```
AddType text/html .shtml
AddHandler server-parsed .shtml</pre>
```

## Exempel på Apache HTACCESS-fil

```
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

## Referenser

* [Apache HTTP Server Tutorial: .htaccess-filer](https://httpd.apache.org/docs/current/howto/htaccess.html)
