{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Make File - Xcode Makefile Script File",
  "description":"Μάθετε για το XCode MakeFile Format και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία MakeFile.",
  "linktitle" : "MAKE",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}


## Τι είναι ένα αρχείο MAKE;

Ένα αρχείο MAKE είναι ένα αρχείο σεναρίου XCode που οργανώνει τη συλλογή κώδικα. Χρησιμοποιείται για τη μεταγλώττιση και τη σύνδεση προγραμμάτων από πολλαπλά αρχεία πηγαίου κώδικα. Αυτό βοηθά να αποφασίσετε ποια μέρη μιας μεγάλης εφαρμογής πρέπει να μεταγλωττιστούν εκ νέου όταν η εφαρμογή πρέπει να ενημερωθεί. Κάντε τα αρχεία να χρησιμοποιούν μια σειρά οδηγιών για εκτέλεση ανάλογα με τα αρχεία που έχουν αλλάξει.

## Παράδειγμα μορφής αρχείου MAKE

Τα ακόλουθα περιεχόμενα εκτελούνται χρησιμοποιώντας το βοηθητικό πρόγραμμα Make και οι έξοδοι είναι όπως ακολουθούν.

```
hello:
	echo "hello world"
```
**Κάντε έξοδο**

```
$ make
echo "hello world"
hello world
```

## βιβλιογραφικές αναφορές
* [XCode and Make - Apple Forums](https://developer.apple.com/forums/thread/657458)
* [Οδηγός Object-C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

