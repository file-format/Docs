{
  "date" : "2021-07-29",
  "keywords" :[ "fișier md5", "format fișier md5", "ce este un fișier md5", "fișier", "exemplu md5", "extensie fișier md5", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MD5 - Fișier sumă de verificare MD5",
  "description":"Aflați despre fișierul MD5 și API-urile care pot crea și deschide fișiere MD5.",
  "linktitle" : "MD5",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## Ce este un fișier MD5?

Un fișier MD5 este un fișier de sumă de control utilizat pentru verificarea integrității unui fișier. Este similar cu o amprentă pentru fișierul asociat și este generat în mod unic folosind un algoritm care utilizează numărul de biți din fișier. Este folosit pentru a verifica fișierul cu software precum [md5sum](http://www.gnu.org/software/coreutils/manual/html_node/md5sum-invocation.html). Un avantaj al utilizării fișierelor MD5 este acela de a verifica dacă fișierele descărcate nu sunt corupte.

## Format de fișier MD5 - Mai multe informații

De obicei, un fișier MD5 este salvat cu același nume ca numele fișierului original, dar cu extensia .md5. De exemplu, dacă numele fișierului asociat este `abc_987_123456.grb`, numele fișierului MD5 corespunzător va fi `abc_987_123456.grb.md5`. Fișierele MD5 ajută la identificarea faptului că un fișier primit sau descărcat nu este corupt sau afectat de conținut rău intenționat. Pe scurt, fișierele MD5 garantează completitatea unui fișier.


## Cum se verifică suma de control MD5?

Un singur fișier poate fi verificat/verificat pentru MD5 utilizând instrumentul [md5sum](https://en.wikipedia.org/wiki/Md5sum), după cum urmează.

```
md5sum -c abc_987_123456.grb.md5
```

## Referințe

* [md5sum - Wikipedia](https://en.wikipedia.org/wiki/Md5sum)

