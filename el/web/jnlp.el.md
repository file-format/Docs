---
date: 2022-07-30
συγγραφέας:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Μορφή αρχείου JNLP - Τι είναι ένα αρχείο JNP;
linktitle: JNLP
description: "Μάθετε για τη μορφή αρχείου JNLP και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία JNLP."
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## Τι είναι ένα αρχείο JNLP;

Ένα αρχείο JNLP είναι ένα αρχείο Java Web Start (JWS) που περιέχει πληροφορίες XML για την εκκίνηση ενός προγράμματος Java μέσω του δικτύου. Αποθηκεύεται σε μορφή Java Network Launching Protocol (JNLP). Χρησιμοποιείται από την τεχνολογία Java Web Start (JWS) που είναι μια τεχνολογία ανάπτυξης εφαρμογών για τη λήψη και εκτέλεση μιας εφαρμογής. Ένα αρχείο JNLP περιέχει την απομακρυσμένη διεύθυνση του διακομιστή από τον οποίο γίνεται λήψη και εκκίνηση του προγράμματος σε τοπικό μηχάνημα.

## Μορφή αρχείου JNLP - Περισσότερες πληροφορίες

Τα αρχεία JNLP αποθηκεύονται ως αρχεία **[XML](/el/web/xml/)** που αποθηκεύονται σε μορφή κειμένου αναγνώσιμη από τον άνθρωπο. Το αρχείο XML έχει τις πληροφορίες που χρησιμοποιούνται για την εκκίνηση και την εκτέλεση μιας εφαρμογής Java μέσω του δικτύου. Το JWS σάς επιτρέπει να εκκινείτε εφαρμογές κάνοντας κλικ στον σύνδεσμο της ιστοσελίδας. Η λήψη της εφαρμογής γίνεται σε περίπτωση που δεν έχει ήδη ληφθεί στον υπολογιστή χρήστη.

Η Oracle κατήργησε το JWS με την κυκλοφορία της Java Platform Standard Edition (JSE) 9. Με αυτό, τα αρχεία JNLP δεν υποστηρίζονται πλέον.

### Πώς να ανοίξετε αρχεία JNLP;

Οι εφαρμογές που μπορούν **να ανοίξουν αρχεία JNLP** περιλαμβάνουν **Microsoft Visual Studio Code**, **Notepad**, **Notepad++**, **Oracle Java Web Start**, **Karakun OpenWebStart** και * *GitHub Atom**.

### Παράδειγμα αρχείου JNLP

```
<jnlp spec="1.0" codebase="http://localhost/jws" href="Notepad.jnlp">
   <information>
      <title>Notepad Demo</title>
      <vendor>Sun Microsystems, Inc.</vendor>
   </information>
   <resources>
      <property name="jnlp.publish-url" value="$$context/publish"/>
      <j2se version="1.3+" href="http://java.sun.com/products/autodl/j2se"/>
      <jar href="Notepad.jar"/>
   </resources>
   <application-desc main-class="Notepad"/>
</jnlp>
```
**Χρήση**

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0 Transitional//EN">
<HTML>
<HEAD>
   <TITLE>Java Web Start Demo</TTLE>    
</HEAD>
<BODY>

<H1>Java Web Start Demo</H1>
<a href="Notepad.jnlp">Lanuch Notepad Application</a>
This link is to the Notepad.jnlp file.
</BODY>
</HTML>
```
## Πώς να εκτελέσετε αρχεία JNLP;

Με την κατάργηση του JWS, οι εφαρμογές που έχουν αναπτυχθεί με βάση την τεχνολογία JWS δεν μπορούν να εκτελεστούν με την πιο πρόσφατη έκδοση της Java. Αυτά τα προγράμματα που βασίζονται στο JNLP, ωστόσο, μπορούν να εκτελεστούν χρησιμοποιώντας το OpenWebStart, το οποίο είναι μια εκ νέου εφαρμογή ανοιχτού κώδικα της τεχνολογίας Java Web Start. Εγκαθίσταται παράλληλα με την πιο πρόσφατη έκδοση της Java και παρέχει τις πιο συχνά χρησιμοποιούμενες λειτουργίες του Java Web Start και του προτύπου JNLP.

## Βιβλιογραφικές αναφορές ##

* [Τι είναι το Java Web Start και πώς εκκινείται;](https://www.java.com/en/download/help/java_webstart.html)
* [Εκτέλεση JNLP με την τελευταία έκδοση Java](https://openwebstart.com/)
* [Java Web Start - Wikipedia](https://en.wikipedia.org/wiki/Java_Web_Start)

