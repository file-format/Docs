{
  "date" : "2021-28-05",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" : "MAR — Microsoft Access pārskatu fails",
  "keywords" : [ "mar", "mar file", "mar file format", "what is access report", "access report", "microsoft access report"],
  "description":"Uzziniet par piekļuves atskaites (MAR) faila formātu, ko izmanto Microsoft Access programmatūra, lai izveidotu saīsni vai saiti uz Microsoft Access atskaiti.",
  "linktitle" : "MAR",
  "menu" : {
    "docs" : {
    "identifier": "reporting-mar-lv",
      "parent" : "reporting"
}
},
  "lastmod" : "2021-28-05"
}

## Kas ir piekļuves pārskats (MAR fails)? ##
Fails, ko Microsoft Access izveidojis kā pārskata saīsni, tiek saglabāts ar faila paplašinājumu .mar. **Microsoft Access pārskats** piedāvā veidu, kā formatēt, skatīt un apkopot informāciju Microsoft Access datu bāzē. Šīs atskaites ļauj formatēt datus precīzā un informatīvā izkārtojumā, lai tos varētu skatīt ekrānā vai drukāt. Pārskatā tiek rādīti tikai statiskie dati, kas nozīmē, ka, skatot Access pārskatu, mēs nevaram mainīt tabulu datus. Atverot atskaiti, tiek parādīti jaunākie dati.

## Microsoft Access atskaites (MAR) faila formāts

Programmatūra Microsoft Access izmanto MAR faila formātu, lai izveidotu saīsni vai saiti uz Microsoft Access atskaiti, kas ir datu bāzes objekts, kas kļūst noderīgs, ja datu bāzē ir jāuzrāda informācija kādam no šiem lietojumiem:

- Parādiet datu kopsavilkumu.
- Arhivējiet datu momentuzņēmumus.
- Parādiet informāciju par atsevišķiem ierakstiem.
- Izveidojiet etiķetes.

## Piekļuves pārskata daļas
Access atskaites dizains ir sadalīts dažādās sadaļās, kuras var skatīt noformējuma skatā. Nākamajā tabulā ir paskaidrots, kā katra sadaļa darbojas un var palīdzēt izveidot pārskatus.
| Sadaļa | Kā sadaļa tiek parādīta drukātā veidā | Kur var izmantot sadaļu |
---------|----|------|
| Pārskata galvene | Ziņojuma sākumā. | Izmantojiet pārskata galveni, lai iegūtu informāciju, kas parasti var tikt rādīta titullapā, piemēram, logotipam, nosaukumam vai datumam. Ja atskaites galvenē ievietojat aprēķināto vadīklu, kurā tiek izmantota funkcija Summa agregate, aprēķinātā summa attiecas uz visu pārskatu. Atskaites galvene tiek drukāta pirms lapas galvenes. |
| Lapas galvene | Katras lapas augšdaļā. | Izmantojiet lapas galveni, lai atkārtotu pārskata nosaukumu katrā lapā. |
| Grupas galvene | Katras jaunas rekordu grupas sākumā. | Izmantojiet grupas galveni, lai izdrukātu grupas nosaukumu. Piemēram, pārskatā, kas ir grupēts pēc produkta, izmantojiet grupas galveni, lai izdrukātu produkta nosaukumu. Ja grupas galvenē ievietojat aprēķināto vadīklu, kurā tiek izmantota funkcija Summa agregate, summa attiecas uz pašreizējo grupu. Pārskatā var būt vairākas grupas galvenes sadaļas atkarībā no tā, cik grupēšanas līmeņus esat pievienojis. Papildinformāciju par grupu galveņu un kājenju izveidi skatiet sadaļā Grupēšanas, kārtošanas vai kopsummu pievienošana. |
| Sīkāka informācija | Parādās vienreiz katrā ieraksta avota rindā. | Šeit jūs ievietojat vadīklas, kas veido pārskata galveno daļu. |
| Grupas kājene | Katras ierakstu grupas beigās. | Izmantojiet grupas kājeni, lai drukātu kopsavilkuma informāciju par grupu. Pārskatā var būt vairākas grupas kājenes sadaļas atkarībā no tā, cik grupēšanas līmeņus esat pievienojis. |
| Lapas kājene | Katras lapas beigās. | Izmantojiet lapas kājeni, lai drukātu lappušu numurus vai informāciju par katru lapu. |
| Pārskata kājene | Ziņojuma beigās. Piezīme. Noformējuma skatā pārskata kājene parādās zem lapas kājenes. Tomēr visos citos skatos (piemēram, izkārtojuma skatā vai kad atskaite tiek drukāta vai priekšskatīta) pārskata kājene tiek parādīta virs lapas kājenes, tieši aiz pēdējās grupas kājenes vai detalizētās rindiņas pēdējā lapā. | Izmantojiet atskaites kājeni, lai drukātu atskaites kopsummas vai citu kopsavilkuma informāciju visam pārskatam. |






## Atsauces Nr.

- [Introduction to reports in Access](https://support.microsoft.com/en-us/office/introduction-to-reports-in-access-e0869f59-7536-4d19-8e05-7158dcd3681c)
- [Designing Reports in Access](https://github.com/prijuly2000/DBMS/blob/master/DesigningReportsinAccess2010.pdf)

