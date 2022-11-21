{
  "date" : "2021-05-24",
  "keywords" :["rjs", "File", "Extension", "File Format", "File Extension", "RJS", "Ruby Javascript File"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RJS - Ruby Javascript File",
  "description":"Μάθετε τι είναι η μορφή αρχείου RJS και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία RJS.",
  "linktitle" : "RJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Τι είναι ένα αρχείο RJS;

Ένα αρχείο με επέκταση .rjs είναι ένας συνδυασμός κώδικα Ruby και JavsScript που επιτρέπει στους προγραμματιστές του Rails να χρησιμοποιούν το Ruby για την παραγωγή δυναμικού κώδικα JavaScript. Ο κώδικας Ruby είναι ενσωματωμένος σε λειτουργίες Java και μεταγλωττίζεται στον διακομιστή ιστού που απαιτεί η μηχανή Ruby να εκτελείται στον διακομιστή. Το RJS είναι παρόμοιο με το [RHTML](/el/web/rhtml/); η μόνη διαφορά είναι ότι το πλευρικό περιέχει κώδικα Ruby σε [HTML](/el/web/html/) ενώ περιέχει κώδικα Ruby σε συναρτήσεις Javascript.

## Μορφή αρχείου RJS

Τα αρχεία RJS κωδικοποιούνται σε απλό κείμενο όπως κάθε άλλη γλώσσα προγραμματισμού ή δέσμης ενεργειών. Όταν μια τέτοια σελίδα ζητηθεί από τον πελάτη, ο κώδικας Ruby εκτελείται στον διακομιστή και μόνο ο κώδικας HTML και Javascript επιστρέφονται στο πρόγραμμα περιήγησης του πελάτη. Η σύνταξη του αρχείου RJS είναι παρόμοια με αυτή του συνδυασμού σύνταξης Ruby και JavaScript έτσι ώστε μόνο ο κώδικας Ruby είναι ενσωματωμένος στις συναρτήσεις JavaScript.

### Παράδειγμα RJS

Το παρακάτω παράδειγμα δείχνει έναν απλό κώδικα Ruby ανεξάρτητα και στη συνέχεια ενσωματωμένο σε μια συνάρτηση JavaScript.

```Ruby
### Default Ruby Functions

def foo
  "bar"
end
```

```JavaScript
# JS style which looks like JS

foo = -> { return "bar" }
```
και παρακάτω είναι το RubyJS:
```Ruby
# here you go!

foo = -> { "bar" }
```
## βιβλιογραφικές αναφορές

* [RJS](https://github.com/makevoid/rjs)

