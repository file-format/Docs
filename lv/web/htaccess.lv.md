{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HTACCESS fails — Apache HTACCESS faila formāts",
  "description": "Jūsu faila formāta ceļvedis, lai uzzinātu, kas ir HTACCESS fails",
  "linktitle": "HTACCESS",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-htacces-lvs"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir HTACCESS fails?

HTACCESS fails ir Apache konfigurācijas fails, kas nodrošina mehānismu, lai atļautu konfigurācijas izmaiņas dažādām vietnes mapēm/direktorijiem. Tas ietver konfigurācijas direktīvas, kas ir piemērojamas direktorijam un apakšdirektorijiem.

HTACCESS fails veic vairākas pārbaudes, piemēram, definē vietnes rādītāja lapu, uzskaita 404 (lapa nav atrasta) kļūdas lapu, veic 301. vai 302. lapas novirzīšanu, bloķē piekļuvi no noteiktas IP adreses vai citām vietnēm. Tādējādi .htaccess failu izmantošana palēnina Apache HTTP servera vispārējo veiktspēju.

## HTACCESS faila formāts

HTACCESS faili tiek saglabāti diskā vienkārša teksta faila formātā. Tas nozīmē, ka varat atvērt un rediģēt šos failus jebkurā teksta redaktorā. Pirms . .htaccess failā, parādot, ka tas ir mapē slēpts fails.

## HTACCESS faila parastie lietojumi

Pieci izplatītākie HTACCESS faila lietojumi ir šādi.

### Mod_Rewrite

HTACCESS failu var izmantot, lai norādītu un mainītu to, kā vietnes URL un tīmekļa lapas tiek rādītas lietotājiem.

### Autentifikācija

Autentificēšanu var panākt ar .htaccess, izveidojot passowrd failu ar nosaukumu .htpasswd. Tas ļauj vietnes apmeklētājiem norādīt paroli, ja viņi vēlas apmeklēt noteiktu tīmekļa lapas sadaļu.

### Pielāgotas kļūdu lapas

Varat izveidot pielāgotas kļūdu lapas, piemēram, 400. slikts pieprasījums, 401. vajadzīga autorizācija, 403. aizliegtā lapa, 404. fails nav atrasts un 500. iekšēja kļūda, izmantojot .htaccess failu. Tomēr tas palēninās servera veiktspēju, jo visas šīs pārbaudes tiks izpildītas, piekļūstot lapām.

### MIME veidi

Apache HTACCESS failus var modificēt, lai iekļautu daudzfunkcionālo interneta pasta paplašinājumu (MIME) veidus. Tas ļauj jūsu serverim atbalstīt tādu lietojumprogrammu failu piegādi, kurus vietne neatbalstīja.

### SSI

Server Side Includes (SSI) darbojas kā lielisks laika ietaupījums vietnē. SSI var iespējot, savā .htaccess failā ievietojot šādu kodu.

```
AddType text/html .shtml
AddHandler server-parsed .shtml</pre>
```

## Apache HTACCESS faila piemērs

```
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

## Atsauces

* [Apache HTTP Server Tutorial: .htaccess files](https://httpd.apache.org/docs/current/howto/htaccess.html)

