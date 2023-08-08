{
  "date" : "2019-12-12",
  "keywords" :[ "JT", "fișier", "extensie", "format", "3D fbx", "" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier JT și despre API-urile care pot crea și deschide fișiere JT.",
  "title" :"JT - Jupiter Tessellation File Format",
  "linktitle" : "JT",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier JT?

**JT** (Jupiter Tessellation) este un format de date 3D standardizat ISO eficient, axat pe industrie și flexibil, dezvoltat de Siemens PLM Software. Domeniile CAD mecanice din industria aerospațială, industria auto și echipamentele grele folosesc JT ca cel mai important format de vizualizare 3D.

Formatul JT este un grafic al scenei care acceptă atributele și nodurile care sunt specifice CAD. Tehnici sofisticate de compresie sunt folosite pentru a stoca date fațete (triunghiuri). Acest format este structurat pentru a suporta atribute vizuale, informații despre produse și producție (PMI) și metadate. Există un suport bun pentru streaming asincron de conținut. În industria mecanică grea, profesioniștii folosesc fișierul JT în soluțiile CAD și în programele software de management al ciclului de viață al produsului (PLM) pentru a examina geometria mărfurilor complicate.

Deoarece JT acceptă aproape toate formatele importante CAD 3D, ansamblul său poate face față unei varietăți de combinații cunoscute sub numele de „multi-CAD”. Acest ansamblu multi-CAD este întotdeauna bine gestionat și actualizat, deoarece sincronizarea între fișierele native de descriere a produsului CAD cu fișierele JT asociate are loc automat. Fișierele JT sunt inițial ușoare, așa că sunt considerate potrivite pentru colaborările pe internet. Companiile colaborează prin trimiterea de vizualizări 3D pe medii mult mai ușor în comparație cu fișierele CAD originale „grele”. În plus, fișierele JT asigură multe caracteristici de securitate care fac partajarea proprietății intelectuale mai sigură.

## Scurt istoric al formatului de fișier JT

Engineering Animation, Inc. și Hewlett Packard au fost designerii originali ai JT, care au dezvoltat acel format ca setul de instrumente Direct Model. După ce EAI a fost achiziționat de UGS Corp. JT a devenit parte a suitei UGS. La începutul anului 2007, UGS a anunțat JT ca format principal 3D. În același an, Siemens AG a achiziționat UGS și s-a dovedit a fi Siemens PLM Software. Siemens folosește JT ca format comun de interoperabilitate și format de arhivare a datelor. În 2009, ISO a acceptat specificația JT pentru publicare ca specificație ISO disponibilă public (PAS). La mijlocul anului 2010, ProSTEP iViP a anunțat că la nivel industrial, JT și STEP AP 242 XML pot fi utilizate împreună pentru a obține avantajul maxim în date. scenarii de schimb. În 2012, JT a fost declarat oficial ca format de vizualizare 3D standardizat ISO (ISO 14306:2012 (ISO JT V1)).

## Format fișier JT ##

Toate obiectele în format JT sunt reprezentate printr-un identificator de obiect, iar referințele dintre obiecte sunt gestionate prin identificatorul obiectului referit. Integritatea acestor referințe la obiect poate fi menținută prin dezactivarea/swizzling-ului de pointeri.

Un fișier JT este aranjat ca o serie de blocuri, iar blocul antet este întotdeauna primul bloc de date din fișier. O serie de segmente de date și un segment TOC urmează imediat blocul antet. Segmentul de date (6 segment LSG) posedă un fișier JT conform referințelor, există întotdeauna. Segmentul TOC conține informații despre locația tuturor celorlalte Segmente de date ale acelui fișier.

{{< figure src="../JT-1.png" alt="Format de fișier JT" >}}

### Antet fișier ###

Antetul fișierului este primul bloc din ierarhia de date a fișierului JT. Informațiile de versiuni și informațiile despre locația TOC sunt incluse în antet, ceea ce facilitează citirea fișierelor de încărcare. Conținutul antetului fișierului este aranjat după cum urmează.

### Segment TOC ###

Segmentul TOC trebuie să existe într-un fișier și să conțină informații de identificare și locație ale tuturor celorlalte segmente de date. Locația reală a Segmentului TOC este specificată de câmpul Offset TOC din antetul fișierului. Fiecare Segment de date adresabil individual este reprezentat de intrarea TOC într-un segment de TOC.

### Segment de date ###

Fișierul JT definește toate datele stocate într-un segment de date. Unele segmente de date pot comprima toți octeții de date de informații rămase în cadrul segmentului. Segmentele de date au următoarea structură:

![alt text](../JT-2.png "JT Data Segment")

Următorul tabel descrie diferite tipuri de segmente de date:

|Nume|Descriere
---|---|
|Segment LSG|Cuprinde o colecție de obiecte legate prin referințe direcționate pentru a forma LSG (structură de grafic aciclică direcționată)
|Segmentul LOD de formă|conține datele definitorii pentru formele geometrice (de ex. vârfuri, normale, poligoane etc.)
|JT B-Rep Segment|Are element pentru date pentru a reprezenta limita geometrică precisă pentru o porțiune individuală în format JT B-Rep.
|XT B-Rep segment|Aveți element pentru date care să reprezinte limita geometrică precisă pentru o porțiune individuală în format de reprezentare a limitei
|Segment wireframe|Datele reprezintă un wireframe 3D precis pentru o anumită porțiune este definită de un element conținut în acest segment.
|Segment de metadate|Permite stocarea metadatelor în segmente adresabile distincte.
|Segment JT ULP|Avand element pentru date care sa reprezinte limita geometrica semi-precisa pentru o portiune individuala in format JT ULP.
|JT LWPA segment|Conține un element de definire a datelor analitice pentru o anumită piesă. LWPA include colecția de suprafețe analitice în definiția b-rep a piesei.

## compresie ##

Cerințele de transmisie și stocare ale modelelor 3D sunt mai solicitante, așa că fișierele JT pot beneficia de compresie. Un model de date JT poate fi compus din diferite fișiere folosind tehnici de compresie diferite, dar procesul de comprimare este transparent pentru utilizatorul de date JT.

Până acum, JT Open Toolkit (ca standard) și compresia avansată sunt două tehnici de compresie utilizate de fișierele JT. JT Open Toolkit folosește un algoritm de compresie ușor, fără pierderi, în timp ce compresia avansată folosește o tehnică de compresie mai rafinată, specifică domeniului, care duce la compresia geometriei cu pierderi. Aplicațiile client preferă compresia avansată decât utilizarea compresiei standard, deoarece compresia avansată oferă rapoarte de compresie destul de mari. Compatibilitatea cu aplicațiile obișnuite de vizualizare a fișierelor JT este menținută prin furnizarea de compresie standard. Formularul de compresie trebuie să fie compatibil cu versiunea formatului de fișier JT, care poate fi văzută atunci când un fișier JT se deschide folosind un editor de text și este inclus în informațiile antetului ASCII.

## Referințe ##

* [JT File Format Reference](https://www.plm.automation.siemens.com/en_us/Images/JT-v10-file-format-reference-rev-B_tcm1023-233786.pdf)
* [JT (format de vizualizare)](https://en.wikipedia.org/wiki/JT_(visualization_format)#Data_model)

