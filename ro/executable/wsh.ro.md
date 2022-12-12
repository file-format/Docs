{
  "date" : "2021-08-27",
  "keywords" :[ "fișier wsh", "format fișier wsh", "ce este un fișier wsh", "fișier", "exemplu wsh", "extensie fișier wsh", "extensie", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier WSH și despre API-urile care pot crea și deschide fișiere WSH.",
  "title" :"WSH - Fișier Script Windows",
  "linktitle" : "WSH",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-27"
}

## Ce este un fișier WSH?
Un fișier cu extensia .wsh conține proprietăți și parametri pentru un anumit script de limbaj de programare, cum ar fi VB sau VBS etc. Necesitatea reală a WSH este să le folosească pentru personalizarea execuției anumitor scripturi. WScript sau CScript sunt necesare pentru a rula și ambele sunt incluse în sistemul de operare Windows. Fișierele WSH au fost furnizate inițial pe Windows 95 pe discurile de instalare ca opțional configurabil și instalabil pentru Panoul de control, iar apoi o componentă implicită a Windows 98.

## Format de fișier WSH
WSH (Windows Script Host) poate fi utilizat în diverse scopuri, inclusiv administrare, scripturi de conectare și automatizare generală. WSH stabilește un mediu pentru rularea scripturilor. invocă motorul de script adecvat și alocă un set de servicii și obiecte cu care să lucreze scriptul. Aceste scripturi pot fi rulate în modul GUI, dintr-un obiect COM sau modul linie de comandă, oferind flexibilitate utilizatorului atât pentru scripturi interactive, cât și pentru cele non-interactive.

### Exemple
Iată un exemplu foarte simplu care arată unele VBScript care utilizează obiectul rădăcină WSH COM „WScript” pentru a afișa un mesaj cu un buton „OK”. Când acest script va fi lansat, motorul CScript sau WScript va fi apelat și mediul de rulare va fi stabilit.

```
WScript.Echo "Hello world"
WScript.Quit
```


## Referințe

* [Windows Script Host - de la Wikipedia](https://en.wikipedia.org/wiki/Windows_Script_Host)



