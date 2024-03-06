{
   "date":"2023-11-09",
   "keywords":[
"zoodārzs",
"zoodārza fails",
"zoo saspiests fails",
"kā atvērt zoodārza failu",
"failu",
"zoo faila paplašinājums",
"pagarinājumu",
"failu"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"ZOO fails — kas ir .zoo fails un kā to atvērt?",
   "description":"Uzziniet par ZOO saspiesto failu formātu un API, kas var izveidot un atvērt ZOO failus.",
   "linktitle":"ZOO",
   "menu":{
      "docs":{
         "identifier":"compression-zoo-lv",
         "parent":"compression"
}
},
   "lastmod":"2023-11-09"
}

## Kas ir ZOO fails?

.zoo fails ir arhīva formāts, ko izmanto failu un direktoriju saspiešanai un glabāšanai; ir līdzīgs citiem arhīvu formātiem, piemēram, .zip, .tar un .rar. Formāts .zoo” bija populārs skaitļošanas sākumposmā, taču pēdējos gados tas ir kļuvis mazāk izplatīts. Sākotnēji to izstrādāja **Rahul Dhesi**, un to galvenokārt izmantoja Unix un DOS sistēmās.

.zoo failā parasti ir viens vai vairāki faili un direktoriji, kas ir saspiesti un arhivēti vienā failā. Varat izveidot un izvilkt `.zoo` failus, izmantojot dažādus programmatūras rīkus, kas atbalsta šo formātu.

ZOO arhīviem ir unikāla funkcija, kas ļauj glabāt vairākas viena faila versijas, ja katra versija tika modificēta citā datumā. Tas nozīmē, ka ZOO lietotāji var saglabāt un piekļūt iepriekšējām faila iterācijām tieši no ZOO arhīva. Šī funkcija ļauj lietotājiem atgriezties pie iepriekšējās faila versijas vai salīdzināt vecāku versiju ar jaunāku, piedāvājot ērtu veidu, kā pārvaldīt failu pārskatīšanu un izmaiņas laika gaitā.

## Kopējās ZOO failu darbības

Šeit ir dažas izplatītas darbības, kas saistītas ar `.zoo` failiem:

1.  **.zoo faila izveide:** varat izmantot komandrindas utilītu, piemēram, zoo, lai izveidotu .zoo failu. Piemēram, šī komanda izveidos `.zoo` arhīvu no direktorija:
    
`zoo a -c arhīvs.zoo direktorijs/`
    
Šajā komandā a apzīmē pievienot, -c norāda saspiešanu un archive.zoo ir izvades arhīva nosaukums.
    
2.  **Failu izvilkšana no .zoo faila:** Lai izvilktu .zoo arhīva saturu, varat izmantot šādu komandu:
    
`zoo e arhīvs.zoo`
    
Šī komanda izvilks failus no faila archive.zoo.
    
3.  **Zoo faila satura uzskaitīšana:** Varat uzskaitīt .zoo arhīva saturu, to neizvelkot, izmantojot opciju l.
    
    
`zoo l arhīvs.zoo`

## Kā atvērt ZOO failu?

Programmas, kas atver ZOO failus, ietver

- **zoodārzs** (bezmaksas) operētājsistēmai Windows, Linux

## Atsauces
* [Zoo (file format)](https://en.wikipedia.org/wiki/Zoo_(file_format))
