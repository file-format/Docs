{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Αρχείο AIDL - Αρχείο γλώσσας ορισμού διεπαφής Android",
  "description":"Μάθετε τι είναι η μορφή αρχείου AIDL με παραδείγματα και API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία AIDL.",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Τι είναι ένα αρχείο AIDL;

Ένα αρχείο AIDL (Android Interface Definition Language) επιτρέπει στους προγραμματιστές Android να δημιουργήσουν επικοινωνία μεταξύ διαφορετικών εφαρμογών. Με βάση τη διεπαφή προγραμματισμού, τόσο ο πελάτης όσο και η υπηρεσία συμφωνούν να επικοινωνούν χρησιμοποιώντας επικοινωνία μεταξύ διεργασιών (IPC). Το αρχείο AIDL περιέχει τον πηγαίο κώδικα [Java](/el/programming/java/) για τον καθορισμό αυτών των διεπαφών και των συμβάσεων επικοινωνίας μεταξύ εφαρμογών.

Μπορείτε να ανοίξετε αρχεία AIDL με το Google Android Studio ή οποιοδήποτε πρόγραμμα επεξεργασίας κειμένου όπως το Microsoft Notepad και το Notepad++.

## Μορφή αρχείου AIDL - Περισσότερες πληροφορίες

Το AIDL είναι αρχεία κειμένου που περιέχουν τις διεπαφές για την επικοινωνία μεταξύ των εφαρμογών. Το λειτουργικό σύστημα Android δεν επιτρέπει σε μια διαδικασία να έχει πρόσβαση στη μνήμη μιας άλλης διαδικασίας. Αυτό οδηγεί τις διεργασίες να χωρίσουν τα αντικείμενά τους σε πρωτόγονα για την κατανόηση του υποκείμενου λειτουργικού συστήματος και να δημιουργήσουν τη διαδικασία των δομών επικοινωνίας για τον προγραμματιστή.

### Ποιοι τύποι δεδομένων υποστηρίζονται από το AIDL;

Το AIDL υποστηρίζει τους ακόλουθους τύπους δεδομένων από προεπιλογή.

* Όλοι οι πρωτόγονοι τύποι στη γλώσσα προγραμματισμού Java (όπως int, long, char, boolean και ούτω καθεξής)
* Χορδή
* CharSequence
* Λίστα
* Χάρτης

## Παράδειγμα αρχείου AIDL

Ακολουθεί ένα παράδειγμα αρχείου AIDL.

```
// IRemoteService.aidl
package com.example.android;

// Declare any non-default types here with import statements

/** Example service interface */
interface IRemoteService {
    /** Request the process ID of this service, to do evil things with it. */
    int getPid();

    /** Demonstrates some basic types that you can use as parameters
     * and return values in AIDL.
     */
    void basicTypes(int anInt, long aLong, boolean aBoolean, float aFloat,
            double aDouble, String aString);
}

```
## βιβλιογραφικές αναφορές

* [Android Interface Definition Language (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

