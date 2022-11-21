
{
  "date" : "2021-12-14",
  "keywords": [ ".abc file", "extension", "format","ActionScript Byte Code File", "how to open .abc file","abc file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABC - ActionScript Byte Code File",
  "description":"Μάθετε τι είναι η μορφή αρχείου ABC με παραδείγματα και API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία ABC.",
  "linktitle" : "ABC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-14"
}

## Τι είναι ένα αρχείο ABC;

Ένα αρχείο με επέκταση .abc είναι ένα αρχείο κώδικα ActionScript Byte που δημιουργήθηκε από τον μεταγλωττιστή Flash ως αποτέλεσμα της μεταγλώττισης των αρχείων σεναρίου ActionScript. Ο κώδικας byte που περιέχεται στο αρχείο ABC εκτελείται από την εικονική μηχανή ActionScript (AVM και AVM2). Ο κώδικας byte αποτελείται από σταθερά δεδομένα, οδηγίες από το σύνολο εντολών AVM2 και διάφορα είδη μεταδεδομένων. Όταν ένα αρχείο ABC φορτώνεται στο AVM ή στο AVM2, υποβάλλεται σε επαλήθευση. Εάν δεν συμμορφώνεται με την Επισκόπηση AVM2, απορρίπτεται. Τα αρχεία ABC μπορούν να ανοίξουν στο Adobe Flash Player που έχει διακοπεί εδώ και πολύ καιρό.

## Μορφή αρχείου ABC - Περισσότερες πληροφορίες

Τα αρχεία ABC αποθηκεύονται σε δίσκο σε μορφή δυαδικού αρχείου που είναι αναγνώσιμα από εικονικές μηχανές AVM ή AVM2. Η εσωτερική δομή του αρχείου αντιπροσωπεύει το μπλοκ εκτελέσιμου κώδικα με όλα τα σταθερά δεδομένα, τους περιγραφείς τύπων, τον κώδικα και τα μεταδεδομένα.

## Δομή αρχείου ABC

Η δομή του αρχείου ABC είναι όπως φαίνεται παρακάτω.

```
abcFile  
{
           u16        minor_version                
           u16        major_version                
           cpool_info        constant_pool                
           u30        method_count                
           method_info        method[method_count]                
           u30        metadata_count                
           metadata_info        metadata[metadata_count]                
           u30        class_count                
           instance_info        instance[class_count]                
           class_info        class[class_count]                
           u30        script_count                
           script_info        script[script_count]               
           u30        method_body_count                
           method_body_info        method_body[method_body_count]        
}
```

### Πεδία αρχείου ABC

|Όνομα πεδίου|Περιγραφή|
---|---|
|minor_version, major_version|Οι τιμές των major_version και minor_version είναι οι αριθμοί κύριας και δευτερεύουσας έκδοσης της μορφής abcFile.|
|constant_pool|Η συγκέντρωση_constant είναι μια δομή μεταβλητού μήκους που αποτελείται από ακέραιους, διπλούς, συμβολοσειρές, χώρους ονομάτων, σύνολα χώρων ονομάτων και πολλά ονόματα.|
|method_count, μέθοδος|Η τιμή ofmethod_count είναι ο αριθμός των καταχωρήσεων στον πίνακα μεθόδων. Κάθε καταχώρηση στον πίνακα μεθόδων είναι μια δομή μεταβλητού μήκους method_info.|
|metadata_count, metadata|Η τιμή του metadata_count είναι ο αριθμός των καταχωρήσεων στον πίνακα μεταδεδομένων. Κάθε καταχώρηση μεταδεδομένων είναι μια δομή μεταδεδομένων_πληροφοριών που αντιστοιχίζει ένα όνομα σε ένα σύνολο τιμών συμβολοσειράς. |
|class_count, instance, class|Η τιμή του class_count είναι ο αριθμός των καταχωρήσεων στους πίνακες παρουσίας και κλάσης. |
|script_count, script|Η τιμή του script_count είναι ο αριθμός των καταχωρήσεων στον πίνακα σεναρίων. Κάθε καταχώρηση σεναρίου είναι μια δομή script_info που καθορίζει τα χαρακτηριστικά ενός σεναρίου σε αυτό το αρχείο. |
|method_body_count, method_body|Η τιμή του method_body_count είναι ο αριθμός των καταχωρήσεων στον πίνακα method_body. Κάθε μέθοδος_bodyentry αποτελείται από μια δομή μεταβλητού μήκους method_body_info που περιέχει τις οδηγίες για μια μεμονωμένη μέθοδο ή συνάρτηση.|

## βιβλιογραφικές αναφορές

* [Στιβαρό ABC (ActionScript Bytecode) [Dis-]Assembler - Github](https://github.com/CyberShadow/RABCDAsm)

