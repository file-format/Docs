{
  "date" : "2019-12-16",
  "keywords" :[ "NB", "fișier", "extensie", "format fișier", "Mathematica", "Foaie de calcul" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre ce sunt API-urile de fișiere NB care pot crea și deschide fișiere NB.",
  "title" :"NB - Format de fișier caiet Mathematica",
  "linktitle" : "NB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-07-16"
}

## Ce este un fișier NB?

Un fișier cu extensia .nb este un format de fișier pentru notebook Wolfram care salvează instrucțiuni pentru instrucțiuni matematice într-un fișier textual. Poate conține multe tipuri diferite de date, cum ar fi calcul în direct, interfețe dinamice arbitrare, introducere tip tipografie completă, introducere a imaginii, adnotare automată a codului, o interfață programatică completă la nivel înalt și mii de funcții și opțiuni atent organizate. Instrucțiunile textuale sunt intrări și ieșiri Mathematica care sunt generate și actualizate pe măsură ce instrucțiunile de intrare sunt introduse în fișier.

## Format de fișier Wolfram Notebook NB - Mai multe informații

Fișierele Wolfram Notebook NB sunt salvate în format text simplu, care este un format de fișier care poate fi citit de om. Conținutul unui caiet este aranjat în secțiuni ca text simplu, unde fiecare este reprezentat de grupuri de celule, similar unei foi de calcul. Intervalul acestor grupuri este definit printr-o paranteză spre sfârșitul fiecărei celule. Stilul atribuit unei celule determină rolul acesteia în blocnotes, așa cum este detaliat mai jos.

### Caiete ca limbaj Wolfram

Când se intenționează salvarea Notebook-ului format din instrucțiuni matematice pentru execuție de către Wolfram Language Kernal, celulelor din document li se atribuie automat stilul de text `Input`. Acest lucru îi spune kernalului să le considere instrucțiuni care sunt executate atunci când utilizatorul lansează o combinație de taste `Shift+Return`. Un caiet Mathematica este așa cum se arată în exemplul următor.

{{< figure src="../Wolfram Notebook.jpeg" alt="Wolfram Notebook File Format" >}}

### Caiete ca documente

Caietele Mathematica pot fi în format de document pentru a oferi o imagine a ceea ce vedeți ceea ce obțineți (WYSIWYG). Aceste documente sunt identice cu cele vizualizate pe ecran sau pe o hârtie tipărită și sunt interactive. Pentru aceasta, `Stilul de text` este atribuit celulei pentru a afișa conținutul fără a executa instrucțiunile de către Kernel.

## Exportați caietele Mathematica

Caietele Mathematica pot fi exportate în multe formate de fișiere diferite, cum ar fi PDF, grafică, GIS, Comprimat și Foi de calcul.

## Referințe

* [Noțiuni de bază pentru notebook Mathematica](https://reference.wolfram.com/language/guide/NotebookBasics.html)

