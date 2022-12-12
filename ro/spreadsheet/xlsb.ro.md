{
  "date" : "2019-12-10",
  "keywords" :[ "XLSB", "fișier", "extensie", "format fișier", "Fișier Excel Binary Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Ghidul dvs. de format de fișier pentru a afla ce este un fișier XLSB și API-urile care le pot crea și deschide.",
  "title" :"Ce este un fișier XLSB?",
  "linktitle" : "XLSB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Ce este un fișier XLSB?

Formatul de fișier XLSB specifică formatul de fișier binar Excel, care este o colecție de înregistrări și structuri care specifică conținutul registrului de lucru Excel. Conținutul poate include tabele nestructurate sau semistructurate de numere, text sau ambele numere și text, formule, conexiuni de date externe, diagrame și imagini. Spre deosebire de [XLSX](/ro/spreadsheet/xlsx/) (care se bazează pe formatul de fișier Open XML), XLSB reprezintă fișierul binar al registrului de lucru Excel. Fișierele XLSB pot fi citite și scrise mai rapid, ceea ce le face utile pentru lucrul cu fișiere mari. XLSB este rareori folosit pentru a stoca registre de lucru, deoarece XLSX (și anterior [XLS](/ro/spreadsheet/xls/)) sunt cele mai comune formate de fișiere selectate de utilizator pentru salvarea registrelor de lucru. Poate fi deschis de Microsoft Office 2007 și versiuni ulterioare.

## Specificații pentru formatul fișierului XLSB ##

Specificațiile de format de fișier pentru formatul de fișier XLSB au fost făcute publice încă din 2008 ca versiunea 1.0. De atunci, specificațiile au fost revizuite de mai multe ori și cea mai recentă versiune a specificațiilor (v 10.0) a fost publicată în aprilie 2018. Specificațiile sunt disponibile public de Microsoft ca [[MS-XLSB] - Specificații Excel Binary File Format](https:/ /msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx) și ar trebui să fie consultat de oricine pentru citirea sau scrierea fișierelor în format de fișier XLSB.

## Structura fișierului XLSB ##

Un fișier XLSB este un pachet care constă dintr-o colecție de părți. Aceste părți conțin informații despre conținutul unui registru de lucru, inclusiv date din registru de lucru și structura pachetului. Unele părți conțin informații stocate folosind înregistrări binare, unele ca XML, în timp ce altele conțin informații stocate ca flux binar de octeți. Fiecare înregistrare binară conține zero sau mai multe câmpuri structurate care conțin datele din registrul de lucru.

#### Pachet ####

Un pachet XLSB este o arhivă [ZIP](/ro/compression/zip/) care trebuie să conțină exact o parte din registru de lucru. Această parte trebuie să fie ținta unei relații în această parte a relației pachet. Partea registrului de lucru este partea de pornire a documentului XLSB.

#### Partea ####

O parte este un flux de octeți care are asociat un tip de conținut care specifică natura și tipul de conținut stocat în parte. Unele părți stochează informații în format binar, în timp ce altele stochează informații ca XML. Secțiunea [Enumerarea părților](https://msdn.microsoft.com/en-us/library/dd924091(v#office.12).aspx) a documentului cu specificații enumeră părțile valide, tipurile de conținut și relațiile obligatorii/opționale dintre toate piesele într-un pachet.

#### Relație ####

O sursă și o resursă țintă sunt conectate printr-o relație. O relație poate fi:

**Relația pachetului:** unde ținta este o parte și sursa este pachetul ca întreg

**Relație parte-la-parte:** unde ținta este o parte și sursa este o parte a pachetului

**Relație explicită:** în cazul în care o resursă este referită din conținutul unei părți sursă prin referirea valorii atributului ID a unui element de relație

**relația implicită** este o relație care nu este explicită

**Relație internă:** unde ținta face parte din pachet

**Relație externă:** unde ținta este o resursă externă care nu se află în pachet

#### Record ####

O înregistrare este elementul de bază folosit pentru a stoca informații despre caracteristici într-un registru de lucru. Fiecare înregistrare binară este o secvență de octeți cu lungime variabilă. O înregistrare binară constă din trei componente:

* un tip de înregistrare
* o dimensiune record, și
* datele de înregistrare care sunt specifice tipului de înregistrare respectiv.

**Tipul de înregistrare:** Tipul de înregistrare arată tipul de înregistrare specificat de înregistrare. De asemenea, se specifică structura datelor de înregistrare specifice acestei înregistrări. Tipurile de înregistrări valide sunt listate în secțiunea [Enumerarea înregistrărilor](https://msdn.microsoft.com/en-us/library/dd953057(v#office.12).aspx) a documentului cu specificații. Tipul de înregistrare trebuie să fie unul sau doi octeți și trebuie să fie mai mare sau egal cu 128 și mai mic de 16384.

**Dimensiunea înregistrării:** Mărimea înregistrării specifică numărul de octeți care specifică dimensiunea totală a datelor înregistrării. Această valoare TREBUIE să fie unul până la patru octeți. Această valoare TREBUIE să fie de un octet dacă bitul înalt din octetul inferior este egal cu 0; în caz contrar, această valoare TREBUIE să fie mai mare de un octet. Dacă numărul de octeți este mai mare de un octet, bitul înalt din fiecare octet succesiv specifică dacă este utilizat un octet suplimentar. Dacă bitul înalt al celui de-al doilea octet este egal cu 1, atunci această valoare TREBUIE să utilizeze un al treilea octet suplimentar. Dacă bitul înalt al celui de-al treilea octet este egal cu 1, atunci această valoare TREBUIE să utilizeze un al patrulea octet suplimentar. Bitul înalt al celui de-al patrulea octet TREBUIE ignorat. Valoarea constă din cei șapte biți inferiori ai fiecărui octet combinați. Biții mici, cei mai puțin semnificativi sunt conținuti în primul octet și fiecare octet succesiv conține biți de ordin mai mare decât octetul anterior.

**Date de înregistrare:** Componenta de date de înregistrare conține câmpuri care corespund unui anumit tip de înregistrare și cuprind restul înregistrării. Ordinea și structura câmpurilor pentru un anumit tip de înregistrare listat în Record Enumeration sunt specificate în secțiunea corespunzătoare pentru acel tip de înregistrare din Records. Dimensiunea totală a componentei de date de înregistrare TREBUIE să fie egală cu dimensiunea înregistrării. Câmpurile din componenta de date de înregistrare pot conține valori simple, matrice de valori, structuri ale mai multor câmpuri, matrice de câmpuri și matrice de structuri.

#### Exemplu de înregistrare XLSB ####

Următorul tip de înregistrare și dimensiunea înregistrării specifică o înregistrare **BrtCommentText** cu o dimensiune de 200 de octeți:

11111101 00000100 11001000 00000001 [Câmpuri de înregistrare]

Primul octet este 11111101, specificând o valoare scăzută de 125 și că tipul de înregistrare necesită un al doilea octet. Al doilea octet este 00000100, specificând o valoare mare de 4 * 128, care este egală cu 512. Valoarea tipului de înregistrare este 125 + 512 sau 637, care corespunde unui tip de înregistrare **BrtCommentText**. Următorul octet este 11001000, specificând o valoare scăzută de 72 și că dimensiunea înregistrării necesită un al doilea octet. Al doilea octet este 00000001, specificând o valoare mai mare de 1 * 128 și că dimensiunea înregistrării nu necesită un octet suplimentar. Dimensiunea înregistrării este 72 + 128 sau 200, ceea ce specifică dimensiunea totală, în octeți, a componentei de date de înregistrare. Câmpurile din componenta de date de înregistrare sunt specificate de **BrtCommentText**.

## Referințe ##

* [[MS-XLSB] - Format de fișier binar Excel (.xlsb)](https://msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx)

