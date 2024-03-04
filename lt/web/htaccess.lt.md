{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HTACCESS failas – Apache HTACCESS failo formatas",
  "description": "Jūsų failo formato vadovas, kad sužinotumėte, kas yra HTACCESS failas",
  "linktitle": "HTACCESS",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-htacces-lts"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra HTACCESS failas?

HTACCESS failas yra Apache konfigūracijos failas, suteikiantis mechanizmą, leidžiantį keisti skirtingų svetainės aplankų / katalogų konfigūraciją. Jame yra konfigūracijos nurodymai, taikomi katalogui ir pakatalogiams.

HTACCESS failas atlieka daugybę patikrinimų, pavyzdžiui, apibrėžia svetainės rodyklės puslapį, pateikia 404 (puslapis nerastas) klaidos puslapį, atlieka 301 arba 302 puslapio peradresavimą, blokuoja prieigą iš konkretaus IP adreso ar kitų svetainių. Taigi .htaccess failų naudojimas sulėtina bendrą Apache HTTP serverio našumą.

## HTACCESS failo formatas

HTACCESS failai išsaugomi diske paprasto teksto failo formatu. Tai reiškia, kad šiuos failus galite atidaryti ir redaguoti naudodami bet kurią teksto rengyklę. Prieš . .htaccess faile, parodant, kad tai aplanke paslėptas failas.

## Įprasti HTACCESS failo naudojimo būdai

Penki įprasti HTACCESS failo naudojimo būdai yra tokie.

### Mod_Rewrite

HTACCESS failas gali būti naudojamas norint nurodyti ir pakeisti, kaip svetainės URL ir tinklalapiai rodomi vartotojams.

### Autentifikavimas

Autentifikavimas gali būti pasiektas naudojant .htaccess sukuriant slaptažodžio failą, pavadintą .htpasswd. Tai leidžia svetainės lankytojams pateikti slaptažodį, jei jie norėtų apsilankyti tam tikroje tinklalapio dalyje.

### Priskirti klaidų puslapiai

Galite sukurti pasirinktinius klaidų puslapius, pvz., 400 netinkama užklausa, 401 autorizacija reikalinga, 403 uždraustas puslapis, 404 failas nerastas ir 500 vidinė klaida naudodami .htaccess failą. Tačiau tai sulėtins serverio veikimą, nes visi šie patikrinimai bus atliekami atidarius puslapius.

### MIME tipai

Apache HTACCESS failus galima modifikuoti, kad būtų įtraukti daugiafunkciniai interneto pašto plėtiniai (MIME). Tai leidžia jūsų serveriui palaikyti programų failų, kurių nepalaiko svetainė, pristatymą.

### SSI

Server Side Includes (SSI) veikia kaip puikus laiko taupymas svetainėje. SSI galima įjungti į .htaccess failą įterpus šį kodą.

```
AddType text/html .shtml
AddHandler server-parsed .shtml</pre>
```

## Apache HTACCESS failo pavyzdys

```
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

## Nuorodos

* [Apache HTTP Server Tutorial: .htaccess files](https://httpd.apache.org/docs/current/howto/htaccess.html)

