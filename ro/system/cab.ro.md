{
  "date" : "2021-06-29",
  "keywords" :[ "CAB", "extensie", "fișier", "format", "sistem", "Windows Cabinet File", "Microsoft", "Installer", "SetUp", "AdvPak"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CAB – Fișier pentru Windows Cabinet",
  "description":"Aflați despre formatul de fișier CAB și despre API-urile care pot crea și deschide fișiere CAB.",
  "linktitle" : "CAB",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Ce este un fișier CAB? ##

Un fișier cu extensia .cab aparține unui fișier Windows Cabinet care aparține categoriei de fișiere de sistem. Este un fișier care este salvat în formatul de fișier arhivă în versiunile Microsoft Windows care acceptă algoritmi de date comprimate, cum ar fi [LZX](/ro/compression/lzx/), Quantum și [ZIP](/ro/compression/zip/ ). Fișierul are o utilizare vitală atunci când un utilizator sau un dezvoltator dorește să conțină și să partajeze date și fișiere de instalare a software-ului. Caracteristicile de compresie a datelor fără pierderi și certificarea digitală incluse în aceste fișiere fac ca acest fișier să fie perfect pentru stocarea și partajarea unor astfel de fișiere. Acceptă diferite programe de instalare Microsoft, cum ar fi Device Installer, SetUp API și AdvPak.

## Scurt istoric ##

Fișierul CAB este un tip de fișier de comprimare a datelor care a fost dezvoltat de Microsoft. Inițial a fost numit „Diamant”, dar apoi a devenit cunoscut ca fișier CAB, prescurtare pentru cuvântul „Cabinet”.

## Specificatii tehnice ##

Un fișier CAB poate conține de obicei până la maximum 65535 de foldere, care, la rândul lor, pot conține maximum 65536 fișiere fiecare. Mecanismul de stocare a fișierelor CAB este eficient din punct de vedere al timpului și al spațiului, deoarece salvează fiecare folder ca bloc comprimat în loc să comprima și să stocheze fiecare fișier separat. Dosarele goale nu pot fi stocate în folderele de arhivă CAB. Fișierul CAB a fost dezvoltat pentru prima dată de Microsoft și este utilizat în diferite programe de instalare, cum ar fi InstallShield, cu un format ușor diferit. Fișierele CAB sunt în mod obișnuit conectate la programe cu auto-extragere. Fișierele Microsoft CAB sunt ușor de recunoscut datorită markerului lor unic care ajută la identificarea formatului. Markerul unic pentru toate fișierele Microsoft CAB este un prefix de patru cuvinte, MSCF. Văzând acest cod, un utilizator poate distinge cu ușurință un fișier Microsoft CAB de alte fișiere și îl poate utiliza în consecință în compresoare sau versiuni. Fișierele pot fi comprimate cu mai multe date de instalare de software sau datele prezente pot fi decomprimate folosind software-ul potrivit.


## Exemplu CAB ##

Următorul exemplu ilustrează relația dintre fișiere și foldere într-o structură de fișiere CAB:

{{< figure src="../cab.png" alt="Format de fișier CAB" >}}

## Referință ##

* [CAB - WIKIPEDIA](https://en.wikipedia.org/wiki/Cabinet_(file_format))
