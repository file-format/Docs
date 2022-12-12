{
  "date" : "2021-06-24",
  "keywords" :[ "PARTE", "parțial", "extensie", "fișier", "format", "web", "descărcat" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PARTE – Fișier descărcat parțial",
  "description":"Aflați despre formatul de fișier PART și despre API-urile care pot crea și deschide fișiere PART.",
  "linktitle" : "PART",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## Ce este un fișier PART? ##

Un fișier parțial sau extensia .part este un fișier descărcat parțial. Este utilizat atunci când descărcările sunt în curs sau au fost întrerupte din cauza oricărei probleme, oferind managerului de descărcare posibilitatea de a relua descărcarea ori de câte ori este posibil.
Aceasta înseamnă că browserul, cum ar fi Firefox sau programele de transfer de fișiere precum eMule, eMule plus, FlashGet etc. stochează o porțiune a fișierului, numită Fișier parte, în timp ce descărcarea are loc pe dispozitivul dvs. Acest fișier parte vă va arăta dacă descărcarea este în curs sau a fost întreruptă înainte de finalizare. Nu numai asta, ci și fișierul PART stochează toate datele până la finalizarea descărcării, motiv pentru care unele dintre ele pot fi reluate ulterior dacă doriți să începeți din nou descărcarea.

## Format fișier PART ##

There are few browsers that break large download files into smaller downloads and assign each portion a .part extension. These files can be seen in the “Download” folder. Once the download is finished, the browser will combine all the PART files to give a final downloaded file. For example, while downloading a file from Firefox, the download manager will store the data being downloaded in a PART file and replaces the name with certain characters, and add a .part extension at the end, such as **doodle.or** becomes **JKzMn.or.part**. After completion, Firefox will remove the .part extension and the file will be ready to launch.
