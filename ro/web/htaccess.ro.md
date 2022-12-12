{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier HTACCESS - Format fișier Apache HTACCESS",
  "description" :"Ghidul dvs. de format de fișier pentru a afla ce este un fișier HTACCESS",
  "linktitle" : "HTACCESS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier HTACCESS?

Un fișier HTACCESS este un fișier de configurare Apache care oferă un mecanism pentru a permite modificări de configurare pentru diferite foldere/directoare ale unui site web. Acesta include directive de configurare care sunt aplicabile directorului și subdirectoarelor.

Un fișier HTACCESS efectuează o serie de verificări, cum ar fi definirea paginii de index a unui site web, listarea paginii de eroare 404 (Pagina nu a fost găsită), efectuarea redirecționărilor de pagini 301 sau 302, blocarea accesului de la o anumită adresă IP sau alte site-uri web. Prin urmare, utilizarea fișierelor .htaccess încetinește performanța generală a serverului tău Apache [HTTP](/ro/web/http/).

## Format de fișier HTACCESS

Fișierele HTACCESS sunt stocate pe disc în format text simplu. Aceasta înseamnă că puteți deschide și edita aceste fișiere în orice editor de text. Nu există niciun nume înainte de „.” într-un fișier .htaccess, care arată că este un fișier ascuns în folder.

## Utilizări obișnuite ale unui fișier HTACCESS

Cinci utilizări comune ale unui fișier HTACCESS sunt următoarele.

### Mod_Rewrite

Un fișier HTACCESS poate fi utilizat pentru a desemna și a modifica modul în care adresele URL și paginile web de pe un site web sunt afișate utilizatorilor.

### Autentificare

Autentificarea poate fi realizată cu .htaccess prin crearea unui fișier passwrd numit .htpasswd. Acest lucru permite vizitatorilor site-ului să furnizeze o parolă dacă doresc să viziteze o anumită secțiune a paginii web.

### Pagini de eroare personalizate

Puteți crea pagini de eroare personalizate, cum ar fi 400 Solicitare greșită, 401 Autorizare necesară, 403 Pagina interzisă, 404 Fișier nu a fost găsit și 500 Eroare internă cu fișierul .htaccess. Totuși, acestea vor încetini performanța serverului, deoarece toate verificările vor fi executate pe măsură ce paginile sunt accesate.

### Tipuri MIME

Fișierele Apache HTACCESS pot fi modificate pentru a include tipuri MIME (Multipurpose Internet Mail Extensions). Acest lucru permite serverului dvs. să accepte livrarea fișierelor de aplicație care nu au fost acceptate de site.

### SSI

Server Side Includes (SSI) acționează ca o mare economie de timp pe un site web. SSI poate fi activat inserând următorul cod în fișierul dvs. .htaccess.

```
AddType text/html .shtml
AddHandler server-parsed .shtml</pre>
```

## Exemplu de fișier Apache HTACCESS

```
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

## Referințe

* [Tutorial Apache HTTP Server: fișiere .htaccess](https://httpd.apache.org/docs/current/howto/htaccess.html)

