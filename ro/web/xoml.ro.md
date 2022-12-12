{
  "date" : "2019-10-11",
  "keywords" :["xoml", "Fișier", "Extensie", "Format fișier", "Extensie fișier", "Limbajul de marcare a obiectelor extensibile"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XOML – Windows Workflow File Format",
  "description":"Aflați despre formatul de fișier XOML și despre API-urile care pot crea și deschide fișiere XOML.",
  "linktitle" : "XOML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier XOML?

XOML este acronim pentru Extensible Object Markup Language și este un format de serializare pentru obiectele de flux de lucru ale Windows Workflow Foundation. Bazat pe **[XAML](/ro/web/xaml/)**, este folosit în principal pentru crearea de interfețe cu utilizatorul în format simplu **[XML](/ro/web/xml/)**. Acestea sunt folosite pentru a declara fluxul de lucru pentru interfața utilizator și sunt compilate împreună cu fișierul separat care conține logica de implementare. Conține o structură bazată pe arbore care definește un nod de flux de lucru rădăcină, sub-elemente imbricate și segmente de cod încorporate. Când se creează un nou flux de lucru cu Visual Studio pentru .NET, acesta are o opțiune de a alege dacă ar trebui să fie în format Cod sau format Separat prin cod. În cazul în care îl selectați pe cel mai târziu, IDE-ul va crea două fișiere pentru dvs.; unul în format XOML (constând din aspectul fluxului de lucru și setări), iar celălalt este în formatul [.CS](/ro/programming/cs/)/[.VB](/ro/programming/vb/) în care se află codul de programare.

