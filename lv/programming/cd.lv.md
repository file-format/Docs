{
  "date": "2020-01-10",
  "keywords": [
"cd",
".cd",
"kas ir cd fails",
"kā atvērt cd failu",
"pagarinājumu",
"failu",
"cd fails",
"cd faila formātā",
"cd faila paplašinājums"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CD — Visual Studio klases diagrammas fails",
  "description": "Uzziniet par CD failu formātu un API, kas var izveidot un atvērt CD failus.",
  "linktitle": "CD",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-c-lvd"
}
},
  "lastmod": "2021-06-24"
}

## Kas ir CD fails?

Fails ar paplašinājumu .cd ir Visual Studio klašu diagrammas fails, kas sniedz informāciju par struktūru un attiecībām starp visām pašreizējā risinājuma klasēm. Visual Studio risinājumā (ko pārstāv [.sln](/programming/sln/)) var būt viens vai vairāki projekti, katram no kuriem ir vairākas atšķirīgas klases. Klases diagrammas failu var ģenerēt, ar peles labo pogu noklikšķinot uz projekta un atlasot klases diagrammas opciju.

## Klases diagrammas (.cd) faila formāts — vairāk informācijas

Klases diagrammas fails tiek saglabāts standarta XML faila formātā, kas projektā apzīmē klases kā XML mezglus. Ja Visual Studio nav pieejams, šos klašu diagrammas failus var atvērt jebkurā lietojumprogrammā, kas atbalsta XML failu atvēršanu.

### Kā Visual Studio projektam pievienot klašu diagrammas

Programmā Visual Studio atveriet risinājumu/projektu, kuram vēlaties pievienot klases diagrammu. Pēc tam ar peles labo pogu noklikšķiniet uz projekta mezgla un pēc tam izvēlieties Pievienot > Jauns vienums. Vai arī nospiediet Ctrl+Shift+A.

 * Tiek atvērts dialoglodziņš Pievienot jaunu vienumu.

 * Izvērsiet Izplatīti vienumi > Vispārīgi un pēc tam veidņu sarakstā atlasiet Klases diagramma. Visual C++ projektiem meklējiet kategoriju Utilītprogramma, lai atrastu klases diagrammas veidni.

### Eksportējiet klašu diagrammas (CD) uz attēliem

Visual Studio ļauj konvertēt/eksportēt klašu diagrammas tādos attēlos kā [PNG](/image/png/), [JPEG](/image/jpeg/) un [BMP](/image/bmp/). Šos eksportētos klašu diagrammu failus var izmantot dokumentācijas un tehnisko datu pakotņu (TDP) uzskaites vajadzībām. Lai klases diagrammu pārveidotu par attēlu, programmā Microsoft Visual Studio var veikt šādas darbības.

1. Atveriet klases diagrammas (.cd) failu.
1. Izvēlnē Klases diagramma vai diagrammas virsmas saīsnes izvēlnē izvēlieties Eksportēt diagrammu kā attēlu.
1. Izvēlieties diagrammu.
1. Izvēlieties vajadzīgo formātu.
1. Izvēlieties Eksportēt, lai pabeigtu eksportēšanu.

## Atsauces

* [Dizaina nodarbības programmā Visual Studio](https://learn.microsoft.com/en-us/visualstudio/ide/class-designer/designing-and-viewing-classes-and-types?view=vs-2019)


