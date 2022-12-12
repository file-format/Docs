{
  "date" : "2019-10-11",
  "keywords" :[ "mht", "fișier mht", "format fișier mht", "tip fișier mht", "fișier", "tip", "ce este un fișier mht"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHT - MIME HTML File Format",
  "description" :"Aflați despre formatul fișierului MHT și API-urile pentru a crea și deschide fișiere MHT.",
  "linktitle" : "MHT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## Ce este un fișier MHT?

Un fișier cu extensia .mht este un format de fișier de arhivare compatibil MIME care conține diferite tipuri de date într-un singur fișier. Poate stoca date precum text, imagini, stilul paginii sub formă de fișiere [CSS](/ro/web/css/), JavaScript și alte resurse ca resurse încorporate în el. Fișierele MHT, având tip MIME message/rfc822, încapsulează tot conținutul unui fișier HTML ca un singur fișier de arhivă pentru stocarea pe dispozitive de stocare. Aplicațiile software, cum ar fi Microsoft Word, vă permit să vă convertiți documentele WORD în MHT prin exportul ca fișier MHT. Fișierele MHT pot fi deschise folosind browsere populare, cum ar fi Microsoft Internet Explore și Google Chrome.

## Format de fișier MHT

La fel ca [MHTML](/ro/web/mhtml/), MHT este, de asemenea, o încapsulare MIME a documentelor HTML agregate. Conținutul documentului din interiorul unui document MHT, cum ar fi imaginile inline, foile de stil, applet-urile etc. sunt codificate MIME, unde acestea sunt legate la o resursă rădăcină prin intermediul URI-urilor. Clienții de e-mail, cum ar fi Microsoft Outlook, stochează e-mailurile (de obicei [EML](/ro/email/eml/)) în format de fișier MHT. Specificațiile complete ale formatului de fișier MHT sunt disponibile în [RFC 822](https://tools.ietf.org/html/rfc822) și pot fi consultate pentru dezvoltarea de aplicații software care pot procesa fișiere MHT.

## Diferența dintre MHT și MHTML

În timpul salvării unei pagini online, utilizatorului i se cere să stabilească tipul de format de fișier în care pagina online trebuie să fie salvată pe sistemul nativ. Cel mai adesea, utilizatorul se confundă între limbajul de marcare și formatele de fișiere MHTML. Ei observă că este supărător să vadă că formatul de fișier este mai sănătos între acestea.

Când un utilizator decide să evite irosirea paginii online ca limbaj de marcare, se formează un folder, care conține mai multe fișiere pentru diferite conținuturi ale paginii, adică unități de zonă de fișiere total diferite create pentru text, grafică, applet-uri etc. Pe de altă parte, salvarea pagina online ca MHTML creează un fișier pentru pagina online completă. Toate elementele paginii împreună cu grafica, legăturile și fișierele alternative sunt încorporate într-un singur fișier.

Desigur, este ușor să gestionați fișierele MHT sau MHTML, deoarece fișierul, care poate fi protejat și partajat pur și simplu prin e-mail. Cu toate acestea, unitatea de zonă a fișierelor de limbaj de marcare sub șansa de pierdere a informațiilor, deoarece pierderea sau ștergerea chiar și a unui fișier ar putea produce folderul complet de limbaj de marcare inutil pentru utilizator.

## Referințe

* [MHTML - Wikipedia](https://en.wikipedia.org/wiki/MHTML)
* [MHT RFC](https://tools.ietf.org/html/rfc822)

