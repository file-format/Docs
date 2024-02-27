{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HTACCESS-fil - Apache HTACCESS-filformat",
  "description": "Din filformatguide for at lære, hvad en HTACCESS-fil er",
  "linktitle": "HTACCESS",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-htacces-das"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en HTACCESS fil?

En HTACCESS-fil er en Apache-konfigurationsfil, der giver en mekanisme til at tillade konfigurationsændringer for forskellige mapper/mapper på et websted. Det inkluderer konfigurationsdirektiver, der gælder for biblioteket og underbibliotekerne.

En HTACCESS-fil udfører en række kontroller, såsom at definere indekssiden på et websted, angive 404-fejlsiden (Page Not Found), udføre 301- eller 302-sidens omdirigeringer, blokere adgang fra en specifik IP-adresse eller andre websteder. Brugen af .htaccess-filer sænker derfor den overordnede ydeevne af din Apache HTTP-server.

## HTACCESS filformat

HTACCESS-filer gemmes på disken i almindeligt tekstfilformat. Det betyder, at du kan åbne og redigere disse filer i enhver teksteditor. Der er intet navn før . i en .htaccess-fil, der viser, at det er en skjult fil i mappen.

## Almindelig brug af en HTACCESS-fil

Fem almindelige anvendelser af en HTACCESS-fil er som følger.

### Mod_Rewrite

En HTACCESS-fil kan bruges til at udpege og ændre, hvordan URL'er og websider på et websted vises for brugerne.

### Godkendelse

Autentificering kan opnås med .htaccess ved at oprette en passowrd-fil kaldet .htpasswd. Dette giver de besøgende på webstedet mulighed for at angive en adgangskode, hvis de gerne vil besøge en bestemt del af websiden.

### Brugerdefinerede fejlsider

Du kan oprette brugerdefinerede fejlsider såsom 400 Bad Request, 401 Authorization Required, 403 Forbidden Page, 404 File not Found og 500 Intern Error with .htaccess-fil. Disse vil dog sænke serverens ydeevne, da alle disse kontroller vil blive udført, efterhånden som siderne tilgås.

### MIME-typer

Apache HTACCESS-filer kan ændres til at inkludere MIME-typer (Multipurpose Internet Mail Extensions). Dette lader din server understøtte levering af applikationsfiler, der ikke blev understøttet af webstedet.

### SSI

Server Side Includes (SSI) fungerer som en stor tidsbesparelse på et websted. SSI kan aktiveres ved at indsætte følgende kode i din .htaccess-fil.

```
AddType text/html .shtml
AddHandler server-parsed .shtml</pre>
```

## Eksempel på Apache HTACCESS-fil

```
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

## Referencer

* [Apache HTTP Server Tutorial: .htaccess files](https://httpd.apache.org/docs/current/howto/htaccess.html)

