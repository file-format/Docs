{
  "date" : "2021-28-05",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAR - File dei rapporti di Microsoft Access",
  "keywords" :[ "mar", "file mar", "formato file mar", "che cos'è il rapporto di accesso", "rapporto di accesso", "rapporto di accesso microsoft"],
  "description":"Informazioni sul formato di file Acess Report (MAR) utilizzato dal software Microsoft Access per creare un collegamento o un collegamento a Microsoft Access Report.",
  "linktitle" : "MAR",
  "menu" : {
    "docs" : {
    "identifier": "reporting-mar",
      "parent" : "reporting"
}
},
  "lastmod" : "2021-28-05"
}

## Che cos'è il rapporto di accesso (file MAR)? ##
Un file creato da Microsoft Access come collegamento del relativo report viene salvato con estensione di file .mar. Un **report di Microsoft Access** offre un modo per formattare, visualizzare e riepilogare le informazioni nel database di Microsoft Access. Questi report consentono di formattare i dati in un layout preciso e informativo per la visualizzazione su schermo o la stampa. Il report mostra solo i dati statici, il che significa che non possiamo modificare i dati nelle tabelle durante la visualizzazione del report di Access. Il report mostra i dati più recenti quando viene aperto.

## Formato file di Microsoft Access Report (MAR).

Il formato di file MAR viene utilizzato dal software Microsoft Access per creare un collegamento o un collegamento a Microsoft Access Report, che è un oggetto di database che diventa utile quando è necessario presentare le informazioni nel database per uno dei seguenti usi:

- Visualizza un riepilogo dei dati.
- Archivia le istantanee dei dati.
- Visualizza i dettagli sui singoli record.
- Crea etichette.

## Parti del rapporto di accesso
La progettazione di un report di Access è suddivisa in diverse sezioni che possono essere visualizzate nella vista Progettazione. La tabella seguente spiega come funziona ogni sezione e come può aiutarti a creare rapporti.
| Sezione | Come viene visualizzata la sezione quando viene stampata | Dove può essere utilizzata la sezione |
---------|----|------|
| Intestazione rapporto | All'inizio del rapporto. | Utilizza l'intestazione del rapporto per le informazioni che normalmente potrebbero apparire su una copertina, come un logo, un titolo o una data. Quando si inserisce un controllo calcolato che utilizza la funzione di aggregazione Somma nell'intestazione del report, la somma calcolata è per l'intero report. L'intestazione del rapporto viene stampata prima dell'intestazione della pagina. |
| Intestazione pagina | In cima ad ogni pagina. | Utilizza un'intestazione di pagina per ripetere il titolo del rapporto su ogni pagina. |
| Intestazione gruppo | All'inizio di ogni nuovo gruppo di record. | Utilizzare l'intestazione del gruppo per stampare il nome del gruppo. Ad esempio, in un report raggruppato per prodotto, utilizzare l'intestazione del gruppo per stampare il nome del prodotto. Quando si inserisce un controllo calcolato che utilizza la funzione di aggregazione Sum nell'intestazione del gruppo, la somma è per il gruppo corrente. Puoi avere più sezioni di intestazione di gruppo in un rapporto, a seconda di quanti livelli di raggruppamento hai aggiunto. Per ulteriori informazioni sulla creazione di intestazioni e piè di pagina di gruppo, vedere la sezione Aggiungere raggruppamenti, ordinamenti o totali. |
| Particolare | Appare una volta per ogni riga nell'origine record. | Qui è dove si posizionano i controlli che costituiscono il corpo principale del report. |
| Piè di pagina del gruppo | Alla fine di ogni gruppo di record. | Utilizzare un piè di pagina di gruppo per stampare le informazioni di riepilogo per un gruppo. È possibile avere più sezioni di piè di pagina di gruppo in un report, a seconda di quanti livelli di raggruppamento sono stati aggiunti. |
| Piè di pagina | Alla fine di ogni pagina. | Utilizzare un piè di pagina per stampare i numeri di pagina o le informazioni per pagina. |
| Piè di pagina del rapporto | Alla fine del rapporto. Nota: nella visualizzazione Progettazione, il piè di pagina del report viene visualizzato sotto il piè di pagina della pagina. Tuttavia, in tutte le altre visualizzazioni (visualizzazione Layout, ad esempio, o quando il report viene stampato o visualizzato in anteprima), il piè di pagina del report viene visualizzato sopra il piè di pagina, subito dopo l'ultimo piè di pagina del gruppo o la riga di dettaglio nella pagina finale. | Utilizzare il piè di pagina del report per stampare i totali del report o altre informazioni di riepilogo per l'intero report. |






## Riferimenti ##

- [Introduzione ai report in Access](https://support.microsoft.com/en-us/office/introduction-to-reports-in-access-e0869f59-7536-4d19-8e05-7158dcd3681c)
- [Progettazione di report in Access](https://www.uis.edu/informationtechnologyservices/wp-content/uploads/sites/106/2013/04/DesigningReportsinAccess2010.pdf)

