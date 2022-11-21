---
date: 2019-10-11
keywords: f4v, .f4v, μορφή αρχείου f4v, μορφή αρχείου .f4v, επέκταση .f4v, επέκταση f4v, μορφή βίντεο f4v, πώς να ανοίξετε αρχεία f4v, τι είναι τα αρχεία f4v
συγγραφέας:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Μάθετε για τη μορφή αρχείου F4V και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία F4V"
title: Μορφή αρχείου F4V
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Τι είναι ένα αρχείο F4V; ##

Το F4V (Flash MP4 Video File) είναι ένα αρχείο βίντεο που αποθηκεύεται με την επέκταση .f4v. Βασίζεται στη βασική μορφή αρχείου πολυμέσων ISO (MPEG-4 Μέρος 12). Είναι πολύ παρόμοιο με το [MP4](/el/video/mp4/) και γι' αυτό αναφέρεται και ως Flash MP4 ανεπίσημα. Το [FLV](/el/video/flv/) είχε περιορισμούς κατά τη ροή περιεχομένου H.264/ACC, γεγονός που είχε ως αποτέλεσμα η Adobe Systems να δημιουργήσει τη νέα μορφή F4V. Το Flash Player μπορεί να αναπαράγει αρχεία F4V από την κυκλοφορία του Flash Player 9 Update 3.

## Δομή αρχείων F4V ##

Η μορφή αρχείου F4V βασίζεται στη βασική μορφή αρχείου πολυμέσων ISO (MPEG-4 Μέρος 12) και μοιάζει πολύ με τη μορφή MP4. Για λεπτομέρειες σχετικά με τη δομή, ανατρέξτε στη σελίδα [MP4](/el/video/mp4/). Η κύρια διαφορά μεταξύ F4V και MP4 είναι οι μορφές μεταδεδομένων που μπορεί να αποθηκεύσει το F4V. Παρακάτω δίνεται η λίστα με τις μορφές μεταδεδομένων που υποστηρίζονται από τη μορφή F4V.

- **Πλαίσιο ετικέτας**: Πρόσθετα τέσσερα προαιρετικά πλαίσια ετικετών (auth, title, dscp, cprt) μέσα στο πλαίσιο Movie (moov).
- **Πλαίσιο μεταδεδομένων XMP**: Αυτό το πλαίσιο βρίσκεται αμέσως μετά το πλαίσιο Ταινία (moov). Με αυτό, το αρχείο μπορεί να επικοινωνήσει μεταδεδομένα XMP σε μια ταινία SWF μέσω ActionScript.
- **ilst box**: Αυτό το πλαίσιο εμφανίζεται μέσα στο πλαίσιο Meta (meta) και μπορεί να περιέχει έναν αριθμό από ετικέτες μεταδεδομένων. Οι υποστηριζόμενοι τύποι δεδομένων δίνονται παρακάτω.
  - **0**: Custom Data.
  - **1**: Text Data.
  - **12, 14**: Binary Data
  - **21**: Generic Data.
- **Πλαίσιο Μεταδεδομένων κομματιού κειμένου**: Τα δείγματα κειμένου (κείμενο ή tx3g) μέσα στο πλαίσιο δεδομένων πολυμέσων (mdat). Μπορεί να περιέχει τα ακόλουθα πλαίσια μεταδεδομένων.
  - **Style box**: Text style specifications.
  - **Highlight box**: Specifies the range of text to be highlighted.
  - **Highlight Color box**: Specifies the highlight color for the text.
  - **Karaoke box**: Specified the karaoke metadata.
  - **Scroll Delay box**: Specifies the scroll delay.
  - **Drop Shadow Offset box**: Specifies the drop shadow offset coordinates for the text.
  - **Drop Shadow Alpha box**: Specifies the drop shadow alpha value for the text.
  - **Hypertext box**: Specifies the hypertext text with alt text over a text range.
  - **Text Box box**: Defines the coordinates for the text box.
  - **Blinking box**: Specifies blinking for a range of text.
  - **Text Wrap box**: Sets the text wrap flag for the text.
  - **Text Wrap box**: Sets the text wrap flag for the text.

## Βιβλιογραφικές αναφορές ##

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

