{
  "date" : "2021-04-23",
  "keywords": [ "config File", "configuration files", "config File format", "extension", "format","git config file","Configuration files in Linux","what is a config file","Config file php", "ssh config file example", "aws config file example", "python config file example" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CONFIG - Αρχείο διαμόρφωσης",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου CONFIG με παράδειγμα CONFIG και API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία CONFIG.",
  "linktitle" : "CONFIG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## Τι είναι ένα αρχείο CONFIG;
Ένα αρχείο CONFIG είναι γνωστό ως αρχείο διαμόρφωσης. χρησιμοποιείται για τη διαμόρφωση των παραμέτρων και των πρωταρχικών ρυθμίσεων για πολλά λογισμικά υπολογιστών. Ορισμένα λογισμικά διαβάζουν μόνο τα **τα αρχεία διαμόρφωσής τους** κατά την εκκίνηση. Άλλοι ελέγχουν περιοδικά τα αρχεία διαμόρφωσης για αλλαγές.

## Μορφή αρχείου CONFIG
Η μορφή **CONFIG File** χρησιμοποιείται για διαδικασίες διακομιστή, εφαρμογές λογισμικού και ρυθμίσεις λειτουργικού συστήματος. Ένας προγραμματιστής μπορεί να γράψει κώδικα για να δώσει εντολή σε ένα λογισμικό να διαβάσει τα αρχεία διαμόρφωσης ξανά και ξανά μετά από συγκεκριμένο χρονικό διάστημα και να εφαρμόσει τις αλλαγές στην τρέχουσα διαδικασία. Δεν υπάρχουν οριστικά πρότυπα ή ισχυρές συμβάσεις για τη σύνταξη αρχείων CONFIG. Για παράδειγμα, το αρχείο Web.config της Microsoft ανήκει στη μορφή αρχείου CONFIG, η οποία αποτελείται από ένα σύνολο ετικετών που βασίζεται σε [XML](https://docs.fileformat.com/web/xml/). μπορεί να επεξεργαστεί με το Microsoft Visual Studio ή οποιοδήποτε άλλο πρόγραμμα επεξεργασίας κειμένου.

## Παραδείγματα αρχείων διαμόρφωσης:
Δεδομένου ότι τα αρχεία διαμόρφωσης δεν δημιουργούνται ακολουθώντας κανόνες, πρότυπα ή συμβάσεις, αυτά τα αρχεία ενδέχεται να έχουν γραφτεί χρησιμοποιώντας διαφορετικές μορφές. Ένα αρχείο .config μπορεί να βασίζεται σε XML, [JSON](https://docs.fileformat.com/web/json/) ή σε οποιαδήποτε άλλη μορφή. Ακολουθούν τα παραδείγματα αρχείων διαμόρφωσης για γνωστά λειτουργικά συστήματα και λογισμικά:

### Αρχεία διαμόρφωσης στο Linux
Κάθε πρόγραμμα Linux είναι ένα εκτελέσιμο αρχείο που διατηρεί τη λίστα των **opcodes** που εκτελεί η CPU για να ολοκληρώσει τυπικές λειτουργίες. Οι λειτουργίες σχεδόν κάθε προγράμματος μπορούν να προσαρμοστούν στις απαιτήσεις σας αλλάζοντας τα αρχεία διαμόρφωσής του. Πολλά αρχεία διαμόρφωσης στο σύστημα Linux βρίσκονται στον κατάλογο /etc. Τα αρχεία ρυθμίσεων μπορούν να ταξινομηθούν στις ακόλουθες κατηγορίες:
|Κατηγορία|Παράδειγμα| Σχόλια|
---|---|---|
|Πρόσβαση στα αρχεία|/etc/host.conf|Ενημερώνει στον διακομιστή τομέα δικτύου πώς να αναζητήσει ονόματα κεντρικών υπολογιστών.|
|Εκκίνηση και login/logout|/etc/rc.d/rc.local|Μη επίσημο. Μπορεί να κληθεί από rc, rc.sysinit ή /etc/inittab.|
|Σύστημα αρχείων|/etc/mtools.conf|Διαμόρφωση για όλες τις λειτουργίες (mkdir, αντιγραφή, μορφή, κ.λπ.) σε ένα σύστημα αρχείων τύπου DOS.|
|Διαχείριση συστήματος|/etc/shells|Διατηρεί τη λίστα των πιθανών "κελυφών" που είναι διαθέσιμα στο σύστημα.|
|Δίκτυο|/etc/gated.conf|Διαμόρφωση για gated. Χρησιμοποιείται μόνο από τον περιφραγμένο δαίμονα.|
|Εντολές συστήματος|/etc/logrotate.conf|Διαμόρφωση για το Dynamic Linker.|
|Daemons|/etc/httpd.conf|Το αρχείο διαμόρφωσης για τον Apache, τον διακομιστή Web. Αυτό το αρχείο συνήθως δεν βρίσκεται στο /etc.|
|Προγράμματα χρήστη| /etc/lynx.cfg| Ρυθμίσεις διακομιστή μεσολάβησης|
### Παράδειγμα αρχείου AWS CONFIG
Οι ρυθμίσεις διαμόρφωσης και τα διαπιστευτήρια που χρησιμοποιούνται συχνά μπορούν να αποθηκευτούν σε αρχεία CONFIG που διατηρούνται από το AWS CLI. Το αρχείο CONFIG πρέπει να είναι αρχείο απλού κειμένου που χρησιμοποιεί την ακόλουθη μορφή:
```
[default]
region = us-west-2
output = json

[profile dev-user]
region = us-east-1
output = text

[profile developers]
role_arn = arn:aws:iam::123456789012:role/developers
source_profile = dev-user
region = us-west-2
output = json
```
### Παράδειγμα αρχείου SSH CONFIG
Το αρχείο διαμόρφωσης από την πλευρά του πελάτη OpenSSH ονομάζεται CONFIG και αποθηκεύεται στον κατάλογο .ssh. Το αρχείο SSH CONFIG αποτελείται από την ακόλουθη δομή:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### Παράδειγμα αρχείου Python CONFIG
Ένα αρχείο Python CONFIG θα μπορούσε να μοιάζει με αυτό:

```
#!/usr/bin/env python
import preprocessing

mysql = {
    "host": "localhost",
    "user": "root",
    "passwd": "my secret password",
    "db": "write-math",
}
preprocessing_queue = [
    preprocessing.scale_and_center,
    preprocessing.dot_reduction,
    preprocessing.connect_lines,
]
use_anonymous = True
```



## βιβλιογραφικές αναφορές

* [Κατανόηση των αρχείων διαμόρφωσης Linux](https://developer.ibm.com/technologies/linux/articles/l-config/)
* [Ρυθμίσεις αρχείου διαμόρφωσης και διαπιστευτηρίων](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
* [Αρχεία διαμόρφωσης στην Python](https://martin-thoma.com/configuration-files-in-python/)

