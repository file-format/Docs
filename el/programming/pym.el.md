---
date: 2022-05-09
συγγραφέας:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Μορφή αρχείου PYM - Αρχείο προεπεξεργαστή μακροεντολών PYM
linktitle: PYM
description: "Μάθετε για τη μορφή αρχείου PYM και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία PYM."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Τι είναι ένα αρχείο PYM;

Ένα αρχείο PYM είναι ένα αρχείο προεπεξεργαστή μακροεντολών που βασίζεται στη γλώσσα προγραμματισμού Python. Αναπτύχθηκε από την VRVis Research και αποθηκεύει συντομεύσεις μακροεντολών. Όταν το αρχείο PYM ερμηνεύεται από το στάδιο προεπεξεργασίας του διερμηνέα Python, αυτές οι συντομεύσεις επεκτείνονται ως αντικαταστάσεις για το πλήρες κείμενό τους. Επιπλέον, μια τρίτη, προαιρετική λειτουργία που μπορεί να εκτελεστεί από έναν προεπεξεργαστή μακροεντολών είναι η συμπερίληψη αρχείων. Τα αρχεία PYM μπορούν να ανοίξουν σε προγράμματα επεξεργασίας κειμένου όπως το Notepad, το Notepad++, το Apple TextEdit και το VI στο Linux.

## Μορφή αρχείου PYM

Τα αρχεία PYM αποθηκεύονται ως αρχεία απλού κειμένου σε δίσκο. Ένα αρχείο PYM μπορεί επίσης να περιλαμβάνει άλλα αρχεία χρησιμοποιώντας την οδηγία «#include».

### Σύνταξη PYM

Οι δηλώσεις PYM περιλαμβάνονται μεταξύ των δεικτών ""#begin python και "#end python", όπως φαίνεται παρακάτω.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### Επέκταση μακροεντολής PYM

Η επέκταση μακροεντολής PYM αντιπροσωπεύεται από δύο ακολουθίες, π.χ. <[ και ]>. Αυτές είναι ειδικές ετικέτες html και μπορούν να εμφανιστούν οπουδήποτε σε μια γραμμή. Ένα μικρό παράδειγμα PYM είναι το ακόλουθο.

```
#begin python
TITLE = "My Web page"
def EXP(e): return str(e)
#end python
<head>
<title><[TITLE]></title>
</head>
<body>
<h4><[TITLE]></h4>
<p>The value of 2 raised to the 4th power is <[EXP(2**4)]>.</p>
</body>
```

Το αποτέλεσμα της εκτέλεσης αυτού μέσω του PYM είναι το εξής:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## Βιβλιογραφικές αναφορές ##

* [PYM - Ένας προεπεξεργαστής μακροεντολών που βασίζεται στην Python](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
* [PYM Interpreters](https://github.com/interpreters/pym)

