{
  "date" : "2021-07-20",
  "keywords" :["MJS", "File", "Extension", "File Format", "File Extension", "Node.js ES Module File"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Αρχείο Javascript MJS - Node.js ES Module",
  "description" :"Μάθετε τι είναι ένα αρχείο MJS και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχείο MJS.",
  "linktitle" : "MJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-20"
}

## Τι είναι ένα αρχείο MJS;

Ένα αρχείο με επέκταση .mjs είναι ένα αρχείο πηγαίου κώδικα JavaScript που χρησιμοποιείται ως ECMA Module (ECMAScript Module) στις εφαρμογές Node.js. Το σύστημα της μονάδας natvie του Node.js είναι το CommonJS που χρησιμοποιείται για τον διαχωρισμό του κώδικα σε διαφορετικά αρχεία για να διατηρείται οργανωμένος ο κώδικας [JS](/el/web/js/). Το MJS είναι ο μόνος τρόπος που χρησιμοποιείται από το Node.js για να προσδιορίσει εάν η λειτουργική μονάδα είναι CommonJS ή ES6. Οι μονάδες ECMAScript είναι τυπικές μορφές για τη συσκευασία κώδικα JavaScript για επαναχρησιμοποίηση. Τα αρχεία MJS μπορούν να ανοίξουν σε προγράμματα επεξεργασίας κειμένου όπως Atom, Vim, Apple xCode, Microsoft Visual Studio και Notepad.

## Μορφή αρχείου MJS - Περισσότερες πληροφορίες

Τα αρχεία MJS αποθηκεύονται σε δίσκο ως μορφή απλού κειμένου σε σύνταξη JavaScript. Αυτά μπορούν να ανοίξουν σε οποιοδήποτε πρόγραμμα επεξεργασίας κειμένου και είναι αναγνώσιμα από τον άνθρωπο. Από το 2018, σχεδόν όλα τα μεγάλα προγράμματα περιήγησης υποστηρίζουν πλέον ενότητες ES.

## Διαφορές μεταξύ μονάδων ES και CommonJS

Τι κάνει λοιπόν τα αρχεία MJS διαφορετικά από τα απλά αρχεία JS; Η διαφορά μεταξύ των μονάδων ES και του CommonJS μπορεί να συνοψιστεί ως εξής:

* Δεν απαιτείται, εξαγωγές ή module.exports
* Όχι \__όνομα αρχείου ή \__dirname
* Δεν υπάρχει φόρτωση μονάδας JSON
* Δεν υπάρχει φόρτωση εγγενούς μονάδας
* Δεν απαιτείται.επίλυση
* Όχι NODE_PATH
* Δεν απαιτείται.επεκτάσεις
* Δεν απαιτείται.cache

## βιβλιογραφικές αναφορές

* [Node.js ESM](https://nodejs.org/docs/latest/api/esm.html)
* [Διαφορά μεταξύ JS και MJS](https://nodejs.org/docs/latest/api/esm.html#esm_differences_between_es_modules_and_commonjs)

