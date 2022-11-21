{
  "date" : "2021-05-24",
  "keywords" :["pac", "File", "Extension", "File Format", "File Extension", "Proxy Auto-Configuration"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAC - Αρχείο Auto-Configuration (PAC) διακομιστή μεσολάβησης",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου PAC και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία PAC.",
  "linktitle" : "PAC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-17"
}

## Τι είναι ένα αρχείο PAC;

Ένα αρχείο με επέκταση .pac (Αυτόματη διαμόρφωση διακομιστή μεσολάβησης) είναι ένα αρχείο διαμόρφωσης που περιέχει κανόνες που στέλνουν αιτήματα ιστού απευθείας στο διαδίκτυο ή τα δρομολογούν μέσω διακομιστή μεσολάβησης. Περιέχει μια συνάρτηση [JavaScript](/el/web/js/) που δρομολογεί τα αιτήματα Ιστού μέσω κάποιου διακομιστή μεσολάβησης ιστού αντί να τα στέλνει απευθείας στον προορισμό. Ένας διακομιστής μεσολάβησης είναι σαν ένας άνθρωπος στη μέση που δέχεται αιτήματα από πολλούς πελάτες και τα εξυπηρετεί με προώθηση σε προορισμούς. Αυτά χρησιμοποιούνται για τον έλεγχο του φορτίου στην κίνηση στο Διαδίκτυο. Τα αρχεία PAC μπορούν να ανοίξουν με οποιοδήποτε πρόγραμμα επεξεργασίας κειμένου όπως το Microsoft Notepad.

## Περισσότερες πληροφορίες σχετικά με τη μορφή αρχείου PAC

Τα αρχεία PAC εισήχθησαν για πρώτη φορά στο Netscape Navigator το 1990. Τα αρχεία PAC είναι γραμμένα σε απλή μορφή κειμένου JavaScript και είναι αναγνώσιμα από τον άνθρωπο. Τα προγράμματα περιήγησης Ιστού έχουν την επιλογή να καθορίσουν τις πληροφορίες διεύθυνσης URL του διακομιστή μεσολάβησης από όπου γίνεται ανάκτηση της λίστας διευθύνσεων URL μεσολάβησης.

Η λειτουργία που ορίζεται μέσα στο PAC χρησιμοποιώντας JavaScript είναι η εξής:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### Παράδειγμα αρχείου PAC

```JavaScript
function FindProxyForURL(url, host) {

// If the hostname matches, send direct.
	if (dnsDomainIs(host, "intranet.domain.com") ||
		shExpMatch(host, "(*.abcdomain.com|abcdomain.com)"))
		return "DIRECT";

// If the protocol or URL matches, send direct.
	if (url.substring(0, 4)=="ftp:" ||
		shExpMatch(url, "http://abcdomain.com/folder/*"))
		return "DIRECT";

// If the requested website is hosted within the internal network, send direct.
	if (isPlainHostName(host) ||
		shExpMatch(host, "*.local") ||
		isInNet(dnsResolve(host), "10.0.0.0", "255.0.0.0") ||
		isInNet(dnsResolve(host), "172.16.0.0",  "255.240.0.0") ||
		isInNet(dnsResolve(host), "192.168.0.0",  "255.255.0.0") ||
		isInNet(dnsResolve(host), "127.0.0.0", "255.255.255.0"))
		return "DIRECT";

// If the IP address of the local machine is within a defined
// subnet, send to a specific proxy.
	if (isInNet(myIpAddress(), "10.10.5.0", "255.255.255.0"))
		return "PROXY 1.2.3.4:8080";

// DEFAULT RULE: All other traffic, use below proxies, in fail-over order.
	return "PROXY 4.5.6.7:8080; PROXY 7.8.9.10:8080";

}
```
## βιβλιογραφικές αναφορές

* [Τι είναι το αρχείο PAC;](http://findproxyforurl.com/pac-file-introduction/)

