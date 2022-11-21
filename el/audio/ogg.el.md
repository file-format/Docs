---
date: 2019-12-13
keywords: ogg, μορφή αρχείου ogg, επέκταση .ogg, μορφή ήχου ogg
συγγραφέας:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Μάθετε για τη μορφή αρχείου OGG και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία OGG."
title: Αρχείο OGG - Αρχείο ήχου Ogg Vorbis
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## Τι είναι ένα αρχείο OGG;

Το OGG είναι ένα συμπιεσμένο αρχείο ήχου Ogg Vorbis που αποθηκεύεται με την επέκταση .ogg. Τα αρχεία OGG χρησιμοποιούνται για την αποθήκευση δεδομένων ήχου και μπορούν επίσης να περιλαμβάνουν πληροφορίες καλλιτέχνη και κομμάτι και μεταδεδομένα. Το OGG είναι μια δωρεάν και ανοιχτή μορφή κοντέινερ που διατηρείται από το Ίδρυμα Xiph.Org.

## Σύντομο ιστορικό της μορφής αρχείου OGG

Το έργο Ogg ξεκίνησε ως μέρος ενός μεγαλύτερου έργου το 1993 και ονομάστηκε Squish αλλά λόγω ενός υπάρχοντος εμπορικού σήματος, μετονομάστηκε σε OggSquish. Περιγράφηκε ως μια προσπάθεια δημιουργίας μιας ευέλικτης μορφής συμπιεσμένου ήχου για σύγχρονες εφαρμογές ήχου. Η αναφορά OGG διαχωρίστηκε από τη Vorbis στις 2 Σεπτεμβρίου 2000.

Το OGM δημιουργήθηκε το 2002 λόγω της έλλειψης επίσημης υποστήριξης βίντεο στο OGG. Αυτό επέτρεψε την ενσωμάτωση βίντεο από το πλαίσιο Microsoft DirectShow σε ένα περιτύλιγμα που βασίζεται σε OGG. Μέχρι το 2006, το OGG υποστηρίζονταν από πολλές μηχανές βιντεοπαιχνιδιών και χρησιμοποιούνταν συνήθως για την κωδικοποίηση ελεύθερου περιεχομένου. Το Ίδρυμα Ελεύθερου Λογισμικού ξεκίνησε μια εκστρατεία στις 15 Μαΐου 2007, για να αυξήσει τη χρήση του Vorbis ως ανώτερης εναλλακτικής του MP3. Μέχρι τις 30 Ιουνίου 2009, το OGG ήταν η μόνη μορφή κοντέινερ που υποστηριζόταν από την εφαρμογή HTML5 του Firefox 3.5.

## Μορφή αρχείου OGG

Η μορφή OGG αποτελείται από κομμάτια δεδομένων. Κάθε κομμάτι ονομάζεται σελίδα Ogg. Κάθε σελίδα ξεκινά με "OggS" για να προσδιορίσει τη μορφή Ogg. Η κεφαλίδα περιέχει τον σειριακό αριθμό και τον αριθμό σελίδας που προσδιορίζει κάθε σελίδα ως μέρος μιας σειράς. Η σελίδα αποτελείται από τα ακόλουθα στοιχεία.

- **Κεφαλίδα σελίδας**
  - **Capture Pattern(32 bits)**: This is used for synchronization when parsing OGG files.
  - **Version(8 bits)**: It indicates the version of the Ogg bitstream.
  - **Header Type(8 bits)**: It indicates the type of page.

| Bit | Αξία | Περιγραφή |
| --- | --- | --- |
| 0 | 0x01 | Υποδεικνύει ότι το πρώτο πακέτο της σελίδας είναι η συνέχεια του προηγούμενου πακέτου στη λογική ροή bit. |
| 1 | 0x02 | Υποδεικνύει ότι αυτή η σελίδα είναι η πρώτη στο λογικό bitstream. |
| 2 | 0x04 | Υποδεικνύει ότι αυτή η σελίδα είναι η τελευταία στη λογική ροή bit. |

  - **Granule position(64 bits)**: It is the time marker whose meaning is determined by the codec.
  - **Bitstream serial number(32 bits)**: It is the serial number that identifies the page belonging to a particular logical bitstream.
  - **Page sequence number(32 bits)**: It indicates the sequence of the page with the first page starting at 0.
  - **Checksum(32 bits)**: Provides the CRC32 checksum of the entire page data.
  - **Page segments(8 bits)**: Indicates the number of segments on the page.
  - **Segment table**: It is an array of 8-bit values indicating the length of each segment in the page body.
- **Μεταδεδομένα**: Το VorbisComment είναι ο πιο ευρέως υποστηριζόμενος μηχανισμός για την αποθήκευση μεταδεδομένων. Άλλοι μηχανισμοί περιλαμβάνουν τα ακόλουθα:
  - FLAC metadata blocks
  - Ogg Skeleton
  - Continuous Media Markup Language

## Βιβλιογραφικές αναφορές ##

- [OGG - Wikipedia](https://en.wikipedia.org/wiki/Ogg)

