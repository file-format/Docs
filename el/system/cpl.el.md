{
  "date" : "2021-06-29",
  "keywords" :[ "CPL", "επέκταση", "αρχείο", "μορφή", "σύστημα", "Αρχείο πίνακα ελέγχου", "Windows", "προγράμματα", "υπολογιστής", "εφαρμογή" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPL - Αρχείο Πίνακα Ελέγχου",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου CPL και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία CPL.",
  "linktitle" : "CPL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Τι είναι ένα αρχείο CPL; ##

Ένα αρχείο CPL είναι ένας τύπος αρχείου "συστήματος". Χρησιμοποιείται από το λειτουργικό σύστημα Windows. Ένα αρχείο CPL είναι συντομογραφία για το Αρχείο Πίνακα Ελέγχου. Αυτά τα αρχεία είναι δυαδικά αρχεία που ανοίγουν με τον πίνακα ελέγχου σε ένα λειτουργικό σύστημα Microsoft Windows και χρησιμοποιούνται για την αναπαράσταση και το άνοιγμα των εργαλείων που είναι διαθέσιμα στον πίνακα ελέγχου, όπως ποντίκι, οθόνες, δικτύωση, μεταξύ άλλων. Τα αρχεία CPL συνήθως αποθηκεύονται στο φάκελο συστήματος της συσκευής σας. Αυτά τα αρχεία δεν πρέπει να ανοίγονται χειροκίνητα.


## Μορφή αρχείου CPL ##

Διαφορετικά αρχεία CPL στο λειτουργικό σας σύστημα Windows είναι συνδεδεμένα για να αντιπροσωπεύουν διαφορετικά στοιχεία του πίνακα ελέγχου. Όλα τα στοιχεία του πίνακα ελέγχου συνδέονται με ένα αρχείο CPL και έχουν το επίθημα ".cpl" συνδεδεμένο στα στοιχεία τους.

Μερικοί συνήθεις τύποι αρχείων CPL με τις μορφές τους είναι:

* Inetcpl.cpl – Για ιδιότητες Διαδικτύου στη συσκευή σας
* Appwiz.cpl – Για να προσθέσετε ή να αφαιρέσετε ιδιότητες προγραμμάτων στη συσκευή σας
* Desk.cpl – Για τις ιδιότητες Display
* Main.cpl – Για ιδιότητες που σχετίζονται με ποντίκι, γραμματοσειρές, πληκτρολόγιο και εκτυπωτές.
* Netcpl.cpl – Για ιδιότητες που σχετίζονται με το δίκτυο
* System.cpl – Για ιδιότητες που σχετίζονται με το σύστημα και για τον οδηγό προσθήκης νέου υλικού
* TimeDate.cpl – Για ιδιότητες ημερομηνίας ή ώρας
* Mlcfg32.cpl – Για ιδιότητες Microsoft Exchange ή Windows Messaging
* Intl.cpl – Αυτό αφορά τις ιδιότητες περιφερειακών ρυθμίσεων
* Modem.cpl – Για ιδιότητες που σχετίζονται με το μόντεμ
* Themes.cpl – Αποθηκεύει θέματα και ιδιότητες επιφάνειας εργασίας.
* Password.cpl – Για ιδιότητες κωδικού πρόσβασης
* Mmsys.cpl – Για ιδιότητες πολυμέσων
* Wgpocpl.cpl – Αφορά το Ταχυδρομείο της Microsoft Mail

## Σύντομη Ιστορία ##

Ο τύπος αρχείου CPL αναπτύχθηκε από τα Microsoft Windows και αποτελεί αναπόσπαστο μέρος του λειτουργικού συστήματος Windows από τα Windows 1.0. Εξακολουθεί να χρησιμοποιείται σε όλες τις εκδόσεις των Windows και όλες οι ιδιότητες των στοιχείων του πίνακα ελέγχου αποθηκεύονται χρησιμοποιώντας αυτόν τον τύπο αρχείου.

## Παράδειγμα CPL ##

Ένα δείγμα αρχείου CPL μπορείτε να δείτε παρακάτω:

```
<!-- Copyright (c) Microsoft Corporation -->
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity name="Microsoft.Windows.Net.ncpa" processorArchitecture="x86" version="5.1.0.0" type="win32"/>
<description>NCPA CPL</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="x86" 
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3">
    <security>
        <requestedPrivileges>
            <requestedExecutionLevel level="asInvoker" uiAccess="false"/>
        </requestedPrivileges>
    </security>
</trustInfo>
</assembly>

```
