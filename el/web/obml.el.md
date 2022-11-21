{
  "date" : "2022-05-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Μορφή αρχείου OBML - Αποθηκευμένο αρχείο ιστοσελίδας Opera Mini",
  "description" :"Μάθετε για το τι είναι ένα αρχείο OBML και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχείο OBML.",
  "linktitle" : "OBML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-05-19"
}

## Τι είναι ένα αρχείο OBML;

Ένα αρχείο OBML (Opera Binary Markup Language) είναι μια έκδοση εκτός σύνδεσης μιας ιστοσελίδας που έχει αποθηκευτεί από το πρόγραμμα περιήγησης ιστού Opera Mini για κινητά. Είναι μια αυτόνομη, συμπαγής έκδοση των αρχείων [HTML](/el/web/html/) που περιέχει όλα τα στοιχεία της σελίδας για εμφάνιση σε συγκεκριμένες συσκευές ενώ είστε εκτός σύνδεσης. Η μορφή αρχείου OBML έχει αναβαθμιστεί σε πολλές εκδόσεις με τα OBML15 και OBML16 να χρησιμοποιούνται ευρέως. Ένα σημαντικό σημείο που πρέπει να λάβετε υπόψη είναι ότι κάθε έκδοση Opera Mini είναι συμβατή μόνο με μία μορφή OBML. Έτσι, η αναβάθμιση του Opera Mini θα αφήσει τις σελίδες που είχαν αποθηκευτεί προηγουμένως ευανάγνωστες. Τα αρχεία OBML μπορούν να μετατραπούν σε HTML και [PDF](/el/pdf/).

## Μορφή αρχείου OBML

Η μορφή αρχείου OBML αποθηκεύεται στην αποκλειστική μορφή αρχείου της Opera και οι προδιαγραφές της μορφής αρχείου δεν είναι διαθέσιμες δημόσια. Ωστόσο, η [μορφή OMBL](https://github.com/grawity/obml-parser/blob/master/obml.md) τροποποιήθηκε αντίστροφα για την αποκωδικοποίηση της δομής της ως εξής.

### Τύποι δεδομένων OBML

Σύμφωνα με τα αποτελέσματα αντίστροφης μηχανικής, το OBML χρησιμοποιεί τους ακόλουθους πρωτόγονους τύπους:

* «byte» – ανυπόγραφος ακέραιος αριθμός (1 byte)
* `short` – υπογεγραμμένος ακέραιος (2 byte, big-endian)
* «μέσο» – υπογεγραμμένος ακέραιος (3 byte, big-endian)
 * `blob` – { length: short, data: byte[length] }
* «char» – ένα byte που περιέχει έναν χαρακτήρα ASCII
* «string» – μια μάζα που περιέχει κωδικοποιημένο κείμενο UTF-8

### Κεφαλίδα OBML

```
header := {
	(if version >= 15) {
		fake_file_size: medium = 0x02d355
		fake_version: byte     = 16
	}
	file_size: medium
	version: byte
	page_size: coords
	(if version == 16) {
		unknown: byte[3]      // always S\x00\x00
	}
	unknown: short                // always -1
	page_title: string
	unknown: blob
	page_url_base: string
	page_url: url
	(if version >= 15) {
		unknown: byte[6]
	}
	(if 6 < version <= 13) {
		unknown: byte[5]
	}
	(if version == 6) {
		unknown: byte[1]
	}
	metadata: chunk[]
	content: chunk[]
}
```
## βιβλιογραφικές αναφορές

* [Μορφή OMBL](https://github.com/grawity/obml-parser/blob/master/obml.md)

