{
  "date" : "2021-06-24",
  "keywords" :[ "PART", "μερική", "επέκταση", "αρχείο", "μορφή", "ιστός", "λήψη" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PART - Μερικώς ληφθέν αρχείο",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου PART και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία PART.",
  "linktitle" : "PART",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## Τι είναι ένα αρχείο PART; ##

Ένα αρχείο τμήματος ή επέκταση .part είναι ένα αρχείο που έχει ληφθεί μερικώς. Χρησιμοποιείται όταν οι λήψεις βρίσκονται σε εξέλιξη ή έχουν διακοπεί λόγω οποιουδήποτε προβλήματος, δίνοντας στον διαχειριστή λήψης την ευκαιρία να συνεχίσει τη λήψη όποτε είναι δυνατόν.
Αυτό σημαίνει ότι το πρόγραμμα περιήγησης, όπως ο Firefox ή τα προγράμματα μεταφοράς αρχείων όπως το eMule, το eMule plus, το FlashGet κ.λπ. αποθηκεύει ένα τμήμα του αρχείου, που ονομάζεται Part file, ενώ η λήψη πραγματοποιείται στη συσκευή σας. Αυτό το αρχείο τμήματος θα σας δείξει εάν η λήψη βρίσκεται σε εξέλιξη ή εάν έχει διακοπεί πριν από την ολοκλήρωση. Όχι μόνο αυτό, αλλά το αρχείο PART αποθηκεύει όλα τα δεδομένα μέχρι να ολοκληρωθεί η λήψη, γι' αυτό ορισμένα από αυτά μπορούν να συνεχιστούν αργότερα, εάν θέλετε να ξεκινήσετε ξανά τη λήψη.

## Μορφή αρχείου PART ##

There are few browsers that break large download files into smaller downloads and assign each portion a .part extension. These files can be seen in the “Download” folder. Once the download is finished, the browser will combine all the PART files to give a final downloaded file. For example, while downloading a file from Firefox, the download manager will store the data being downloaded in a PART file and replaces the name with certain characters, and add a .part extension at the end, such as **doodle.or** becomes **JKzMn.or.part**. After completion, Firefox will remove the .part extension and the file will be ready to launch.
