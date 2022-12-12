{
  "date" : "2021-24-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier MKS",
  "keywords" :[ "mks", "matroska video", "mkv format", "fișier", "format", "video"],
  "description":"Aflați despre formatul de fișier MKS pentru subtitrări create numai de Matroska și API-uri care pot crea și deschide fișiere MKS.",
  "linktitle" : "MKS",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-25-02"
}

## Ce este un fișier MKS?

Fișierele MKS sunt în general cunoscute ca fișiere Matroska care conțin numai subtitrări. Deși Matroska este un container de fișiere general, evită păstrarea informațiilor de formate specifice. Deoarece subtitrarile sunt folosite în unele dintre containerele audio sau video, Matroska acordă atenție stocării unor formate comune de subtitrare. Ajută Matroska să fie în concordanță cu rata de creștere. Trebuie să urmați punctele prezentate mai jos pentru a stoca subtitrările în Matroska:

- „.mks”. extensia va fi folosită de fișierul Matroska (conținând doar subtitrări).
- **CodecPrivate** este folosit pentru a stoca toate informațiile legate de codecuri care sunt globale pentru un întreg flux.
- Eliminați marcajele de timp de pornire și oprire care sunt utilizate într-un format de stocare nativ de marcaj de timp. În schimb, utilizați marcajul de timp Blocuri și Durata.
- Puteți folosi orice cu un strat transparent, inclusiv un videoclip.

## Formate comune de subtitrare

Iată câteva note scurte despre mai multe formate de subtitrare stocate în Matroska:

### Subtitrări imagini
Formatul de subtitrare VobSub este primul format de subtitrare de imagine importat în Matroska. Acest format este generat prin exportul subtitrarilor de pe un DVD. Piesele ar trebui separate în timpul stocării în Matroska dacă VobSub constă dintr-un set de fluxuri multiple.

### Subtitrări SRT
SRT este cel mai simplu și de bază dintre toate formatele de subtitrare. Este format din patru părți, după cum este prezentat mai jos:
 



1. Un număr care indică succesiunea subtitrării.
2. Timpul de apariție și dispariție a subtitrarilor pe ecran.
3. Subtitrarea în sine.
4. O linie goală pentru a indica începutul următoarei subtitrări.
 



### Subtitrări SSA/ASS
Sub Station Alpha (SSA) este un format de fișier folosit de popularul editor de subtitrări SubStation Alpha. Subtitrarile SSA sunt utilizate pe scară largă de către fansubbers. Are capacitatea de a afișa caracteristici moderne, de exemplu karaoke, poziționare, stil etc.
 



### Subtitrări WebVTT
World Wide Web Consortium (W3C) a dezvoltat WebVTT, care este abreviat ca „Web Video Text Tracks Format”. Acest format este utilizat pentru a marca resursele externe de urmărire text în legătură cu elementul HTML.

### Subtitrări grafice de prezentare HDMV
Formatul de subtitrare pentru grafică de prezentare HDMV (HDMV PGS) este o serie de hărți de biți și nu putem spune deloc text. Cu alte cuvinte, puteți spune că este doar o secvență cronometrată de imagini grafice. Pentru a extrage informațiile, conversia PGS în SRT este un proces necesar.

### Subtitrări text HDMV
Textul HDMV este cunoscut ca formatul de subtitrare textual folosit pe Blu-ray. Matroska permite doar setul de caractere UTF-8 Când stochează subtitrările TextST.

### Subtitrare Digital Video Broadcasting (DVB).
Formatul de subtitrare DVB a fost introdus pentru a reglementa transmiterea și afișarea mai multor limbi de subtitrare pe semnalele TV. Un format tipic de subtitrare ar permite oricărui spectator să urmărească transmisii subtitrate DVB, indiferent care este producătorul sistemelor de transmisie.


## Referințe ##

- [Matroska Subtitrări](https://www.matroska.org/technical/subtitles.html)

