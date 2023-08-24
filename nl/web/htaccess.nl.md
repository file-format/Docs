{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTACCESS-bestand - Apache HTACCESS-bestandsindeling",
  "description" :"Uw gids voor bestandsindelingen om te leren wat een HTACCESS-bestand is",
  "linktitle" : "HTACCESS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een HTACCESS-bestand?

Een HTACCESS-bestand is een Apache-configuratiebestand dat een mechanisme biedt om configuratiewijzigingen voor verschillende mappen/directories van een website toe te staan. Het bevat configuratierichtlijnen die van toepassing zijn op de directory en subdirectories.

Een HTACCESS-bestand voert een aantal controles uit, zoals het definiëren van de indexpagina van een website, het weergeven van de 404 (Page Not Found)-foutpagina, het uitvoeren van de 301- of 302-paginaomleidingen, het blokkeren van toegang vanaf een specifiek IP-adres of andere websites. Het gebruik van .htaccess-bestanden vertraagt dus de algehele prestatie van uw Apache HTTP-server.

## HTACCESS-bestandsindeling

HTACCESS-bestanden worden op schijf opgeslagen in platte tekstbestandsindeling. Dit betekent dat u deze bestanden in elke teksteditor kunt openen en bewerken. Er staat geen naam voor de "." in een .htaccess-bestand, waaruit blijkt dat het een verborgen bestand in de map is.

## Veelvoorkomend gebruik van een HTACCESS-bestand

Vijf veelvoorkomende toepassingen van een HTACCESS-bestand zijn als volgt.

### Mod_Herschrijven

Een HTACCESS-bestand kan worden gebruikt om aan te geven en te wijzigen hoe URL's en webpagina's op een website aan de gebruikers worden weergegeven.

### Authenticatie

Authenticatie kan worden bereikt met .htaccess door een wachtwoordbestand aan te maken met de naam .htpasswd. Hierdoor kunnen sitebezoekers een wachtwoord opgeven als ze een bepaald gedeelte van de webpagina willen bezoeken.

### Aangepaste foutpagina's

U kunt aangepaste foutpagina's maken, zoals 400 Bad Request, 401 Authorization Required, 403 Forbidden Page, 404 File not Found en 500 Internal Error met .htaccess-bestand. Deze zullen echter de serverprestaties vertragen, aangezien deze alle controles zullen worden uitgevoerd wanneer de pagina's worden geopend.

### MIME-typen

Apache HTACCESS-bestanden kunnen worden aangepast om MIME-typen (Multipurpose Internet Mail Extensions) op te nemen. Hierdoor kan uw server de levering van toepassingsbestanden ondersteunen die niet door de site werden ondersteund.

### SSI

Server Side Inclusief (SSI) werkt als een geweldige tijdsbesparing op een website. SSI kan worden ingeschakeld door de volgende code in uw .htaccess-bestand in te voegen.

```
AddType text/html .shtml
AddHandler server-parsed .shtml</pre>
```

## Apache HTACCESS-bestandsvoorbeeld

```
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

## Referenties

* [Apache HTTP Server-zelfstudie: .htaccess-bestanden](https://httpd.apache.org/docs/current/howto/htaccess.html)

