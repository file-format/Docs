{
  "date" : "2019-10-11",
  "keywords": [ "mf file", "mf", "extension", "format", "mf file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MF – Format fișier Java Manifest",
  "description":"Aflați despre formatul de fișier MF și despre API-urile care pot crea și deschide fișiere MF.",
  "linktitle" : "MF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Ce este un fișier MF?

Un fișier cu extensia .mf este un fișier Java Manifest care conține informații despre intrările individuale ale fișierului [JAR](/ro/programming/jar/). Fișierul MF în sine este conținut în fișierul JAR și oferă toată extensia și definiția legată de pachet. Fișierele JAR pot fi produse pentru a fi utilizate ca fișier executabil. În acest caz, fișierul mainfest specifică clasa principală a aplicației care conține instrucțiunea **`public static void main`**. Fișierele manifest sunt denumite MANIFEST.MF și pot fi deschise cu orice editor de text pe sistemele de operare Windows, MacOS și Linux.

## Specificații pentru formatul fișierului manifest

[Specificațiile formatului fișierului manifest](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) sunt disponibile de Oracle în ghidul lor pentru formatul de fișier JAR. Un fișier Manifest cuprinde secțiuni principale care sunt urmate de o listă de secțiuni pentru intrările individuale ale fișierului JAR. Fiecare secțiune respectă anumite reguli și restricții.

### Secțiunile principale

O secțiune principală:

* conține informații despre securitate și configurare despre fișierul JAR
* conține informații despre aplicația sau extensia din care face parte fișierul JAR
* definește atributele principale pentru fiecare articol individual de manifest

**Notă**: Niciun atribut din această secțiune nu poate fi numit „Nume”.

### Secțiuni individuale

O secțiune individuală definește diferite atribute pentru pachetele sau fișierele unui fișier JAR. Fiecare secțiune trebuie să înceapă cu un atribut numit „Nume” a cărui valoare trebuie să fie o cale relativă către fișier sau o adresă URL absolută care face referire la date din afara arhivei.

### Specificații Manifest

|Atribute|Descriere|
---|---|
|fișier-manifest|secțiune-principală noua linie *secțiune-individuală|
|secțiune-principală|informații-versiune linie nouă *atribut-principal|
|version-info|Manifest-Version : versiune-număr|
|număr-versiune|cifră+{.cifră+}*|
|principal-atribut|(orice atribut principal legitim) newline|
|individual-section|Nume : valoare newline *perentry-attribute|
|atribut-perentry|(orice atribut perentry legitim) newline|
|newline|CR LF | LF | CR (nu este urmat de LF)|
|cifra|{0-9}|

## Referințe

* [Oracle - Format de fișier JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html)
* [Format fișier JAR](https://en.wikipedia.org/wiki/JAR_(file_format))

