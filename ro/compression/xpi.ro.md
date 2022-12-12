{
  "date" : "2022-06-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPI - Fișier pachet de instalare multiplatformă",
  "description":"Aflați despre formatul de fișier XPI și despre API-urile care pot crea și deschide fișiere XPI.",
  "linktitle" : "XPI",
  "menu" : {
    "docs" : {
    "identifier": "compression-xpi",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-07"
}

## Ce este un fișier XPI?

Un fișier XPI este o arhivă de instalare care este comprimată pentru a reduce dimensiunea fișierului. Este folosit de aplicațiile Mozilla pentru instalarea de pluginuri și fișiere suplimentare. Conține un script de instalare sau un manifest la rădăcina fișierului împreună cu un număr de fișiere de date. Un fișier XPI poate conține teme, set de instrumente sau pluginuri Firefox pe care utilizatorul le poate instala pentru a deveni parte a browserului Firefox, Thunderbird sau SeaMonkey.

## Format de fișier XPI - Mai multe informații

Fișierele XPI sunt salvate pe disc ca arhive [ZIP](/ro/compression/zip/) care combină mai multe fișiere într-un singur fișier comprimat. Fișierele din interiorul unui fișier XPI pot include fișiere script de instalare, cum ar fi JS și fișiere web, cum ar fi [CSS](/ro/web/css/), [HTML](/ro/web/html/) și [JSON](/ro/web/json/ ). Uneori, poate conține, de asemenea, fișiere imagine [PNG](/ro/image/png/) pentru a fi folosite ca pictograme prin supliment.

### Cum să vizualizați conținutul fișierului XPI?

Un fișier XPI este practic o arhivă ZIP al cărei conținut poate fi vizualizat urmând pașii următori.

* Schimbați extensia fișierului de la XPI la ZIP
* Extrageți conținutul fișierului folosind orice utilitar standard de decompresie, cum ar fi WinZip (Windows, Mac), 7-Zip (Windows) sau Apple Archive Utility (Mac).

### Instalați fișierul XPI pe Firefox Android

În cea mai mare parte, oamenii sunt curioși să știe dacă fișierele XPI pot fi instalate în Firefox pe dispozitivele Android. Pe Android, puteți instala suplimentul dintr-un fișier XPI localizând fișierul și deschizându-l cu Firefox.

## Referințe

* [XPInstall - Wikipedia](https://en.wikipedia.org/wiki/XPInstall)
* [Cum pot deschide o extensie de fișier XPI?](https://support.mozilla.org/en-US/questions/1009049)

