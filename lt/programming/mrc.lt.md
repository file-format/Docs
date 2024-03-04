{
  "date": "2021-09-14",
  "keywords": [
"mrc",
"failą",
"pratęsimas",
"Dokumento formatas",
"mrc įgyvendinimas",
"Programavimo vadovas",
"mrc pavyzdys",
"mIRC",
"mIRC scenarijų kalba",
"INI failai",
"mSL scenarijų kalba",
"mIRC kalba",
"mIRC scenarijus",
"scenarijų kalba"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "MRC – mIRC scenarijaus kalbos failas",
  "description": "Sužinokite apie MRC failo formatą ir API, kurios gali kurti ir atidaryti MRC failus.",
  "linktitle": "MRC",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-mr-ltc"
}
},
  "lastmod": "2021-09-14"
}

## Kas yra MRC failas?

mIRC yra scenarijų kalba, įterpta kaip IRC klientas (Internet Relay Chat) į Windows operacinę sistemą. Tai suteikia galimybę apsaugoti nuo šiukšlių asmeniniam ir kanalo naudojimui. Siekiant užtikrinti geresnę vartotojo suderinamumo patirtį, ši mIRC scenarijų kalba leidžia kurti dialogo langus. Failai, kuriuose yra scenarijų, dažniausiai paprasto teksto formatu, yra saugomi su MRC plėtiniu arba kaip [INI](/system/ini/) failai. Šios kalbos funkcijos yra žinomos kaip komandos ir identifikatoriai (kai jie grąžina reikšmę).

mIRC kalba leidžia vienu metu įkelti kelis scenarijaus failus. Kita vertus, vienas failas gali būti nebenaudojamas, kai įkeliamas vienu metu. Komandos išsaugomos ir IRC gali egzistuoti automatiškai. Šioje kalboje naudojamos komandos ir slapyvardžiai neturi jokių simbolių pirmumo.

mIRC plačiai naudojamas, kad robotai automatiškai valdytų kanalą, tačiau jį taip pat galima modifikuoti naudojant mSL scenarijų kalbą. Jis gali pristatyti daug naujų funkcijų, pvz., makrokomandas, muzikos grojimo galimybes, mažas makrokomandas ir funkcijas, pagrindinius žaidimus arba mažų programų valdymą.


## Trumpa istorija ##

Šią scenarijų kalbą 1995 m. pirmą kartą sukūrė Khaledas Adam Bey. Scenarijų kalbos dizainą taip pat sukūrė Khalidas. Šios kalbos tikslas buvo įvykiais pagrįstas programavimas. Iš pradžių šios programavimo kalbos failams naudotas failo plėtinys buvo .mrc ir .ini. Be to, jis buvo sukurtas pagal patentuotos programinės įrangos licenciją.

## Techninė specifikacija Nr.

Kai kurios funkcijos yra pritaikytos pagal šią mIRC kalbą ir yra žinomos kaip slapyvardžiai. Kai šie slapyvardžiai grąžina reikšmes, jie yra žinomi kaip pasirinktiniai identifikatoriai. Visi šioje mIRC kalboje esantys kintamieji įvedami dinamiškai. Sigilius naudoja mIRC scenarijai. Dar viena šios scenarijų kalbos savybė – iššokantys langai. Vartotojai gali skambinti į iššokančiuosius langus tiesiog juos pasirinkę. Nuotolinio valdymo pultai yra nurodyti tam tikriems įvykiams. Nuotolinio valdymo pultai iškviečiami, kai įvyksta santykinis įvykis.

Tarpu atskirti žetonai naudojami kiekvienai šios kalbos kodo eilutei nutraukti. Yra keletas kitų populiarių plėtinių, naudojamų mIRC failams, pvz., MDX (mIRC Dialog Extension) ir DCX (Dialog Control Extension). Abu jie yra dialogo plėtiniai ir yra palyginti populiaresni. Kalbos konstrukcijos yra nurodytos šios scenarijų kalbos nomenklatūroje. mIRC kalba apima įvairius scenarijų kalbos aspektus, tokius kaip vietiniai ir pasauliniai kintamieji, dvejetainiai kintamieji, maišos lentelės ir failų tvarkymas.


## MRC failo formato pavyzdys Nr.

```

;Defines the alias 'hello' in the remote script

;Note: if this is placed in an alias script,
;the 'alias' part must be removed (result: hello {)
;Usage: /hello

alias hello {

  ;Displays(/echo) 'Hello World!' into the active window(-a)
  echo -a Hello World!

}

```

```
;Placed in a remote script

;When a user types Hello! in a channel,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:#:{ msg $chan Hello, $nick $+ ! }

;When a user types Hello! in a private message,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:?: { msg $nick Hello, $nick $+ ! }

;Here is a script which automatically gives voice to a user
;who joins a particular channel (The Bot or user should have HOP)

on *:JOIN:#?: { mode $chan +v $nick }

;A bad word script

on *:Text:die*:#: { .mode $chan +b $nick | kick $chan $nick Dont say that again }

```

## Nuoroda ##

* [MIRC – pateikė Vikipedija](https://en.wikipedia.org/wiki/MIRC_scripting_language)




