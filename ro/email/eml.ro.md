{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EML - Mesaj de e-mail",
  "description":"Aflați despre formatul de fișier EML și despre API-urile care pot crea și deschide fișiere EML.",
  "linktitle" : "EML",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-16"
}

## Ce este un fișier EML?

Formatul de fișier EML reprezintă mesajele de e-mail salvate folosind Outlook și alte aplicații relevante. Aproape toți clienții de e-mail acceptă acest format de fișier pentru conformitatea cu standardul RFC-822 Internet Message Format. Microsoft Outlook este software-ul implicit pentru deschiderea tipurilor de mesaje EML. Fișierele EML pot fi folosite pentru salvarea pe disc, precum și pentru trimiterea către destinatari folosind protocoale de comunicare.

## Scurt istoric al EML

Specificațiile de format de fișier EML sunt disponibile conform [RFC 822](https://www.ietf.org/rfc/rfc0822.txt) Format standard. Înainte de RFC-822, RFC-733 a guvernat regulile de schimb de mesaje în rețea până în 1982, primul a fost creat ca o îmbunătățire a lateral prin stabilirea standardelor ARPA. În același timp, Microsoft și-a creat propriile module COM pentru dezvoltarea propriului client de e-mail, adică Outlook Express. RFC-822 a luat calea pentru a fi stabilit ca format proprietar atunci când Microsoft a deviat de la standardul deschis și a creat formatul de fișier [PST](/ro/email/pst/) în care e-mailurile sunt salvate într-un format de bază de date foarte structurat. Acest lucru a dus la probleme pentru utilizatorii clienților de e-mail non-Microsoft atunci când e-mailurile au fost redirecționate din Microsoft Outlook.

A fost în 2001 când standardul 822 a fost îmbunătățit la 2822 - Internet Message Format, care este utilizat în prezent pentru crearea, citirea și trimiterea mesajelor EML în format MIME RFC-822.

## Specificații pentru formatul fișierului EML

Fișierele EML cuprind două secțiuni distincte:

* Anteturi - Conține informații despre antetul mesajului
* Corpul mesajului - Conține o serie de informații care pot include conținutul mesajului, imagini încorporate și atașamente

### Informații anteturi ###

Un fișier EML constă din informații de antet și opțional corpul mesajului. Fiecare linie de antet din EML are două părți separate prin două puncte „:”. Primul se numește Header Name și cel care urmează după două puncte este header body. De exemplu, astfel de anteturi includ:

* Adresa de e-mail a expeditorului
* Adresa de e-mail destinatar
* Subiectul e-mailului
* Timpul și data mesajului

**Exemplu antet**

```
Din:<John@bmw.eml.light.com>

La:<Andy@fileformat.com>

Data: Joi, 8 Mar 2018 10:43:37 +0100

Subiect: bmw eml light
```

### Conținutul mesajului ###

Corpul mesajului EML conține informațiile principale ale e-mailului sub formă de text, hyperlinkuri și atașamente. Corpul e-mailului poate conține text simplu care poate fi citit, dar nu este necesar. În acest caz, corpul mesajului poate fi gol sau poate conține date codificate de atașamente.

Conținutul corpului mesajului este descris de tipul său de conținut, care permite aplicațiilor de citire să citească informațiile în formatele respective. Acesta reprezintă de fapt natura și formatul unui document. Structura unui tip MIME sau a unui tip de conținut este foarte simplă; este format dintr-un tip și un subtip, două șiruri de caractere, separate printr-un „/”. Nu este permis niciun spațiu. `Tipul` reprezintă categoria și poate fi un tip discret sau cu mai multe părți. `Subtipul` este specific fiecărui tip. Lista de tipuri, care se încadrează în categoria Content-Type, este lungă, dar unele tipuri importante de conținut sunt următoarele:


|**Tip**|**Descriere**|**Exemplu de subtipuri**
---|---|---|
|text|Reprezintă formatul care poate fi citit de om|text/plat, text/html, text/css, text/javascript
|imagine|Reprezintă o imagine de orice tip, cu excepția videoclipurilor|imagine/bmp, image/png, image/jpg, image/gif
|audio|Reprezintă orice format de fișier audio|audio/mdi, audio/wav
|aplicație|Reprezintă orice fel de date binare|application/octet-stream, application/vnd.mspowerpoint, application/xhtml+xml, application/xml, application/pdf

### Reprezentarea atașamentului în corpul EML ###

Corpul EML conține limite pentru fiecare tip de conținut pe care îl conține. Atașarea din corpul mesajului este identificată prin tipul de conținut și dispoziția conținutului, așa cum se arată în exemplul următor:

Tip de conținut: text/plan simplu; set de caractere#"windows-1252"; nume# „Apple App Store.txt”
Conținut-Dispoziție: atașament; nume fișier#"apple app store.txt"
Conținut-Transfer-Codificare: base64
X-Atașament-Id: f_jkhztmd02

După cum se poate vedea, setarea Content-Disposition la atașament permite aplicațiilor de citire să obțină informații despre atașament, cum ar fi numele fișierului atașat și codificarea transferului. Informațiile din antetul atașamentului sunt urmate de conținutul codificat al atașamentului care urmează să fie citit.

#### Exemplu de foaie de calcul ca atașament ####

Tip de conținut: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet; nume#"english_spodr.xlsx"
Conținut-Dispoziție: atașament; nume de fișier#"english_spodr.xlsx"
Conținut-Transfer-Codificare: base64
X-Atașament-Id: f_jkhztmd43

## Referințe

* [RFC 822](https://www.ietf.org/rfc/rfc0822.txt)

