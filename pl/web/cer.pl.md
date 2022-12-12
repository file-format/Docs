{
  "date" : "2021-07-13",
  "keywords" :["CER", "rozszerzenie", "plik", "format", "sieć", "certyfikat", "język"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CER - format pliku certyfikatu",
  "description":"Poznaj format pliku CER i interfejsy API, które mogą tworzyć i otwierać pliki CER.",
  "linktitle" : "CER",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## Czym jest plik CER? ##

Plik z rozszerzeniem .cer jest odpowiedzialny za przechowywanie pewnych informacji o certyfikacie właściciela i konkretnym kluczu publicznym. Ten format plików nie może przechowywać kluczy prywatnych i może przechowywać tylko jeden certyfikat, którym jest x509. Specjalnie zabezpieczone urzędy certyfikacji to te, które należą do HTTPS, zaufanego i zabezpieczonego protokołu do przeglądania
CER to certyfikat twojego serwera. Zwykle jest odbierany przez urząd certyfikacji dla domeny. CER jest w większości uważany za taki sam jak [CRT](/pl/web/crt/), chociaż oba są tym samym formatem certyfikatu SSL, ale mają różne rozszerzenia nazw plików.
Można ich używać w systemach operacyjnych, po prostu otwierając przeglądarkę i sprawdzając bezpieczeństwo używanej przeglądarki lub witryny.

## Krótka historia ##

W 1995 roku Thawte stała się pierwszym organem certyfikującym, który rozwiązał problem publicznych certyfikatów SSL (bezpieczne łącze gniazda) poza Stanami Zjednoczonymi. Następnie istnieje szereg takich organów, które powstały w latach 1995-2020.

## Format pliku CER ##

Te pliki mogą być proste
* PKC S#7 obejmuje kodowanie Base64 ASCII
* Jego rozszerzenia plików to p7b lub p7cZ
* W przypadku zawartości binarnej certyfikatem byłby DER lub pkcs12/pfx.
Istnieje wiele rodzajów plików certyfikatów z pewnymi unikalnymi specyfikacjami:
* .pem, kiedy organizacja usThawteificate łączy ten format, jest dobrze znana z tworzenia certyfikatów
* .arm, gdy wymagana jest metoda wyodrębniania certyfikatu wspomagająca samopodpisanie, określonym formatem do tego celu jest .arm. Jest reprezentowany w kodowaniu base-64 ASCII.
* .der, składa się z danych binarnych. Oznacza to, że można go używać tylko dla jednego certyfikatu
* .pfx (PKC512), Składa się z klucza prywatnego odpowiadającego certyfikatowi wydanemu przez urząd certyfikacji lub certyfikatowi z podpisem własnym. Ten format jest dobrze znany z konwersji jednej implementacji SSL na drugą.


