{
  "date" : "2021-02-15",
  "keywords" :[ "fișier asf", "format fișier asf", "ce este un fișier asf", "fișier", "exemplu asf", "extensie fișier asf", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASF - Format de fișier de sistem avansat",
  "description":"Aflați despre formatul de fișier ASF și despre API-urile care pot crea și deschide fișiere ASF.",
  "linktitle" : "ASF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Ce este un fișier ASF?

Un fișier cu extensia .asf este un format de fișier multimedia pentru stocarea și redarea fluxurilor media digitale în rețea. Este un format de fișier container care poate avea atât conținut video, cât și audio pentru streaming online. Veți găsi rar fișiere ASF și, mai probabil, găsiți fișierele Windows Media Audio ([WMA](/ro/audio/wma/)) și Windows Media Video ([WMV](/ro/video/wmv/)) care ambele specifică fișiere ASF având conținut codificat cu codecurile respective. Fișierele Windows media pot fi create și citite utilizând Windows Media Format SDK.

## Format de fișier ASF

Un fișier ASF poate cuprinde mai multe fluxuri independente sau dependente. Aceasta poate include mai multe fluxuri audio pentru audio multicanal sau fluxuri video cu mai multe rate de biți. Ratele de biți multiple fac fluxurile potrivite pentru transmisie pe lățimi de bandă diferite. Mai mult, fluxurile dintr-un fișier ASF pot fi în format comprimat sau necomprimat. Cea mai bună compresie este obținută cu codecurile Microsoft Windows Media Audio și Video din seria 9. Specificațiile complete ale formatului de fișier ASF sunt disponibile pe [site-ul Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

### Structura fișierelor de nivel superior ASF

Fișierele ASF conțin în mod logic trei tipuri de obiecte de nivel superior:

* `Obiect Header` - obligatoriu și trebuie plasat la începutul fiecărui fișier ASF
* `Data Object` - obligatoriu și trebuie să urmeze obiectul antet
* `Obiect(e) de indexare` - opțional, dar util pentru furnizarea de acces aleatoriu bazat pe timp la fișierele ASF

Următoarea imagine arată structura de nivel superior a fișierelor ASF.

![ASF File Structure](../asf.png "ASF File Structure")

#### Obiect antet de nivel superior ASF

Obiectul Header oferă o secvență de octeți binecunoscută la începutul fișierelor ASF și poate conține opțional metadate, cum ar fi informații bibliografice. Conține toate informațiile necesare pentru a interpreta corect informațiile din obiectul de date. Obiectul antet poate include mai multe obiecte standard, inclusiv, dar fără a se limita la:

* File Properties Object - Conține atribute globale ale fișierului.
* Stream Properties Object - Definește un flux media digital și caracteristicile acestuia.
* Header Extension Object - Permite adăugarea de funcționalități suplimentare la un fișier ASF, menținând în același timp compatibilitatea cu versiunea anterioară.
* Obiect de descriere conținut - Conține informații bibliografice.
* Script Command Object - Conține comenzi care pot fi executate pe cronologia redării.
* Obiect marcator - Oferă puncte de salt numite într-un fișier.

Obiectul antet este reprezentat folosind următoarea structură:

|Numele câmpului |Tipul câmpului |Dimensiune (biți)|
---|---|---|
|ID obiect| GUID| 128|
|Dimensiunea obiectului| QWORD| 64|
|Numărul de obiecte antet| DWORD| 32|
|Rezervat1| BYTE| 8|
|Rezervat2| BYTE| 8|

#### Obiect de date de nivel superior ASF

Toate datele media digitale pentru un fișier ASF sunt conținute în obiectul de date și sunt stocate sub formă de pachete de date ASF. Fiecare pachet de date are o lungime fixă și conține date pentru unul sau mai multe fluxuri media digitale.

#### Obiecte index de nivel superior ASF

Obiectele index de nivel superior ASF au următoarele două tipuri:

* `Simple Index Object` - Conține un index bazat pe timp al datelor video dintr-un fișier ASF. Intervalul de timp dintre intrările de index este constant și este stocat în obiectul index simplu.
* `Obiect index` - Se referă la obiectul index, obiectul index al obiectului media și obiectul index al codului de timp, ale căror formate sunt similare. Ca și obiectul index simplu, obiectul index indexează în funcție de timp cu un interval de timp fix, dar nu se limitează la fluxurile video.

## Referințe

* [Format de fișier ASF - Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)
* [Format de fișier QuickTime - Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)

