{
  "date" : "2023-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Fișier EAZ - Ce este un fișier EAZ și cum se deschide?",
  "description":"Aflați despre formatul de fișier EAZ și despre API-urile care pot crea și deschide fișiere EAZ.",
  "linktitle" : "EAZ",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-en-ea-roz"
}
},
  "lastmod" : "2023-12-23"
}

## Ce este un fișier EAZ?

Fișierul EAZ este un fișier de completare utilizat de ArcGIS Explorer, o aplicație gratuită dezvoltată de ESRI pentru explorarea, vizualizarea și partajarea hărților. Conține o arhivă de fișiere comprimată care include un [XML file](/web/xml/), cod compilat și fișiere de suport necesare pentru supliment. Aceste fișiere sunt folosite pentru a extinde funcționalitatea de bază a software-ului prin încorporarea de butoane noi, ferestre de andocare și alte extensii.

## Format de fișier EAZ - Mai multe informații

Fișierele EAZ sunt create prin utilizarea ArcGIS Explorer SDK, un kit de dezvoltare conceput pentru a crea funcționalități personalizate în ArcGIS Explorer. Aceste fișiere utilizează compresia [ZIP](/compression/zip/) pentru a-și împacheta în mod eficient conținutul. În centrul arhivei, fișierul **Addins.xml** se află în directorul rădăcină, servind ca o componentă vitală care descrie și detaliază diferitele personalizări încorporate în fișierul EAZ.

Fișierul Addins.xml acționează în esență ca o foaie de parcurs, oferind perspective asupra îmbunătățirilor, modificărilor și extensiilor specifice pe care fișierul EAZ le introduce în ArcGIS Explorer. Prin această structură cuprinzătoare, dezvoltatorii pot încapsula și integra perfect noi funcții, butoane și ferestre de andocare, îmbunătățind funcționalitatea generală și experiența utilizatorului aplicației ArcGIS Explorer.

## Referințe

 * [Sharing and installing add-ins](https://desktop.arcgis.com/en/arcmap/latest/analyze/python-addins/sharing-and-installing-add-ins.htm)
