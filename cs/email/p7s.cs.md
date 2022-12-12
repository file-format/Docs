{
  "date" : "2022.01.31",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Soubor P7S – digitálně podepsaná e-mailová zpráva",
  "description":"Další informace o formátu souboru P7S a rozhraních API, která mohou vytvářet a otevírat soubory P7S.",
  "linktitle" : "P7S",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2022.01.31"
}

## Co je soubor P7S?

Soubor P7S je digitální podpis, který je přijímán s digitálně podepsaným e-mailem. Přítomnost tohoto souboru jako přílohy k e-mailu ověřuje, že je e-mail odeslán z autentického zdroje. Tím je zajištěno, že odesílatel má na svém počítači nainstalovaný certifikát Email Signing. Když je takto podepsaný e-mail odeslán z počítače uživatele, je k němu připojen soubor P7S, který obsahuje jméno odesílatele. E-mailové klienty podporující podepsané e-maily mohou vidět informace o odesílateli.

## Formát souboru P7S – Další informace

S/MIME (Secure/Multipurpose Internet Mail Extensions) Soubory P7S obsahují informace ve formátu prostého textu, který je čitelný pro člověka. E-mailové klienty, jako je Microsoft Outlook, Apple Mail a Mozilla Thunderbird, podporují čtení digitálně podepsaných informací z e-mailu S/MIME. Podepsáním e-mailu ověříte identitu odesílatele a sdělíte příjemci, že zpráva je autentická. Když jsou e-maily staženy z e-mailových klientů (buď jako [EML](/cs/email/eml/) nebo [MSG](/cs/email/msg/)), tyto soubory P7S se najdou v příloze těchto e-mailů.

Soubor P7S obsahuje následující informace:

* Zdroj původu e-mailu
* Datum a čas odeslání,
* Zda bylo změněno během přenosu

Tyto informace jsou vloženy pomocí technologie Public-Key Cryptography Standard #7 (PKCS7) pro digitální připojení zašifrovaných podpisů k e-mailu.

## Reference ##

* [Microsoft Sign Tool](https://docs.microsoft.com/en-us/windows-hardware/drivers/devtest/signtool)

