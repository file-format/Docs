{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier CMS - Fișier profil serviciu Connection Manager",
  "description":"Aflați despre fișierele CMS și API-urile care pot crea și deschide fișiere CMS.",
  "linktitle" : "CMS",
  "menu" : {
    "docs" : {
      "identifier": "misc-cms",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Ce este un fișier CMS?

Un fișier CMS este un fișier de date care conține informații de profil utilizate de Microsoft Windows Connection Manager. Permite utilizatorilor de la distanță să se conecteze la o rețea folosind aceste informații de profil. Informațiile stocate în interiorul unui fișier CMS includ date despre sistemul de operare al utilizatorului și permisiunile care sunt utilizate pentru a stabili o conexiune între un utilizator la distanță și rețea. Administratorii CMS folosesc Connection Manager Administrator Kit (CMAK) pentru a genera fișiere CMS.

## Format de fișier CMS - Mai multe informații

Fișierele CMS nu se găsesc în mod obișnuit pe computerele utilizatorului. Deoarece acestea sunt utilizate în mod special pentru a permite utilizatorilor de la distanță să intre într-o rețea, le veți găsi pe computere care sunt utilizate pentru a se conecta la o rețea a companiei sau la un anumit birou cu scop specific. În cele mai multe cazuri, este folosit pentru a se conecta la o rețea organizațională, cum ar fi rețeaua privată virtuală (VPN), care este dedicată doar unei companii. Fiind administrator de rețea, veți configura accesul la o astfel de rețea cu Connection Manager pentru a-i permite să acceseze rețeaua companiei dintr-o locație de la distanță.

### Ce este insdie CMS?

Un fișier de profil CMS este creat utilizând Connection Manager și este împachetat cu alte fișiere de configurare înainte de a fi furnizat utilizatorului de la distanță. Aceste fișiere suplimentare pot include un fișier CMP și și un fișier INF care sunt împachetate alături de un fișier [EXE](/ro/executable/exe/). Acest pachet complet este furnizat utilizatorului de la distanță pentru conectarea la rețea.

## Referințe

* [Înțelegerea și configurarea Windows Connection Manager](https://docs.microsoft.com/en-us/windows-hardware/drivers/mobilebroadband/understanding-and-configuring-windows-connection-manager)

