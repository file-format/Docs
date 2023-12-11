{
"data": "2023-05-31",
  "keywords": [
"fișier desktop",
"Ce este un fișier desktop",
"ce conține fișierul desktop",
"exemplu de fișier desktop",
"cum se deschide fișierul desktop",
"care este formatul fișierului desktop",
"fişier",
"extensie fișier desktop",
"extensie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format de fișier DESKTOP - fișier de intrare pe desktop",
  "description":"Aflați despre formatul DESKTOP și despre API-urile care pot crea și deschide fișiere DESKTOP.",
  "linktitle": "DESKTOP",
  "menu": {
    "docs": {
      "identifier": "settings-desktop",
      "parent": "settings"
}
},
"lastmod": "2023-05-31"
}

## Ce este un fișier DESKTOP?

Un fișier .desktop este un fișier de configurare utilizat de mediile desktop Linux pentru a defini comenzile rapide și lansatoarele de aplicații. Oferă metadate despre o aplicație, cum ar fi numele, pictograma, comanda de executat și alte proprietăți. Aceste fișiere sunt de obicei folosite pentru a crea comenzi rapide în meniurile aplicațiilor, lansatoarele desktop sau panourile în sistemele bazate pe Linux.

## Ce conține fișierul DESKTOP?

Un fișier .desktop urmează un anumit format și conține mai multe câmpuri cheie:

- **[Intrare desktop]:** Acesta este antetul secțiunii principale pentru fișierul .desktop.
- **Nume:** Specifică numele aplicației.
- **Comentariu:** Oferă o scurtă descriere sau comentariu despre aplicație.
- **Exec:** Definește comanda de executat la lansarea aplicației.
- **pictogramă:** specifică calea către fișierul pictogramă asociat cu aplicația.
- **Terminal:** Specifică dacă aplicația ar trebui să fie rulată într-o fereastră de terminal.
- **Tip:** Specifică tipul de intrare, cum ar fi "Aplicație" sau "Link".
- **Categorii:** Specifică categorii sau grupuri în care aplicația ar trebui să fie afișată în meniu.
- **StartupNotify:** Specifică dacă mediul desktop ar trebui să afișeze o notificare de pornire pentru aplicație.
- **NoDisplay:** Specifică dacă aplicația ar trebui să fie ascunsă din meniuri.
- **Acțiuni:** Definește acțiuni suplimentare care pot fi efectuate pe aplicație, cum ar fi deschiderea unui anumit fișier.

## Exemplu de fișier DESKTOP

Iată un exemplu de fișier .desktop pentru un editor de text fictiv numit "MyTextEditor":

```
[Desktop Entry]
Name=MyTextEditor
Comment=A simple text editor
Exec=mytexteditor %F
Icon=/path/to/icon.png
Terminal=false
Type=Application
Categories=TextEditor;Utility;
StartupNotify=true
NoDisplay=false
Actions=OpenNewWindow;OpenExistingFile;

[Desktop Action OpenNewWindow]
Name=Open New Window
Exec=mytexteditor

[Desktop Action OpenExistingFile]
Name=Open Existing File
Exec=mytexteditor %U
```

În acest exemplu, fișierul .desktop definește aplicația "MyTextEditor" cu proprietățile asociate. De asemenea, include două acțiuni suplimentare, "Deschide o fereastră nouă" și "Deschide fișier existent", care pot fi accesate din meniul contextual al lansatorului de aplicații.

Prin plasarea unui fișier .desktop în directoare specifice, cum ar fi `/usr/share/applications` sau `~/.local/share/applications`, mediul desktop îl va recunoaște și va afișa aplicația în mod corespunzător în meniuri sau va permite lansarea acesteia din desktop.

## Cum se deschide fișierul DESKTOP?

Mai multe programe software pot deschide și gestiona fișiere .desktop. Aceste programe sunt de obicei manageri de fișiere sau medii desktop pe sisteme bazate pe Linux. Aici sunt cateva exemple:

- **Nautilus (Fișiere):** Managerul de fișiere implicit pentru mediul desktop GNOME.
- **Nemo:** Managerul de fișiere pentru mediul desktop Cinnamon.
- **Dolphin:** Managerul de fișiere implicit pentru mediul desktop KDE Plasma.
- **Thunar:** Managerul de fișiere implicit pentru mediul desktop Xfce.
- **Editor de meniu KDE:** Un instrument specific mediului desktop KDE Plasma care vă permite să vizualizați și să editați fișiere .desktop.

Acești manageri de fișiere și medii desktop oferă o interfață grafică pentru gestionarea fișierelor .desktop. Acestea vă permit să vizualizați și să editați proprietățile fișierelor .desktop, să creați lansatoare de aplicații și să organizați comenzi rapide în meniurile aplicațiilor sau pe desktop.

Fișierele .desktop sunt fișiere text simplu, așa că le puteți deschide și edita și cu un editor de text la alegere. Pur și simplu faceți clic dreapta pe fișierul .desktop și selectați "Deschide cu" sau "Deschide cu altă aplicație" pentru a alege un editor de text din lista de programe instalate.

## Care este formatul fișierului DESKTOP?

Formatul de fișier .desktop urmează o structură și un format specific. Este un fișier text simplu cu un set de perechi cheie-valoare organizate în secțiuni. Iată o prezentare generală a formatului:

- **Anteturi de secțiune:** Fiecare secțiune începe cu un antet cuprins între paranteze drepte ([]). Secțiunea principală este de obicei numită [Desktop Entry], care conține metadatele principale pentru aplicație sau lansator.
- **Perechi cheie-valoare:** în cadrul fiecărei secțiuni, definiți proprietăți folosind perechi cheie-valoare. Formatul este "Cheie=Valoare". Cheia identifică proprietatea, iar valoarea furnizează datele corespunzătoare.
- **Sintaxa proprietății:** Valorile proprietăților pot fi de diferite tipuri, inclusiv șiruri de caractere, valori booleene, căi de fișiere sau liste. Formatul pentru fiecare valoare de proprietate depinde de tipul acesteia.
- **Comentarii:** Puteți include comentarii în fișierul .desktop folosind simbolul "#". Orice lucru care urmează pe linia "#" este considerat un comentariu și este ignorat.

## Referințe
* [Fișiere de intrare desktop](https://www.baeldung.com/linux/desktop-entry-files)

