{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TNEF",
  "description":"Aflați despre formatul de fișier TNEF și despre API-urile care pot crea și deschide fișiere TNEF.",
  "linktitle" : "TNEF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier TNEF?

Transport Neutral Encapsulation Format (TNEF) este un proprietar Microsoft, pentru încapsularea atașamentelor de e-mail bazate pe Interfața de programare a aplicației de mesagerie (**MAPI**). Microsoft Outlook și Microsoft Exchange Server acceptă în întregime TNEF, în timp ce mai târziu decodifică TNEF în MAPI și afișează e-mailurile formatate. Un atașament de e-mail cu codificare TNEF are un tip MIME MS-TNEF și se stochează ca winmail/win.dat. Atașamentul din winmail .dat încapsulează următoarele informații:


|Mesaj|Obiecte OLE|Funcții Outlook
---|---|---|
|<ul><li> Atașamente la mesaje originale</li><li> Versiunea originală formatată</li><li> fonturi, dimensiuni ale textului și culori ale textului</li></ul> |<ul><li> imagini încorporate</li><li> documente Office încorporate</li></ul> |<ul><li> formulare personalizate</li><li> butoane de vot</li><li> cereri de întâlnire</li></ul>


Alte servicii de e-mail care nu acceptă TNEF, prezintă text simplu pentru mesajele formatate TNEF. Outlook încorporează un format bogat al mesajului în fișiere TNEF (OLE) sau în anumite caracteristici Outlook (formulare, butoane de sondare și solicitări de conferințe). Sancționarea codării explicite TNEF în clientul de e-mail Outlook nu este posibilă, totuși, optarea formatului RTF pentru expedierea unui e-mail facilitează implicit codificarea TNEF.

## Format de fișier TNEF

Algoritmul de date TNEF stabilește o structură aplatizată din proprietăți bogate ale mesajelor ierarhice. Aceste structuri aplatizate folosesc apoi pentru a reprezenta un flux de date în serie compus din proprietăți specifice.

În unele situații, în care proprietățile apar în grupuri sau au mai multe valori, fluxul poate include numărări și completări pentru a impune o anumită aliniere a datelor. O situație distinctivă în care utilizarea acestui algoritm este avantajoasă este într-un mediu de mesagerie neacceptabil. În astfel de medii, o proprietate bogată de mesaj este codificată într-un flux de date serial de către un TNEF Writer. În plus, proprietățile care nu aparțin TNEF-ului subiacent pot fi încapsulate în timpul transmiterii. Aceste proprietăți încapsulate sunt apoi puse la dispoziție prin decodare printr-un TNEF pentru a asigura disponibilitatea tuturor proprietăților mesajului original pentru aplicația client.

În TNEF, toate tipurile de date numerice sunt little-endian și dimensiunea lor este mai mare de un octet. Manipularea acestor valori numerice pe platforme non-little-endian necesită realizarea transformărilor adecvate pentru a obține valori corecte. Valorile șirurilor sunt reprezentate în format Augmented Backus-Naur Form (ABNF) conform specificațiilor [RFC5234]. Când șirul se termină cu caracter nul, este de asemenea inclus; de exemplu, `"worker@specimen.com" %x00`.

{{< figure src="../TNEF.png" alt="Format de fișier TNEF" >}}

## Atribute TNEF și reguli de procesare ##

Fluxul de date din TNEF începe cu un număr de versiune moștenită, o semnătură, o valoare a cheii primitive și un atribut reprezintă o pagină de cod. Această pagină de coduri este generată atunci când codificatorul înregistrează atributele și proprietățile ANSI. După aceea, fluxul a devenit o serie de atribute în care atributele mesajului erau rânduite mai întâi și apoi urmate de atributele atașării. Diferite caracteristici ale mesajelor și atașamentelor sunt conținute în atribute speciale, cum ar fi attMsgProps, attachment și attRecipTable. Atributele care apar în fluxul TNEF conțin structura, proprietățile mesajului și conversiile necesare pentru a le implica cu proprietățile mesajului. Fiecare atribut constă dintr-un ID, dimensiunea și datele atributului, o sumă de control și un nivel în funcție de aplicarea acestuia.

## Relația cu protocoale și alți algoritmi ##

Sistemele care au un mecanism slab pentru afișarea unui format bogat de mesaje au nevoie nativ de algoritmul de date TNEF pentru transport. Folosind tipul media ms-TNEF, rezultatul algoritmului constă dintr-un fișier atașat (winmail.dat) și o parte a corpului MIME specificată în [RFC2045]. Corpul mesajului text simplu este transmis utilizând UUENCODE conform specificației [MSDN-UAF] și acest corp de mesaj sau metoda echivalentă este decodificat la capătul destinatarului. Mai mult, TNEF poate transmite date de mesaje folosind diferite protocoale de internet precum SMTP, POP3, IMAP4 și cele care integrează MIME conform standardului RFC2045.

## Declarație de aplicabilitate ##

Pe lângă transmiterea simplă a mesajelor, aplicația originală a TNEF urma să fie creată pentru a utiliza clase de mesaje și pentru a suporta caracteristici suplimentare care nu au suport original în protocolul de transport. Această aplicație a fost îmbunătățită și mai mult pentru transmiterea proprietăților de mesaje bogate și proprietăți denumite pe care clienții moderni de mesagerie le folosesc în prezent. Pentru conformitatea cu implementarea inițială, sintaxa atributului original este menținută și un atribut special deține proprietățile mesajului nou separat.

## Referințe

* [Format de încapsulare neutru pentru transport](https://en.wikipedia.org/wiki/Transport_Neutral_Encapsulation_Format)
* [Adrese de e-mail și agende de adrese în Exchange Server](https://learn.microsoft.com/en-us/exchange/email-addresses-and-address-books/email-addresses-and-address-books?view# exchserver-2019)
* [[MS-OXTNEF]: Algoritm de date pentru formatul de încapsulare neutru de transport (TNEF)](https://msdn.microsoft.com/en-us/library/cc425498(v#exchg.80).aspx)

