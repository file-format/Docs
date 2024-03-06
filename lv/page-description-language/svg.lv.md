{
  "date": "2020-03-02",
  "keywords": [
"SVG",
"failu",
"faila formātā",
"Lapas apraksts Valoda",
"Skalārs"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par SVG failu formātu un API, kas var izveidot un atvērt SVG failus.",
  "title": "Kas ir SVG fails?",
  "linktitle": "SVG",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-sv-lvg"
}
},
  "lastmod": "2020-03-02"
}

## Kas ir SVG fails? ##

An SVG file is a Scalar Vector Graphics file that uses XML based text format for describing the appearance of an image. The word Scalable refers to the fact that the SVG can be scaled to different sizes without losing any quality. Text-based description of such files makes them independent of resolution. It is one of the most used formats for building a website and print graphics in order to achieve scalability. The format can only be used for two-dimensional graphics though. SVG files can be viewed/opened in almost all modern browsers including Chrome, Internet Explorer, Firefox, and Safari.

## Īsa vēsture ##

SVG specifications are available as open standard by World Wide Web Consortium (W3C) since 1999. Pirms tam līdz 1998. gadam W3C tika iesniegtas līdzīgas failu formātu specifikācijas sešos dažādos formātos. 2011. gadā specifikācijām tika lietots atjauninājums un tā versija tika 1.1. 2016. gadā SVG 2 tika publicēts kā jaunāka versija, kas ietver papildu funkcijas papildus SVG 1.1.

## Faila formāta specifikācijas ##

SVG dokumenta objektu modelis (DOM) liek pamatus visām specifikācijām un saskarnēm, kas atbilst konkrētajām specifikāciju sadaļām. SVG skatītājiem ir jāievieš SVG DOM saskarnes, kā noteikts visās W3C specifikācijās. Tā DOM atklāj vairākas saskarnes dažādiem datu tipiem un elementiem.

### SVG formas ###

SVG ir daži iepriekš noteikti formas elementi, kurus var izmantot izstrādātāji:

* Taisnstūris<rect>

* Aplis<circle>

* Elipse<ellipse>

* Līnija<line>

* Polilīnija<polyline>

* Daudzstūris<polygon>

* Ceļš<path>


Pamatojoties uz šīm formām un specifikācijām, SVG funkcionālās jomas ir šādas.

**Ceļi** — ceļi tiek izmantoti, lai attēlotu vienkāršas, kā arī saliktas formas kontūras. Kodējumi tiek izmantoti, lai definētu darbības raksturu. Piemēram, M tiek izmantots Move To, L tiek izmantots Line To, Z tiek izmantots, lai aizvērtu ceļu un tā tālāk.

**Pamatformas** — var zīmēt taisnu līniju ceļus un ceļus, kas sastāv no virknes savienotu taisnu līniju segmentu (polilīniju), kā arī slēgtus daudzstūrus, apļus un elipses. Taisnstūri un taisnstūri ar apaļiem stūriem arī ir standarta elementi.

**Teksts** — teksta attēlojums tiek izteikts kā XML rakstzīmju dati, kur tekstam var izmantot daudzus vizuālos efektus. Specifikācijas ļauj apstrādāt divvirzienu tekstu, vertikālu tekstu un rakstzīmes pa izliektu ceļu.

**Glezniecība** — formas var aizpildīt un/vai ieskicēt ar krāsu, gradientu vai rakstu, kas ļauj to padarīt necaurspīdīgu vai jebkāda veida caurspīdīgumu. Līnijas beigu elementi, piemēram, bultu uzgaļi vai simboli, kas parādās daudzstūra virsotnēs, tiek attēloti ar marķieriem.

**Krāsa** — SVG specifikācijas ļauj piemērot krāsas visiem redzamajiem SVG elementiem vai nu tieši, vai ar aizpildījumu, triepienu un citām īpašībām. Var izmantot dažādus krāsu kodus, lai norādītu, piemēram, melnu vai zilu, heksadecimālo attēlojumu, decimāldaļu vai RGB formas procentuālo daļu.

**Gradienti un raksti** — SVG faila formas var aizpildīt vai ieskicēt ar vienkrāsainām krāsām, gradientiem vai atkārtotiem rakstiem.

**Filtra efekti** — patiesībā tā ir grafikas darbību sērija, kas tiek lietota noteiktai avota vektorgrafikai, lai iegūtu modificētu rezultātu.

**Interaktivitāte** — lietotāji var mijiedarboties ar SVG failiem, mainot fokusu, noklikšķinot ar peles klikšķi, ritinot vai tuvinot attēlu. Interaktivitāte ļauj SVG attēliem mijiedarboties ar lietotājiem daudzos dažādos veidos, kā minēts iepriekš.

**Saistīšana** — SVG attēliem var būt hipersaites uz citiem dokumentiem. Tas tiek panākts, izmantojot XML saistīšanas valodu vai XLink. Tas ļauj izveidot īpašus skata stāvokļus, kas tiek izmantoti, lai tuvinātu/tālinātu noteiktu apgabalu vai ierobežotu skatu uz noteiktu elementu.

**Skriptēšana** — līdzīgi kā HTML, visi SVG dokumenta aspekti ir pieejami manipulācijām, izmantojot skriptus. SVG DOM objekti sniedz norādījumus, kā to panākt, izmantojot SVG elementu un atribūtu. Skripti ir ietverti skripta taga elementos un var darboties, reaģējot uz rādītāja, tastatūras vai dokumenta notikumiem pēc vajadzības.

**Animācija** — DOM elementi<animate> ,<animateMotion> un<animateColor> ļauj iekļaut animāciju SVG saturam. Protams, tas nav sasniedzams, neizmantojot skriptus un iebūvētos taimerus. Šīs animācijas var būt nepārtrauktas, un tās var ievietot cilpā, kā arī atkārtot, tajā pašā laikā reaģējot uz lietotāja notikumiem.

**Fonti** — teksts SVG formātā var atsaukties uz ārējiem fontu failiem, piemēram, sistēmas fontiem. Ja šādu fontu nav, teksts SVG formātā netiks renderēts izvadē. To var novērst, iekļaujot nepieciešamos glifus šādā failā kā fontu, kas pēc tam tiek renderēts, izmantojot<text> elements.

## Piemēri ##
Nākamajās rindiņās ir parādīts, kā aplis tiek attēlots, izmantojot SVG skriptu.

```
<html>
<body>

<h1>My first SVG</h1>

<svg width#"100" height#"100">
  <circle cx#"50" cy#"50" r#"40" stroke#"green" stroke-width#"4" fill#"yellow" />
</svg>

</body>
</html>
```

Šīs koda rindas parāda, kā izmantot<text> bloks teksta renderēšanai SVG formātā.

```
<svg height#"30" width#"200">
  <text x#"0" y#"15" fill#"red">I love SVG!</text>
</svg>
```

## Atsauces Nr.

* [W3C SVG specifikācijas](https://www.w3.org/TR/SVG2/Overview.html)

* [SVG — Wikipedia](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics)


