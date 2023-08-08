{
  "date" : "2019-10-11",
  "keywords" :[ "fișier md", "format fișier md", "ce este un fișier md", "fișier", "exemplu md", "extensie fișier md", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MD - Fișier de limbă MarkDown",
  "description":"Aflați despre formatul de fișier MD și despre API-urile care pot crea și deschide fișiere MD.",
  "linktitle" : "MD",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier MD?

Fișierele text create cu dialectele limbii Markdown sunt salvate cu extensia de fișier **.md** sau **.MARKDOWN**. Fișierele MD sunt salvate în format text simplu, care utilizează limbajul Markdown, care include și simboluri de text în linie, definind modul în care un text poate fi formatat, cum ar fi indentări, formatarea tabelului, fonturile și anteturile. Fișierele MD pot fi convertite în HTML cu un program numit Markdown. Limbajul Markdown este lansat de John Gruber.

Fișierele MD pot fi, de asemenea, clasificate ca fișiere de dezvoltator, care sunt utilizate în principal de Markdown, pentru conversia fișierelor text în versiuni HTML, astfel încât utilizatorii să poată crea fișiere ușor de citit și scris. Următoarele sunt aplicațiile care pot deschide un fișier .md:

* Microsoft Notepad
* Notepad2
* Apple TextEdit
* Microsoft WordPad

Un cuvânt de precauție este că nu redenumiți extensia fișierelor .md. Dacă da, acest lucru nu va schimba tipul de fișier, deoarece există programe speciale de conversie disponibile pentru schimbarea unui fișier de la un tip la altul. După cum sa discutat mai sus, fișierele .MD sunt extensii ale fișierelor create de software-ul de limbaj Markdown. **Markdown** este un [limbaj de markup ușor](https://en.wikipedia.org/wiki/Lightweight_markup_language) destinat unui singur scop, pentru a fi utilizat pentru a formata textul pe web cu sintaxă de formatare a textului simplu. Să fie clar că Markdown nu este un înlocuitor pentru HTML, deoarece sintaxa acestuia este foarte mică, conținând un subset foarte mic de etichete HTML. Motivul din spatele Markdown este acela de a facilita citirea, scrierea și editarea prozei. Cu alte cuvinte, putem spune că HTML este un format de publicare, în timp ce Markdown este un format de scriere.

Markdown este acum unul dintre cele mai populare limbaje de marcare din lume. În timpul utilizării Microsoft Word, formatarea cuvintelor și expresiilor se face prin clic pe butoane, iar modificările sunt vizibile imediat. Dar Markdown nu este așa. Când este creat fișierul formatat Markdown, sintaxa Markdown este adăugată textului pentru a indica cuvintele și expresiile care pot arăta diferit. De exemplu, pentru a afișa un antet, înaintea acestuia este adăugat un semn numeric (de ex. # Heading One). Pentru a face o propoziție îngroșată, două asteriscuri sunt adăugate înainte și după ea (de exemplu, **acest text este aldine**). Sintaxa Markdown poate fi văzută după un timp în text.

## Scurt istoric

John Gruber și Aaron Swartz în 2004 au creat limbajul Markdown cu ideea de a permite oamenilor „să scrie folosind un format simplu de citit și scris simplu și cu opțiunea de a-l converti în XHTML sau HTML. Scopul din spatele designului său este lizibilitatea - limbajul este lizibil așa cum este, fără să arate ca a fost etichetat sau adăugat cu instrucțiuni de formatare, așa cum se face în limbaje de marcare precum RTF sau HTML, unde etichetele și instrucțiunile de formatare sunt evidente. Inspirația de bază este utilizarea convențiilor existente pentru marcarea textului simplu în e-mail.

De atunci Markdown a fost re-implementat de alții, la fel ca într-un [modul](https://en.wikipedia.org/wiki/Modular_programming) Perl disponibil pe [CPAN](https://en.wikipedia.org/wiki/CPAN) și în diverse alte limbaje de programare. Este distribuit sub o [licență în stil BSD](https://en.wikipedia.org/wiki/BSD_license) și este inclus cu sau disponibil ca plugin pentru mai multe [sisteme de gestionare a conținutului](https://en.wikipedia.org/wiki/Content_management_system).

## Specificatii tehnice

Când ceva este scris în Markdown, textul este mai întâi stocat într-un fișier text simplu cu o extensie de .md sau .markdown, apoi aplicația de markdown, cum ar fi Dillinger, este folosită pentru procesarea fișierului Markdown pentru a converti textul formatat Markdown în HTML pentru a-l afișa pe web. browsere. Aplicațiile Markdown utilizează un //procesor Markdown// (denumit în mod obișnuit „parser” sau „implementare”) pentru a prelua textul formatat Markdown și a-l scoate în format HTML. Diagrama de flux a procesului este următoarea:

Pe scurt, este un proces în patru etape, după cum urmează:

1. În primul rând, crearea fișierelor Markdown cu un editor de text sau cu o aplicație Markdown cu extensia .md sau .markdown.
1. Fișierul Markdown este apoi deschis într-o aplicație Markdown.
1. Aplicația Markdown este utilizată pentru a converti fișierul Markdown într-un document HTML.
1. Fișierul HTML este apoi vizualizat într-un browser web sau aplicația Markdown este folosită pentru a-l converti într-un alt format de fișier, cum ar fi PDF.

Markdown este rapid și ușor de luat note, de scriere de conținut pentru site-uri web, de a produce documente gata de tipărire, de a publica cărți, de a genera prezentări și de a crea documente.

Unele dintre versiunile din markdown au avut un impact substanțial asupra altor versiuni atât de mult încât le vom vedea adesea citate ca parte a altor versiuni. De exemplu, bibliotecile menționează suport pentru CommonMark (GFM). Să aruncăm o privire pe scurt la acestea.

### GFM
Markdown este atât de popular în rândul dezvoltatorilor, deoarece platforma de partajare open source Github a acceptat și a extins limbajul cu o versiune numită Github Flavoured Markup (GFM), care include blocuri de cod îngrădite, aultolinking URL, barare, tabele și crearea de sarcini.

### CommonMark
Dezvoltatorii Markdown au încercat recent să standardizeze markdown-ul, s-au unit pentru a crea o versiune, teste și documentație pentru limbajul care este mai robust și se numește CommonMark. Acest format este puțin nou și nu acceptă multe funcții, dar în curând vor fi adăugate multe funcții MultiMarkdown.

### Multi-Markdown
Multi-Markdown a adăugat diverse funcții la limbă, care sunt acceptate de alte versiuni. Inițial a fost scris în Perl, dar mai târziu a fost mutat în C. Acesta acceptă blocuri de cod îngrădite, evidențierea sintaxelor, tabele, metadate, fragmente/linkuri referințe încrucișate, note de subsol, baraj, liste de definiții, matematică.

## Referințe

* [Mastering MarkDown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

