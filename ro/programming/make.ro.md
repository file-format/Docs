{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Faceți fișierul - fișierul script Xcode Makefile",
  "description":"Aflați despre formatul XCode MakeFile și despre API-urile care pot crea și deschide fișiere MakeFile.",
  "linktitle" : "MAKE",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}


## Ce este un fișier MAKE?

Un fișier MAKE este un fișier script XCode care organizează compilarea codului. Este folosit pentru a compila și lega programe din mai multe fișiere de cod sursă. Acest lucru vă ajută să decideți care părți ale unei aplicații mari trebuie să fie recompilate atunci când aplicația trebuie actualizată. Faceți ca fișierele să utilizeze o serie de instrucțiuni pentru a rula în funcție de fișierele modificate.

## Exemplu de format de fișier MAKE

Următorul conținut este executat folosind utilitarul Make și ieșirile sunt după cum urmează.

```
hello:
	echo "hello world"
```
**Efectuați ieșire**

```
$ make
echo "hello world"
hello world
```

## Referințe
* [XCode and Make - Forumuri Apple](https://developer.apple.com/forums/thread/657458)
* [Ghid pentru obiectul C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

