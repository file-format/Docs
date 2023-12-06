{
"data":"2023-11-01",
   "keywords":[
"pat",
"fișier pat",
"fișier de instalare a managerului de stație de disc pat",
"cum se deschide un fișier pat",
"fişier",
"extensia fișierului pat",
"extensie",
"fişier"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"Format fișier PAT - Fișier de instalare DiskStation Manager",
   "description":"Aflați despre formatul fișierului de instalare PAT DiskStation Manager și despre API-urile care pot crea și deschide fișiere PAT.",
"linktitle":"PAT",
   "menu":{
      "docs":{
         "identifier":"system-pat-diskstation",
         "parent":"system"
}
},
"lastmod":"2023-11-01"
}

## Ce este un fișier PAT?

Un fișier PAT este asociat în mod obișnuit cu **DiskStation Manager (DSM)**, sistemul de operare utilizat de dispozitivele Synology Network-Attached Storage (NAS). Fișierul PAT este un fișier de instalare utilizat pentru a actualiza sau instala DSM pe un Synology NAS.

## Utilizarea fișierului PAT

Iată cum utilizați de obicei un fișier PAT pentru a instala sau actualiza DSM pe Synology NAS:

1. Descărcați fișierul PAT: Puteți obține fișierul PAT de pe site-ul oficial Synology sau din alte surse de încredere.
    







2. Conectați-vă la NAS: Accesați interfața de utilizator bazată pe web a Synology NAS introducând adresa IP într-un browser web. Veți avea nevoie de privilegii de administrator pentru a efectua această operațiune.
    







3. Accesați Centrul de pachete: în interfața web, navigați la "Centrul de pachete". Aici gestionați și instalați aplicații pe NAS.
    







4. Instalare manuală: În Centrul de pachete, ar trebui să existe o opțiune pentru "Instalare manuală" sau "Instalare/Actualizare", în funcție de versiunea DSM pe care o utilizați. Alegeți această opțiune.
    







5. Căutați fișierul PAT: vi se va solicita să căutați fișierele locale și să selectați fișierul PAT descărcat.
    







6. Instalați sau actualizați: După ce selectați fișierul PAT, urmați instrucțiunile de pe ecran fie pentru a instala DSM (dacă este o instalare nouă) fie pentru a actualiza DSM (dacă faceți upgrade la o versiune mai nouă).
    







7. Așteptați finalizarea: procesul de instalare sau actualizare poate dura ceva timp, iar NAS-ul dvs. se poate reporni ca parte a procesului. Ai răbdare și așteaptă să se termine.
    







8. Configurare post-instalare: După instalare sau actualizare, poate fi necesar să configurați setările NAS în funcție de preferințele dvs.

## Manager DiskStation

DiskStation Manager, adesea abreviat ca DSM, este un sistem de operare dezvoltat de Synology pentru dispozitivele lor Network-Attached Storage (NAS). Acesta servește ca interfață de management și control pentru serverele Synology NAS. DiskStation Manager oferă o interfață web ușor de utilizat, care permite utilizatorilor să configureze și să gestioneze diverse aspecte ale NAS-ului lor, cum ar fi stocarea datelor, partajarea fișierelor, soluții de backup, servicii multimedia și multe altele.

DSM este cunoscut pentru versatilitatea și ecosistemul său extins de pachete, care le permite utilizatorilor să instaleze și să ruleze diverse aplicații și servicii pe Synology NAS, transformându-l într-un server multifuncțional atât pentru uz casnic, cât și pentru afaceri. Unele dintre funcționalitățile comune ale DiskStation Manager includ partajarea de fișiere, backup și sincronizare a datelor, streaming media, caracteristici de securitate și suport pentru virtualizare.

Synology lansează în mod regulat actualizări și versiuni noi de DSM pentru a îmbunătăți securitatea, performanța și funcțiile. Utilizatorii pot actualiza manual DSM folosind fișiere PAT sau pot configura actualizări automate pentru a se asigura că NAS-ul lor rulează cea mai recentă și mai sigură versiune a DiskStation Manager.

## Cum se deschide un fișier PAT

Pentru a actualiza manual DiskStation Manager, puteți utiliza un fișier PAT pe care l-ați descărcat din Synology Download Center, urmând următorii pași:

1. Accesați Panoul de control DiskStation Manager.
2. Navigați la secțiunea "Actualizare și restaurare" și alegeți "Actualizare DSM".
3. De acolo, selectați "Actualizare manuală DSM".
4. Faceți clic pe butonul "Răsfoiți", apoi localizați și alegeți fișierul PAT pe care l-ați descărcat.
5. Pentru a iniția actualizarea DiskStation Manager, faceți clic pe butonul "Aplicare".

## Referințe
* [Synology](https://en.wikipedia.org/wiki/Synology)
