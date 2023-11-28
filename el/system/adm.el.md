{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Αρχείο ADM - Μορφή αρχείου προτύπου διαχείρισης",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου ADM και πώς να ανοίγετε αρχεία ADM.",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Τι είναι ένα αρχείο ADM;

Ένα αρχείο ADM είναι ένα αρχείο προτύπου που χρησιμοποιείται από το λογισμικό Microsoft Group Policies για να καθορίσει τη θέση των ρυθμίσεων πολιτικής που βασίζονται σε μητρώο στο αρχείο μητρώου. Χρησιμοποιείται από τους διαχειριστές συστήματος για τον καθορισμό της πολιτικής για τη διαχείριση μιας ομάδας υπολογιστών που αποτελούν μέρος της ομάδας. Αυτές οι πληροφορίες γίνονται μέρος των αντικειμένων πολιτικής ομάδας (GPO) που δημιουργούνται για τη διαχείριση της ομάδας.

Μπορείτε να ανοίξετε αρχεία ADM χρησιμοποιώντας το πρόγραμμα επεξεργασίας αντικειμένων πολιτικής ομάδας της Microsoft.

## Μορφή αρχείου ADM - Περισσότερες πληροφορίες

Τα αρχεία ADM αποθηκεύονται ως αρχεία κειμένου με μορφοποίηση unicode. Αυτά χρησιμοποιήθηκαν κυρίως για την περιγραφή της θέσης των ρυθμίσεων πολιτικής που βασίζονται σε μητρώο στα Windows Vista και στο μητρώο των Windows 7.

Τα αρχεία ADM δεν υποστηρίζονται πλέον και έχουν αντικατασταθεί από τα αρχεία [ADMX](/el/system/admx/). Το GPA αγνοεί τα ακόλουθα προεπιλεγμένα αρχεία ADM σε υπολογιστές με Microsoft Windows Vista Service Pack 1 ή νεότερη έκδοση.

* system.adm
* inetres.adm
* conf.adm
* wmplayer.adm
* wuau.adm

## βιβλιογραφικές αναφορές

* [Administrative Template Files - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - Διαχείριση αρχείων προτύπων διαχείρισης](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

