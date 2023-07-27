{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAR - Μορφή αρχείου επεκτάσιμου αρχείου",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου XAR και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία XAR.",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Τι είναι ένα αρχείο XAR;

Ένα αρχείο με επέκταση .xar (Extensible Archive Format) είναι ένα αρχείο UNIX που μπορεί να είναι σε συμπιεσμένη ή μη συμπιεσμένη μορφή. Χρησιμοποιείται επίσης σε Mac OS για εγκατάσταση πακέτων. Το XAR είναι ανοιχτού κώδικα και ήταν μέρος του Mac OS X 10.5 για χρήση με το πρόγραμμα περιήγησης Safari.

## Μορφή αρχείου XAR

Ένα αρχείο [XAR](https://github.com/mackyle/xar/wiki/xarformat) έχει τρεις κύριες περιοχές.

* Κεφαλίδα
* Πίνακας περιεχομένων
* Σωρός

### Κεφαλίδα XAR

Η κεφαλίδα XAR είναι δομημένη ως εξής.

|Πεδίο|Τύπος δεδομένων|Μέγεθος σε Byte|
---|---|---|
|Magic|Ανυπόγραφο Int 32|4|
|Μέγεθος|Ανυπόγραφο Int 16|2|
|Έκδοση|Ανυπόγραφο Int 16|2|
|Μήκος TOC Συμπιεσμένο|Ανυπόγραφο Int 64|8|
|Μήκος TOC Ασυμπίεστο|Ανυπόγραφο Int 64|8|
|Άθροισμα ελέγχου|Ανυπόγραφο Int 32|4|
|Όνομα σύνοψης μηνύματος |Null Terminated||

Η δομή C της κεφαλίδας XAR μπορεί να οριστεί ως εξής.
```
struct xar_header {
    uint32_t magic;
    uint16_t size;
    uint16_t version;
    uint64_t toc_length_compressed;
    uint64_t toc_length_uncompressed;
    uint32_t cksum_alg;
    /* A nul-terminated, zero-padded to multiple of 4, message digest name
     * appears here if cksum_alg is 3 which must not be empty ("") or "none".
     */
};
```
Σημειώστε ότι όλα τα πεδία της κεφαλίδας (μαγεία, μέγεθος, έκδοση, toc_length_compressed, toc_length_uncompressed, cksum_alg) αποθηκεύονται πάντα σε αρχεία XAR με σειρά byte δικτύου (γνωστή και ως big endian).

### Πίνακας περιεχομένων XAR (TOC)

Ο πίνακας περιεχομένων είναι ένα έγγραφο XML που είναι (και πρέπει) να κωδικοποιηθεί ως UTF-8. Αποθηκεύεται στην αρχή του αρχείου, καθιστώντας εύκολη τη σάρωση μέσω του αρχείου για την εξαγωγή μεμονωμένου αρχείου. Το αρχείο XAR σάς επιτρέπει να συμπιέσετε/κωδικοποιήσετε τα μεμονωμένα αρχεία στο αρχείο ανεξάρτητα χρησιμοποιώντας διαφορετικά σχήματα συμπίεσης όπως [GZIP](/el/compression/gz/), [BZIP2](/el/compression/bz2/) και άλλα παρόμοια.

```
<?xml version="1.0"?>

<xar>
  <toc>
    <checksum style="sha1">
      <size>20</size>
      <offset>0</offset>
    </checksum>
    <file id="1">
      <name>xar</name>
      <type>file</type>
      <mode>0755</mode>
      <uid>0</uid>
      <gid>0</gid>
      <user>root</user>
      <group>wheel</group>
      <size>81180</size>
      <data>
        <offset>0</offset>
        <size>74108</size>
        <length>23083</length>
        <extracted-checksum style="md5">d852c77ac3c8e83f312c12b4c3198e6d</checksum>
        <archived-checksum style="md5">ceaf793ccb1990ecbadb20112d5f9e5d</checksum>
        <encoding style="application/x-gzip"/>
      </data>
      <ea>
        <name>com.apple.ResourceFork</name>
        <offset>0</offset>
        <size>7072</size>
        <length>3942</length>
        <extracted-checksum style="md5">0f7061dca2d7411352377db0e53792db</checksum>
        <archived-checksum style="md5">c72de8ac25abe462a930254d82958534</checksum>
        <encoding style="application/x-gzip"/>
      </ea>
    </file>
  </toc>
</xar>
```

### Σωρός

Ο σωρός ξεκινά αμέσως μετά το συμπιεσμένο toc. Είναι ένας μη δομημένος σωρός δεδομένων που αναφέρονται από το TOC. Οι τιμές Offset που παρατίθενται στο TOC ξεκινούν από την αρχή του σωρού. Οι τιμές μήκους στο toc αναφέρονται στον πραγματικό αριθμό των byte που είναι αποθηκευμένα στο σωρό (συμπιεσμένα ή όχι) ενώ η τιμή μεγέθους αναφέρεται στο εξαγόμενο μέγεθος του αντικειμένου (μετά την αποσυμπίεση εάν είναι απαραίτητο).

## βιβλιογραφικές αναφορές

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)
* [XAR - Wikipedia](https://en.wikipedia.org/wiki/Xar_(archiver))

